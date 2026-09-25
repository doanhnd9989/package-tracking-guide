# "Delivery Attempted" — What It Actually Records, and What Happens Next

**Short answer:** a *delivery attempted* scan records that a parcel went back on the van, not a claim
that nobody was home. Across parcels tracked on the 24hTrack platform whose outcome is already
settled, **82% of parcels that got an attempt scan were delivered anyway** — 44% within 24 hours,
65% within 48, and 89% within a week. The median wait after the attempt is about **27 hours**. Only
four phrases in the attempt wording mean you have to do something today.

---

## What the status is, mechanically

A driver presses a button on a handheld scanner to record that a parcel is going back to the depot
undelivered. That is the whole event. The button records *that* it came back — the reason field is
optional, often auto-filled, and frequently wrong about intent even when it is right about fact.

This is why "delivery attempted" and "you were out" are not the same statement. The second is an
interpretation the tracking page invites and the scan does not support.

## The most common reason is not "nobody home"

Ranked by how often the wording appears in the scans we see:

1. **"No access to delivery location"** — by a wide margin the most common. A locked lobby, a gate
   with a code the seller never passed on, an entry phone that rings a flat number that does not
   match the label, a business address after closing time.
2. **"Unsuccessful delivery"** — no reason given at all.
3. **"Could not contact the customer"** — the buzzer or the phone number failed.
4. **"Address is incorrect / insufficient"** — the only one of the four you must act on.

The practical consequence: read the wording under the status, not the status itself. A red banner
saying *Exception* tells you nothing; the line under it usually tells you everything.

## How long it takes after an attempt

Measured from the first attempt scan to the delivery scan, on parcels whose outcome is settled:

| Delivered within | Share of parcels |
|---|---|
| 24 hours | 44% |
| 48 hours | 65% |
| 72 hours | 75% |
| one week | 89% |

Median: about 27 hours. In other words, one ordinary working day.

## Most parcels are attempted once, not three times

- **22%** ever show a *second* attempt scan.
- **9%** reach a third.

That surprises people who expect the classic "three attempts then returned" rule. It fits the main
reason, though: if the obstacle was a locked door at two in the afternoon, the same driver on the
same route the next morning often simply gets in — and the successful delivery is the next scan you
see, with no second attempt recorded at all.

## It depends on who is carrying it

| Carrier | Delivered in the end | Typical wait after the attempt |
|---|---|---|
| DHL | 87% | about 1 day |
| USPS | 88% | about 1 day |
| AliExpress route | 64% | about 2 days |
| China Post | 61% | about 3 days |
| Cainiao | 93% | about 6 days |

Domestic carriers retry fast because the same van comes back. Cross-border routes are slower
because an attempt near the end of the journey is often followed by a *handover* to a different
local company rather than by a retry — the next scan can come from a carrier that was not involved
when the parcel shipped.

Full per-carrier numbers: [`data/delivery-attempt-outcomes.csv`](../data/delivery-attempt-outcomes.csv)
· [`.json`](../data/delivery-attempt-outcomes.json)

## The four phrases that do mean something is wrong

Everything above is a waiting game you are likely to win. These are not:

- **Address incorrect / insufficient** — fix it with the seller today. Nothing else will happen.
- **Duties or documents required** — the parcel is parked until you pay or send them.
- **Return to sender** — the retry window has already closed.
- **Held at depot for collection** — it is waiting for *you*, and collection windows expire, often
  in one to two weeks.

## What to do

1. **Give it 24 to 48 hours.** Two thirds arrive in that window with no action from anyone.
2. **Read the attempt wording**, not the banner.
3. **Message the seller, not the courier.** You are not the courier's customer — the seller bought
   the shipping and is the only party that can open a claim on it.
4. **If the number begins with TBA**, it is an Amazon reference. No third-party tracking site can
   open a delivery investigation on it; use Your Orders, because Amazon holds the delivery record.

## FAQ

**Does "delivery attempted" mean the driver actually came?**
It means the parcel went back to the depot undelivered. That usually involves a visit, but the scan
does not prove a doorbell was rung, and the reason field is often auto-filled.

**They marked it attempted but I was home all day. Is that a lie?**
Usually not. The most common recorded reason is no access to the building rather than no answer at
the door — a locked lobby, a gate, or an entry phone that did not work reaches the same outcome
without anyone knocking on your door.

**How many delivery attempts do carriers make?**
Fewer than the folklore suggests. In our data 22% of attempted parcels show a second attempt scan
and 9% a third; most are delivered on the next pass with no second attempt recorded.

**How long until they try again?**
Typically the next working day. 44% of attempted parcels were delivered within 24 hours and 65%
within 48.

**When should I contact someone?**
When the wording says the address is wrong, duties or documents are owed, the parcel is being
returned to sender, or it is being held for collection. Contact the seller, not the carrier.

---

*Numbers measured on parcels tracked with [24hTrack](https://www.24htrack.com), September 2026, on
parcels whose first attempt scan is at least 14 days old so the outcome is settled. Shares and
percentiles only — no parcel counts. Released under CC BY 4.0.*
