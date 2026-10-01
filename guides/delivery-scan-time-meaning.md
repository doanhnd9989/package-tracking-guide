# "Delivered at 21:49" — what the time on a delivery scan actually means

*Last updated: 2026-10-01*

A delivery scan has a time on it. That time is not what most people assume, and three
separate things go wrong with it. This guide separates them, because the fix is different
for each.

## 1. The time belongs to the carrier's clock, not yours

Every line on a tracking page comes from a scan: a device in a facility, or in a driver's
hand, recording a time **where the scan happened**. Carriers publish that wall-clock
reading, and most of them publish it without saying which timezone it belongs to.

That matters, because a tracking page that converts the time anyway is guessing. Tag an
offset-less time as UTC and re-render it in the reader's timezone, and a 09:57 delivery in
Germany shows as 16:57 to a reader in Vietnam. Nothing errors. The page simply displays a
time that nobody published.

This is why the same parcel can show two different delivery times on two different sites.
Only one of them is the carrier's.

**What to do:** before arguing about the minute, check the same scan somewhere that shows
the carrier's own number unconverted.

## 2. A late-evening delivery scan is ordinary

Measured on delivery scans that carry a time of day, flowing through the 24hTrack platform
(sample of roughly 22,000 parsed delivery events):

| Window | Share of delivery scans |
|---|---|
| Late morning to mid-afternoon (peak) | roughly 8–9% per hour |
| 20:00 – 05:59 | **about 9%, or ~1 in 11** |

So a scan stamped 21:49 is unusual for you and completely ordinary for the network.
Contract and gig drivers finish the route they were assigned, and in peak season that runs
later. An evening delivery time is not evidence of anything by itself.

## 3. Some delivery scans have no time at all

| | Share |
|---|---|
| Delivery scans carrying a time of day | ~96% |
| Date only, no clock | **~4%** |

About one delivery scan in twenty-five publishes only the date. If a page shows you
`00:00` for one of those, that midnight came from a date parser, not from a courier — and
the exact minute you are arguing about never existed.

## The field that actually helps: the location

On a delivery scan, the **place** is worth more than the minute.

- "Delivered" with **your town** on it → look at your own property first.
- "Delivered" at a **depot, locker, collection point or access point** → the parcel was
  signed off somewhere else. That is a different conversation, and a stronger one.

Screenshot that line, not the timestamp.

## If the time and your reality disagree

1. **Read the note on the scan** — "left with", "safe place", "signed by". The useful part
   is usually there, not in the headline.
2. **Check everywhere a box could sit** — porch, side gate, bin store, reception, a
   neighbour who takes parcels in.
3. **If you have a camera, review about an hour either side of the scan**, not the exact
   minute. The driver scans at the stop, so the scan and the drop can be minutes apart.
4. **Give it one night.** A small share of parcels are scanned delivered a little early and
   appear the next morning.

## Then go to the seller — for a claim, not an update

If it still has not appeared, the next message is to the **seller**, not the carrier. The
seller bought the shipping, so they are the carrier's customer, and most carriers will only
open an investigation for whoever holds that contract.

Give them three things: the date, the time **exactly as the carrier published it**, and the
location on that line.

What a tracking lookup cannot give you, so you know where to stop asking: your address, the
driver's name, a signature, or a delivery photo. Only the carrier holds those, and the
seller is the one who can request them.

A delivered scan is **evidence, not a verdict**. Claims for parcels marked delivered but
never received are routine.

## FAQ

**Can a delivery scan simply be wrong?**
Yes. A person and a device produce it, so it can be early, late, or occasionally entered at
the wrong stop.

**Why does my friend see a different delivery time for the same parcel?**
Because some pages convert the time into the viewer's timezone and some print the carrier's
own reading. See section 1.

**Does a "delivered" scan mean I cannot claim?**
No. See above — it is evidence, not a verdict.

**Is a midnight delivery time real?**
Usually not. Check whether the carrier published a time at all; `00:00` is the classic
signature of a date-only scan run through a date parser.

## Related

- [Package delivered but not received](package-delivered-but-not-received.md)
- [Who to contact about a parcel problem](who-to-contact-parcel-problem.md)
- [Tracking status meanings](tracking-status-meanings.md)

---

Numbers in this guide are measured on delivery scans from the
[24hTrack](https://www.24htrack.com) platform and are shares, not counts. 24hTrack is a
free package tracker for 3,200+ carriers — paste any tracking number, the carrier is
detected automatically, no sign-up. Licensed CC BY 4.0.
