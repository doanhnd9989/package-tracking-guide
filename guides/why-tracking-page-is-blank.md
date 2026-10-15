# Why a Tracking Page Comes Back Blank (Measured: 97% vs 1 in 5)

A blank tracking page is the single most common reason people think a parcel is lost. It almost never
means that. This guide explains what an empty page actually tells you, backed by a measurement across
three large carriers, and gives you a three-step check that resolves nearly every case.

## The measurement

We counted every tracking number pasted into [24hTrack](https://www.24htrack.com) over 30 days,
grouped by carrier, and asked one question of each group: what share of these numbers ever reached a
real status?

| Carrier | Share of numbers that reached a status | Scans on numbers that reported |
|---|---|---|
| UPS | ~97% | ~12 |
| FedEx | ~1 in 3 | ~11 |
| Australia Post | ~1 in 5 | ~12 |

Two things stand out.

First, the spread is enormous — on the same site, on the same day. That is not one carrier being
"better" at delivering. It is a difference in how openly each network publishes its scans.

Second, look at the right-hand column. When a number does report, all three carry roughly the same
amount of history: about a dozen scans from label to doorstep. So this is not a story about some
carriers being vague and others thorough. Every one of them is thorough **once something arrives**.
The entire difference is whether anything arrives at a third-party page at all.

## What a blank page actually means

There are three honest explanations, in order of how often they apply.

**1. The label exists, the box has not been scanned yet.** The seller buys a shipping label and the
carrier issues the number that same second. Nothing has been collected. Carriers write this as
"Label Created", "Shipment Information Received" or "Info Received" — and many tracking pages show
nothing at all until the first physical scan. This resolves itself the moment the parcel is actually
collected, and it is by far the most common case.

**2. The number belongs to a network that page cannot read.** Nothing is wrong with your parcel and
nothing is wrong with your number. You are standing at the wrong window. The carrier's own site is
the authoritative source for its own numbers.

**3. What you have is the shop's order reference, not a carrier tracking number.** These look similar
enough to fool anyone. An order reference will never work on any tracking site, because no carrier
ever issued it. See
[order number vs tracking number](order-number-vs-tracking-number.md).

Note what is *not* on this list: theft, loss, or a parcel that was never sent. An empty page is a
statement about information, not about a box.

## The three-step check

**Step 1 — the carrier's own site, same number.** If it is alive there and blank elsewhere, your
parcel is fine and you are done.

**Step 2 — read the shape.** A UPS parcel number is `1Z` followed by sixteen letters and digits
(eighteen characters in total). A FedEx number is almost always twelve digits with no letters. If
your string looks nothing like the carrier named on your order confirmation, you are probably holding
the wrong thing. Full reference: [tracking number formats](tracking-number-formats.md).

**Step 3 — ask the seller for the collection date.** Not the order date, not the dispatch date.
*Collected.* That single date is the only thing that tells you whether a box exists inside the
network at all, and most sellers can answer it in one line.

## How long to wait before any of this matters

For parcels that were still moving when first tracked, measured over 120 days:

| Carrier | Median to delivery | 80% delivered within |
|---|---|---|
| FedEx | ~2 days | ~6 days |
| UPS | ~4 days | ~7 days |
| Australia Post | ~6 days | ~13 days |

Australia Post's long tail is mostly inbound international mail, where a flight and a customs queue
are part of the wait. Cross-border parcels in general behave differently from domestic ones — see
[why international parcels look like they are going in circles](international-parcel-journey-explained.md).

## For sellers

If you ship on a carrier that reports thinly outside its own site, sending customers to a generic
tracking link creates the ticket you were trying to avoid: they see a blank page and read it as
"lost". Link them to the carrier's own page instead, and tell them the collection date rather than
the label date.

## Related

- [Label created / info received — how long it lasts](label-created-info-received.md)
- [Tracking not updating](tracking-not-updating.md)
- [Two tracking sites disagree — which one is right?](tracking-sites-disagree.md)
- [What every tracking status means](tracking-status-meanings.md)

---

*Data: numbers tracked on [24hTrack](https://www.24htrack.com), a free multi-carrier package tracker
(3,200+ carriers, no sign-up). Shares and medians only — no absolute volumes. CC BY 4.0.*
