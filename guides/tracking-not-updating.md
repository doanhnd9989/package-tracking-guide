# Why Is My Tracking Not Updating? Causes and How Long to Wait

> Canonical version: https://www.24htrack.com/blog/tracking-not-updating

A tracking page that has not moved in days usually means the parcel is somewhere with no scanner: on a plane, in a shipping container, in a customs queue or waiting for the next truck. Silence is normal on some legs of a journey and a warning sign on others.

## Short answer

Tracking stops updating when the parcel is between scan points: on a flight or ship, in customs, or waiting at a sorting hub. Gaps of 3 to 7 days are common on international routes, especially between leaving the origin country and arriving at the destination. Domestic parcels that go more than 3 or 4 business days without a scan, or international parcels silent for more than 2 weeks, are worth raising with the seller.

## Common reasons tracking stops

- In the air or at sea: nothing scans the parcel until it is unloaded.
- In customs: inspection and clearance can take days and are often shown as a single event.
- Handover between carriers: international parcels are often passed to a local carrier, and the new carrier may use a different tracking number or start showing scans only after it receives the parcel.
- Weekends and holidays: many hubs do not scan on Sundays or public holidays.
- Label created, not shipped: the seller printed a label but has not handed the parcel over yet.

## How long is normal? Measured, not guessed

The honest way to answer "is this gap too long" is to look at parcels that *did* arrive and ask how quiet they went first. Across shipments tracked on 24hTrack over a 120-day window, taking the single longest stretch with no scan on each parcel that was eventually delivered:

| Longest silent gap reached | Share of delivered parcels |
|---|---|
| 3 days or more | 58% |
| 5 days or more | 44% |
| 7 days or more (a full week) | 27% |
| 10 days or more | 11% |
| 14 days or more | 4% |

Median: about 4 days. 90th percentile: about 10 days.

Read that the other way round: **more than one in four parcels that arrived perfectly fine went a whole week with no tracking update.** A quiet page is the normal state of a parcel, not a warning.

### By carrier

Same measurement, split by carrier — the median longest silence on parcels that were delivered, and the value 9 out of 10 stayed under. Full dataset: [`data/silent-gap-by-carrier.csv`](../data/silent-gap-by-carrier.csv) ([JSON](../data/silent-gap-by-carrier.json)), CC BY 4.0.

| Carrier | Median longest gap | 9 in 10 under |
|---|---|---|
| Rayspeed Asia | 1.0 days | 2.6 days |
| FedEx | 2.1 days | 19.4 days |
| Cainiao | 2.7 days | 9.9 days |
| FXYL | 2.9 days | 4.1 days |
| UPS | 3.0 days | 10.0 days |
| Yanwen Express | 3.2 days | 10.1 days |
| YunExpress | 3.5 days | 8.4 days |
| China Post | 3.9 days | 9.5 days |
| USPS | 4.6 days | 10.2 days |
| UniUni | 6.3 days | 12.5 days |
| CTT Express | 11.0 days | 17.8 days |

These are tracking-visibility figures, not service quality: a carrier that scans a parcel at more points along the route shows shorter gaps even when the total journey is the same length. Shipments tracked on a tracking site also skew towards journeys that worried somebody, so treat them as a picture of what people look up rather than a carrier league table.

## How long is normal?

On 24hTrack data for shipments tracked between March and August 2026, the median time from first scan to delivery was 4.0 days for UPS, 9.4 days for USPS, 11.0 days for China Post, 12.9 days for Yanwen Express and 13.3 days for YunExpress. These figures include many cross-border parcels whose first scan happens in the origin country, so a purely domestic parcel is usually faster. Long quiet gaps on China-to-US or China-to-Europe routes are therefore expected, while a domestic UPS parcel silent for a week is not.

Full figures by carrier, including the 80th percentile, are on the carrier statistics page: www.24htrack.com/carrier-statistics.

## What to do

- Open the full scan history to see the last place and date, not just the status.
- Check whether a new carrier name appears in the last scans. If so, track the parcel with the destination carrier too.
- On 24hTrack, save the number to a free account so it is checked automatically and you get an alert as soon as it moves.
- If the gap is well beyond the typical time for the route, send the seller the tracking number and the date of the last scan.

## FAQ

### How long can a package go without a tracking update?

Domestic parcels usually update every 1 to 2 days. International parcels can go 3 to 7 days, sometimes longer, without a scan while in the air, at sea or in customs.

### Does no tracking update mean my package is lost?

Usually not. Most quiet parcels are between scan points. It is worth contacting the seller when the silence is much longer than normal for the route, for example more than 2 weeks on an international shipment.

### How do I get notified when tracking finally updates?

Save the number to a free 24hTrack account. It is checked automatically and you receive app or browser alerts when the status changes.

---

Maintained by [24hTrack](https://www.24htrack.com) — free package tracking for 3,200+ carriers.
