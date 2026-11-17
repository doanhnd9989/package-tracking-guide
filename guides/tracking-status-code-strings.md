# Your Tracking Line Isn't a Sentence: BAG_DISPATCH, droppedOffAtVeho and TRANSITOTRANSITO Decoded

Sometimes a tracking history stops speaking English and starts speaking code. The line reads
`BAG_DISPATCH`, or `droppedOffAtVeho`, or `TRANSITOTRANSITO`, and it looks like something broke.
Nothing broke. You are reading the name of a field inside the carrier's own system, published to you
exactly as the carrier's software stores it.

## Short answer

A status written without spaces — `ITEM_RECEIVE`, `pickedUpFromVeho`, `PackageLoadedOntoFirstMileTransit` —
is an internal event code that was never rewritten into a sentence for customers. It describes a
perfectly ordinary step: a bag of mail moved, a parcel was handed over, a van was loaded. These lines
are rare, but they are not a single carrier's quirk: strings like this turn up on histories from close
to three hundred different carriers, and fewer than one tracking line in three hundred is written this
way. If your parcel's latest line is one of them, no action is needed — read it as the step it names
and look at the next ordinary line for confirmation.

## The five shapes, with real examples

### 1. SCREAMING_SNAKE_CASE — the enum straight out of the database

Seen on India Post histories: `BAG_DISPATCH`, `ITEM_RECEIVE`, `ITEM_DISPATCH`, `CUSTOM_RECEIVE`,
`TMO_RECEIVE`, and the mixed-case variant `Bag_Forward`.

Postal networks move mail in bags, not just as individual items, so their event vocabulary has words
for both. `ITEM_RECEIVE` is your parcel being booked in somewhere. `BAG_DISPATCH` is the sack
containing it leaving for the next office. `CUSTOM_RECEIVE` is customs taking it in. These are
sequential steps, so seeing a bag-level line does not mean your item was lost inside a bag — it means
the office recorded the bag's movement rather than yours at that moment.

### 2. camelCase and PascalCase — the API field name

Seen on Veho histories in the United States: `droppedOffAtVeho`, `pickedUpFromVeho`,
`PackageArrivedAtFacility`, `PackageDepartedFromFacility`, `PackageLoadedOntoFirstMileTransit`,
and plain `created`.

These are readable once you split them at the capitals. `droppedOffAtVeho` is the shop handing the
parcel over. `pickedUpFromVeho` is it leaving a facility with a driver. `created` is the moment the
label existed, which is why it can appear days before anything physical happens. The same network also
writes plain-English versions of several of these on other items — *arrived at facility*, *departed
from facility*, *out for delivery* — so one order can show both spellings of the same journey.

### 3. The doubled word — a concatenation that was never meant to be seen

Seen on TIPSA and Cainiao histories: `TRANSITOTRANSITO`, `REPARTOREPARTO`.

Read them as two copies of one Spanish word: *TRÁNSITO* (in transit) and *REPARTO* (out for delivery).
The doubling is the signature of a code field and a label field being joined with nothing between them,
which is also why the accent is missing. The useful part is the word itself: `TRANSITOTRANSITO` is in
transit, `REPARTOREPARTO` means it is out with a courier.

### 4. Two writing systems glued together

Seen on China Post histories: `邮件到达处理中心Shenzhen`, `邮件离开处理中心Yiwu`.

The Chinese phrase means *the item arrived at* or *left the processing centre*; the English word after
it is the city, with no space, because a place name was appended to a template. There is a second
China Post pattern that does separate them, using full-width brackets — `邮件到达处理中心【HK】` — and that
one is the same event, written more carefully.

### 5. The standards code that looks like a typo

`Posting/Collection` appears, character for character, on histories from a long list of national
posts — China Post, Japan Post, Deutsche Post, Russian Post, Pos Malaysia, Emirates Post, Kenya Post,
Bangladesh Post and more. When unrelated operators on different continents use an identical odd
string, that is the signature of a shared postal standard rather than one company's wording. Read it as
*the item was posted or collected*: the first event in the chain. `Pre-Shipment`, which turns up on
USPS and on some cross-border carriers, is the same kind of thing one step earlier — the label is
known, the parcel is not in the network yet.

## Decoder table

| What you see | What happened | Needs action? |
|---|---|---|
| `ITEM_RECEIVE` | Your item was booked in at a facility | No |
| `ITEM_DISPATCH` | Your item left for the next facility | No |
| `BAG_DISPATCH` / `Bag_Forward` | The mail bag holding it moved on | No |
| `CUSTOM_RECEIVE` | Customs took it in | No, unless a later line asks for documents or duty |
| `TMO_RECEIVE` | Received at a mail office in the postal chain | No |
| `created` | The label exists; the parcel may still be with the sender | No |
| `droppedOffAtVeho` | The shop handed it to the carrier | No |
| `pickedUpFromVeho` | It left the facility with a driver | No |
| `PackageLoadedOntoFirstMileTransit` | Loaded for the long leg toward your region | No |
| `PackageArrivedAtFacility` / `PackageDepartedFromFacility` | Passing through a hub | No |
| `TRANSITOTRANSITO` | In transit (Spanish *tránsito*) | No |
| `REPARTOREPARTO` | Out for delivery (Spanish *reparto*) | No — expect it today |
| `Posting/Collection` | Posted or collected: the first postal event | No |
| `Pre-Shipment` | Label known, parcel not yet in the network | Only if it lasts many days |
| `邮件到达处理中心<city>` | Arrived at the processing centre in that city | No |
| `邮件离开处理中心<city>` | Left the processing centre in that city | No |

## Why it happens at all

Every carrier stores an event as a short identifier plus, usually, a human sentence for each language
it supports. The identifier is stable and the sentence is not, so when a sentence is missing for your
language — or when an integration reads the identifier field by mistake — what reaches the page is the
identifier. It travels unchanged through every system between the carrier and your screen, which is why
two tracking pages can show you the same raw string. On 24hTrack these lines are shown as the carrier
published them, with a standard status alongside, so you can see both what the carrier said and what it
means.

## Rewriting them automatically only gets you halfway

Splitting at the capitals and the underscores is easy, and it does make most of these readable. It also
produces nonsense on the abbreviations: `TMO_RECEIVE` mechanically becomes *Tmo receive*, which is not
English either. That is the honest limit of the trick — the shape of the string can be cleaned up by a
rule, but the vocabulary still has to be learned per carrier. If you are building something, keep the
original text next to whatever you display, because the original is the only version that is
definitely correct.

## FAQ

### Is a code-like status a sign something went wrong?

No. In every pattern above, the event being described is an ordinary step — booked in, dispatched,
loaded, in transit, out for delivery. The formatting is the only thing that is unusual. Judge the
parcel by the *sequence* of lines and the dates, not by how the latest one is typed.

### My status says `created` and nothing else for days. Is that bad?

`created` means the label exists, which is not the same as the carrier holding your parcel. A gap
after it is normal for a day or two and common for longer when a seller prints labels in batches. The
person who can confirm a physical handover is the sender, not the carrier — the carrier cannot scan
something it has not received.

### Why does one of my lines say `BAG_DISPATCH` instead of naming my parcel?

Because postal networks track containers as well as contents. When a sack of mail leaves an office,
that movement gets recorded against the items inside it. It is a normal step on a postal route and it
usually sits between an item-level booking in and an item-level dispatch.

### Can I make these lines display properly?

On your own tracking page, you can: split at underscores and capital letters, collapse a doubled word
to one copy, and keep a lookup table for the abbreviations that a split cannot fix. Pasting the number
into a tracker that normalises statuses is the quicker route if you only want to read it — on 24hTrack
each carrier's wording is mapped to one standard status while the carrier's own line is kept in the
history underneath.

---

*Part of the [Package Tracking Guide](../README.md). Canonical tracking: [24hTrack](https://www.24htrack.com/).*
