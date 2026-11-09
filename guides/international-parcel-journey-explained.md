# Why Your International Parcel Looks Like It's Going in Circles

Your tracking page says the parcel left an airport, arrived at another airport, went through a sorting centre, departed again, and cleared some office you have never heard of. Two weeks in, it still is not at your door, and the obvious thought is: *this thing is going round the world and it is never coming to me.*

Almost always, it is coming. What you are looking at is not a lost parcel — it is a **normal cross-border journey with the lid off**. This guide explains each leg, shows how many scans a cross-border parcel really produces, and gives you a number-based way to tell "slow but fine" from "actually worth chasing".

## A cross-border parcel produces 3–5× more scans than a domestic one

This is the single most useful thing to know, and it is why international tracking *feels* chaotic when it is not.

Average tracking events per shipment, measured on parcels tracked at 24hTrack between 2026-03-20 and 2026-08-19:

| Carrier | Typical route | Avg. tracking events |
|---|---|---|
| Royal Mail | Domestic UK | 4.4 |
| UPS | Mostly domestic | 4.8 |
| Evri | Domestic UK | 8.5 |
| USPS | Domestic US | 10.2 |
| Cainiao | Cross-border | 18.1 |
| Yanwen Express | Cross-border | 18.8 |
| China Post | Cross-border | 21.6 |
| India Post | Cross-border | 23.4 |

A domestic parcel gets scanned four or five times. A parcel crossing a border gets scanned around twenty times, because it changes hands, buildings, companies and legal jurisdictions on the way. **Twenty lines of tracking is the sign of a well-documented parcel, not a confused one.**

Full table: [`data/carrier-transit-times.csv`](../data/carrier-transit-times.csv).

## The legs, in the order you will see them

Most international e-commerce parcels follow the same nine steps. The wording differs by carrier; the sequence rarely does.

1. **Shipping label created / order information received** — the seller has printed a label. The parcel may still be on a shelf. This step alone can sit for days.
2. **Collected / picked up** — the origin courier physically has it.
3. **Arrived at origin sorting centre** — often a city you have never heard of, near the seller, not near you.
4. **Export customs cleared** — the origin country has approved it for export.
5. **Departed on airline / handed to airline** — it is flying, or waiting for a flight with free cargo space. Silence here is normal.
6. **Arrived at destination airport** — first scan in your country.
7. **Import customs** — the slowest and least predictable step. See [Package Held at Customs](package-held-at-customs.md).
8. **Handed to local courier** — a *different company* now has your parcel. This is where most tracking pages go quiet (more below).
9. **At local depot → out for delivery → delivered.**

### "It went to another airport" is usually a transit hub, not a return

Seeing two or three airports is normal. Cargo rarely flies point-to-point; it moves through hubs. A parcel from mainland China to Europe routinely shows a scan in Hong Kong, Dubai, Leipzig or Istanbul on the way. A parcel to the US may show Incheon, Taipei or Anchorage.

Two things distinguish a hub from a genuine problem:

- **A hub keeps moving forward in time and generally toward you.** Departed → arrived → departed.
- **A real return shows words, not just places**: *return to sender*, *refused*, *undeliverable*, *redirecting to origin*. Airport names alone never mean the parcel is being sent back.

### Step 8 is why your tracking "dies"

Once the origin carrier hands the parcel to a local courier, the origin carrier usually stops adding scans — it no longer has the parcel. If you are tracking on the origin carrier's own website, the story simply stops, often with something vague like *handed over to local partner*.

The parcel is fine. The **tracking page** is the thing that ended. The remaining scans exist, but on the local courier's system, sometimes under a different number.

This is the main practical reason to use a universal tracker: [24hTrack](https://www.24htrack.com) detects the carrier from the number and keeps following the parcel past that handover, so both legs appear as one timeline. It is free and needs no account.

### Decoding "office of exchange"

Postal-network parcels describe the border in words almost nobody uses in daily life, and the lines look alarming when they are simply bookkeeping:

| What you see | What it means |
|---|---|
| Arrival at **outward** office of exchange | Reached the facility that hands post *out* of the sending country |
| Departure from **outward** office of exchange | Left that facility — the handover finished |
| Arrival at **transit** office of exchange | Reached a country your parcel only passes *through* |
| Arrival at **inward** office of exchange | Reached the facility that takes post *into* your country |

An office of exchange is just the building where two countries' postal systems hand items over. Seeing an *arrival* and then a *departure* at the same office is the pair you want: it means the step completed. None of these lines is a problem report, and none of them means your parcel changed direction.

### The same scan listed twice is one scan, not two

Some operators publish every event in more than one language — an English line and a line in the destination country's script, carrying the same timestamp. A tracking page that shows you what the operator published will therefore show both.

Count the timestamps, not the rows. If two rows share a minute and a facility, that is one event written out twice. It is worth knowing before you conclude your parcel bounced through sorting twice as often as it really did.

### A freight forwarder's number is not a courier's number

Step 8 above describes one carrier handing to another. There is a second, less obvious case: the number you were given was never a courier's number to begin with.

A **freight forwarder** arranges carriage — it books space on a ship or aircraft, consolidates many sellers' goods into one load, and handles export paperwork. It does not deliver to your door. Its tracking therefore records *the job*, not the parcel:

- **Order placed** — the booking exists
- **Goods received** — the forwarder physically holds the cargo
- **Dispatched** — the cargo has left the origin country

Three or four milestones is a *complete* forwarder record, not a truncated one, and those milestones are often published in the forwarder's own language because they are written for the business that booked the freight rather than for the person waiting at home. The record then ends when the cargo reaches your country and a domestic carrier takes over.

How to tell which kind of number you hold:

- A forwarder reference is usually short and irregular — it does not follow a fixed international pattern, because it is a job number rather than a postal barcode.
- If the history is three lines long, has no depot or door scans, and has not changed in weeks, ask the seller for **the last-mile carrier's number**. That is the one that carries a delivery date.
- If your seller shipped by sea rather than air, weeks of mid-journey silence is the shape of the trip, not a fault in it.

## How to tell "slow but normal" from "worth chasing"

Use the spread, not the average. Here is the same dataset showing the median alongside the 80th percentile — the point where only one parcel in five takes longer:

| Carrier | Median days | 80th percentile days | Spread |
|---|---|---|---|
| Cainiao | 7.2 | 12.1 | 1.7× |
| USPS | 9.4 | 12.7 | 1.4× |
| China Post | 11.0 | 17.8 | 1.6× |
| UniUni | 11.0 | 17.5 | 1.6× |
| AliExpress | 12.4 | 16.3 | 1.3× |
| **Yanwen Express** | **12.9** | **29.3** | **2.3×** |
| YunExpress | 13.3 | 19.0 | 1.4× |
| FXYL | 22.8 | 26.8 | 1.2× |

Transit time is measured from the first carrier scan to the delivery scan, so the clock starts in the origin country, not when you ordered.

Read it like this: with Yanwen Express, a typical parcel takes about 13 days, **but one in five takes 29 days or more**. Nothing has gone wrong at day 20 — you are simply in the slow fifth. That single fact is the answer to most "is it even coming?" questions.

A reasonable rule:

- **Before the median** — no action. Silence during a flight or customs is expected.
- **Between median and 80th percentile** — still normal. Check weekly, not hourly.
- **Past the 80th percentile, with no new scan for 10+ days after arriving in your country** — now it is worth contacting the seller. Domestic silence after an import scan is more meaningful than silence over an ocean.
- **Any of these words at any time** — act immediately, do not wait: *return to sender*, *refused*, *address invalid*, *awaiting payment of duties*, *held — documents required*.

## Quick answers

**Why does my parcel show so many airports?**
Air cargo moves through hubs. Two or three airport scans on an intercontinental parcel is normal routing, not a detour or a return.

**My tracking has not updated in 8 days. Is it lost?**
Usually not, if the last scan was a departure or a customs entry. Flights and customs queues produce no scans at all. Worry when the parcel has already been scanned *in your own country* and then goes quiet for more than about 10 days.

**The tracking stopped after "handed over to local partner". What now?**
The origin carrier no longer has it, so its page will never update again. Put the same number into a universal tracker such as [24hTrack](https://www.24htrack.com), which follows the parcel onto the local courier and shows both legs in one timeline.

**Does a parcel with 20 tracking events mean something went wrong?**
No — the opposite. Cross-border parcels average roughly 18–22 scans, against 4–5 for a domestic one. More scans means better visibility, not more problems.

**When does "in customs" become a real problem?**
Most clearances finish in a few days. If it sits more than a week, check for an unpaid duty or a missing document — those wait for *you*, and nothing moves until they are handled. See [Package Held at Customs](package-held-at-customs.md).

## Related guides

- [Why Is My Tracking Not Updating? Causes and How Long to Wait](tracking-not-updating.md)
- [Package Held at Customs: What It Means and What to Do](package-held-at-customs.md)
- [How to Track Packages from China (AliExpress, Temu, Shein and More)](track-packages-from-china.md)
- [Tracking Status Meanings: In Transit, Out for Delivery, Exception and More](tracking-status-meanings.md)

---

*Figures in this guide are computed from real shipments tracked on [24hTrack](https://www.24htrack.com) between 2026-03-20 and 2026-08-19; transit time runs from the first carrier scan to the delivery scan, with outliers under 6 hours and over 90 days excluded. Live version: [24htrack.com/carrier-statistics](https://www.24htrack.com/carrier-statistics). Text is CC BY 4.0 — reuse it with a link.*
