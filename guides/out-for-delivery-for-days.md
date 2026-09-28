# "Out for Delivery" for Days: What That Status Actually Promises

*Part of the [Package Tracking Guide](../README.md), maintained by [24hTrack](https://www.24htrack.com).*

Your tracking has said **Out for Delivery** for three days. Nobody knocked. The status has not
changed, and every refresh gives you the same three words.

Short version: that scan normally does mean *today* — but it is not a guarantee, it is not
standardised between carriers, and the thing that tells you which situation you are in is not the
headline status. It is the line underneath it.

## What the scan usually means

Measured on the 24hTrack platform across delivered parcels, from the **first** out-for-delivery scan
to the delivery scan:

| | |
|---|---|
| Median | **about 6 hours** |
| 80th percentile | about 9 hours |
| Still not delivered after 24h | **about 5%** (roughly 1 in 20) |
| Parcels with **more than one** out-for-delivery scan | **about 2.5%** (roughly 1 in 40) |

So the typical parcel really does arrive the same working day, and a parcel that is still out after a
full day is the exception rather than the rule. Three days is unusual — but a second attempt the next
morning is far and away the most likely explanation, so it is nowhere near rare enough to mean the
parcel is lost.

> **How to read these two tables.** The figures above are **per parcel**, and that pool is dominated by
> domestic US volume, so they describe a typical *parcel* rather than a typical *carrier*. The per-carrier
> table further down is the one to judge your own parcel against: on the slowest lanes in the set, two
> thirds of parcels are still "out for delivery" a day after the scan. An earlier version of this page
> reported the per-carrier average (6.5 hours, 1 in 6, 1 in 7) in this first table, which overstated how
> often a *parcel* runs past a day; corrected 2026-09-28.

## The three reasons it sticks

### 1. It went out, and it came back

The commonest cause, and the one people never see, is a failed attempt. The parcel genuinely went out
on the van, nobody could take it, and it went back to the depot that evening. In real carrier
wording, one day looks like this:

```
07:52  Your package is out for delivery
18:24  Unable to Deliver - Not answering phone calls/buzz
19:32  Your package has been returned to the local facility
21:09  Scheduled Delivery - Redelivery Processing in Progress
06:19  Your package is out for delivery          <- the next morning
```

If your tracking page only shows you the top-line status, all of that collapses into "Out for
Delivery" three days running. **Scroll into the scan history** — the failure and its reason are
usually recorded there. Common reasons include no answer at the door or buzzer, address could not be
located, and incorrect address.

That distinction matters because each one has a different fix. A driver can try again tomorrow. A
wrong address cannot be fixed by trying again.

### 2. The scan means different things at different carriers

"Out for delivery" is a label each carrier attaches at a moment of its own choosing. Some post it
when the parcel is physically loaded on a delivery vehicle. Others post it when the parcel arrives at
the local delivery depot, which can be the evening before.

Measured the same way, per carrier:

| Carrier | Median to delivery | 90th percentile | Still out after 24h |
|---|---|---|---|
| USPS | ~6h | 8.7h | ~4% |
| Austrian Post | 4.0h | 31.1h | 14% |
| GOFO | 7.0h | 16.3h | 5% |
| UniUni | 6.4h | 26.7h | 12% |
| Yanwen Express | 7.6h | 58.2h | 20% |
| China Post | 7.4h | 76.5h | 27% |
| One cross-border carrier in the set | 25.4h | 29.9h | **65%** |

Full table: [`data/out-for-delivery-dwell.csv`](../data/out-for-delivery-dwell.csv) ·
[JSON](../data/out-for-delivery-dwell.json)

That last row is the point. Two thirds of those parcels are still out 24 hours after the scan. That
is not a slower carrier — it is a scan posted at a different point in the journey. Judge your own
parcel against its own carrier's pattern, not against a general expectation.

### 3. You are reading a page that stopped

On a cross-border order, a local partner usually takes the final miles. The original carrier no
longer has the box, so its page freezes on the last thing it knew — and the last thing it knew is
often "out for delivery". The parcel moved on. The page did not.

A universal tracker shows both legs on one timeline, so you can see whether anything was scanned
after that status. If the export carrier's last scan is out-for-delivery and there is a separate
domestic number, the domestic one is the live one.

## What to do, in order

1. **Look for a second out-for-delivery scan, or an exception line.** That is a failed attempt, and
   it usually names the reason.
2. **If the reason points at your address, buzzer or access**, fix it with the **seller**, not the
   courier. The courier takes its instructions from the merchant who paid for the label — see
   [who actually fixes a parcel problem](who-to-contact-parcel-problem.md).
3. **If it says held for collection**, act today. Those hold windows expire, often within one to two
   weeks, and then the parcel goes back to the sender.
4. **If there is genuinely no new scan of any kind for three days**, stop refreshing and ask the
   seller to open a case. In most networks only the sender can.

## How to see the full history

Paste the number at [24hTrack](https://www.24htrack.com). The carrier is detected from the number
itself, so you do not need to know who is carrying it, and several numbers can go in at once if one
order shipped in pieces. It is free and there is no account.

Related: ["Delivery attempted" — what it actually records](delivery-attempted-what-it-means.md) ·
[Why is my tracking not updating?](tracking-not-updating.md) ·
[Tracking status meanings](tracking-status-meanings.md)

---

*Method: measured on delivered parcels only, from the first out-for-delivery-type scan to the
delivery scan. Parcels with unparseable timestamps and gaps over 30 days were excluded. Data is
published under CC BY 4.0.*
