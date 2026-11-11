# The Tracking Site on Your Label Is Gone: tracking a carrier that renamed

You type the tracking website printed on the parcel or in the dispatch email, and nothing comes up. Not "number not found" — nothing at all.

The usual cause is not a lost parcel. Couriers are sold, merged and rebranded, and the old tracking portal dies with the old brand while the number keeps working somewhere else.

## The short version

**A rename never invalidates your tracking number.** Nothing is reissued when a brand changes, so the number already printed on your label still resolves. What breaks is the signpost: the old URL, and every email, help article and macro that mentioned the old brand.

## The clearest current example: Toll → Team Global Express

| | |
|---|---|
| Old brand | Toll Global Express (the Global Express division of Toll Group, Australia) |
| What happened | Toll Group sold the division to Allegro Funds; it began trading as **Team Global Express** in 2022 |
| Domestic parcel arm | Still **IPEC** (Interstate Parcel Express Company) |
| Old portal | **MyToll** — checked 3 October 2026: neither `mytoll.com` nor `www.mytoll.com` returns a page |
| Current portal | **MyTeamGE**, `myteamge.com` |

Because several systems kept their own spelling, one Australian shipment can reach you labelled **Toll**, **Toll IPEC**, **Toll Road Express** or **Team Global Express**. They are one network, not four.

### Reference, consignment note or purchase order?

Team Global Express's own search box says it accepts "up to 30 shipments, references, sorry we missed you card numbers or purchase orders". That is useful, but it also means the reference a sender gives you may not be a consignment number at all. If the number you were given does not behave like a tracking number, go back and ask for the **consignment number** specifically.

### What the number looks like

Team Global Express consignment numbers are **22 digits beginning 64**: a four-digit prefix, a thirteen-digit consignment number, then a three-digit item sequence. If an order shipped as several boxes, those numbers are identical except for the last three digits.

Do not identify a carrier by length alone — several US numeric labels are also 20–22 digits.

## It is not a one-off

| Carrier | Change |
|---|---|
| Toll Global Express | Sold to Allegro Funds, renamed Team Global Express (2022) |
| CIRRO E-Commerce | Founded as PARCLL, renamed CIRRO E-Commerce (April 2023), acquired by GOFO (February 2026) |

Every step like that leaves old labels, old dispatch emails and old links pointing at a brand that no longer answers.

## What to do when a tracking site returns nothing

1. **Check whether the company still exists under that name** before assuming the parcel is lost. Search the brand together with "renamed" or "acquired" — the new portal is usually in the first few results.
2. **Keep your number.** It was not reissued.
3. **Or skip the brand entirely:** paste the number into a universal tracker such as [24hTrack](https://www.24htrack.com), which works the carrier out from the number itself, so a dead brand name cannot stop you. Free, no account, 3,200+ carriers.

## If you run a store

- Search your email templates, help-centre articles and support macros for **carrier names**, not just URLs. The name is what customers search for.
- Treat `carrier` as an **editable field on the shipment**, not a constant written at order creation. Rebrands, acquisitions and last-mile handovers all change it after the fact.
- Expect **several spellings of the same network** in your data, and normalise them before you report on carrier performance.

## When the brand merges but the tracking systems don't: FedEx and TNT

A rename is one problem. A **merger where the tracking systems stay separate** is a different one, and it produces the same symptom: a real number that returns nothing.

FedEx acquired TNT in 2016. Today tnt.com carries FedEx's own intellectual-property notice and the line *"TNT will become FedEx"*. It is reasonable to conclude from that that a TNT number is now a FedEx number. It is not — and TNT's own customer FAQ still states it plainly:

> "FedEx shipments can be tracked at fedex.com, and TNT consignment tracking is available at tnt.com."

One group, two tracking tools. Paste a TNT consignment number into FedEx tracking and you will usually get nothing back, which looks exactly like a lost parcel.

| | |
|---|---|
| What changed | Ownership: FedEx acquired TNT in 2016 |
| What did **not** change | The tracking systems. TNT consignments are still looked up with TNT's tool |
| TNT consignment number | TNT's own tracking help describes 8-9 digits, no letters |
| Known quirk | TNT states those 8-9 digit numbers "get reused every three or four weeks" |

### TNT is not Team Global Express

These two get mixed up constantly, and this page discusses both, so it is worth being explicit: **Team Global Express is not a renamed TNT.** Its own About page says it began as Team Global Express following its acquisition from **Toll Group**, and traces its heritage to Albert F Toll's 1888 transport business. TNT Australia's own site, meanwhile, still trades as TNT and carries a property notice in the name of TNT Holdings B.V.

They are separate carriers that both move freight in Australia. Each one's tracking only finds its own consignments, so the first thing to check is which name is actually printed on the consignment note.

## When the brand merges and the scans change name mid-journey: Yodel and InPost

The FedEx/TNT case above is a merger where the tracking systems stayed apart. The opposite case is
worth knowing too, because it produces a very different and much more alarming symptom: the number
keeps working, and the **brand inside your scan history changes halfway down**.

Yodel, one of the UK's larger parcel carriers, is the live example. Its own site now trades as
**Yodel by InPost** and carries a banner telling customers that tracking has moved to InPost,
pointing them at inpost.co.uk and the InPost app. The legal entity behind the site is InPost
Delivery Network Limited.

What that does to a scan list is the part nobody warns you about. A typical history on a Yodel
number opens in Yodel's own voice at a national hub, moves to a local site written as a service
centre, and then switches wording entirely:

```
HATFIELD TERMINAL             your parcel is at our national hub
LUTTERWORTH                   your parcel is at our national hub
BIRMINGHAM SERVICE CENTRE     your parcel has arrived at your delivery depot
INPOST                        your parcel is on its way to InPost
INPOST                        we have your parcel
INPOST                        your parcel has been dropped off at the locker
```

Nothing has gone wrong there and the number has not been reused. It is one parcel, one number, and
one company that now has two names on it.

| | |
|---|---|
| What changed | Ownership and branding: InPost acquired Yodel; the site trades as Yodel by InPost |
| What did **not** change | Your number. A Yodel number issued before the change still tracks |
| Yodel number format | 3 letters followed by 16 digits, 19 characters in total; a minority are 2 letters and 16 digits |
| Where it now resolves | Yodel's own site directs tracking to inpost.co.uk and the InPost app |
| Common misreading | Seeing "InPost" and concluding the parcel was handed to a random third party |

### Two practical consequences

**For recipients.** A line naming an InPost locker or an InPost Shop is not a delay — it is a
collection, and the code is in your email or the app. Read the place name rather than the clock: a
record resting at a national hub is still in the trunk network and a quiet day there is normal,
while a record at a local service centre means the town that delivers it already has it.

**For anyone storing this data.** If your system holds one carrier string per shipment, this breaks
it. The company that *issued* the number and the company *handling it right now* are different
questions, and a rebrand changes the second without touching the first. Keep an alias table that
maps `Yodel`, `Yodel by InPost` and InPost-worded scans on a Yodel number to one operator, or your
per-carrier delivery times and exception rates will quietly split across two labels and the carrier
will look like it lost half its volume overnight.

## See also

- [Carrier Name Collisions: When Two Couriers Share a Name](carrier-name-collisions.md)
- [Tracking Number Formats](tracking-number-formats.md)
- [How to Track Any Package, Even If You Don't Know the Carrier](how-to-track-a-package.md)
