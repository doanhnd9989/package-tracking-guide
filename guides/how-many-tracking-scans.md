# Three Scans or Twenty-Five? What the Number of Tracking Updates Means

**Short answer:** the number of lines on your tracking page is a count of *handovers*, not a score.
It does not measure speed, quality, or how close the parcel is to your door. A four-scan parcel is
often a one-day domestic trip; a twenty-five-scan parcel is usually a long international relay. The
only number worth reading is the **age of the newest scan**.

---

## What a scan actually is

Every line exists because something physically handled the parcel and logged it: arrived at a
facility, departed a facility, cleared customs, loaded on a vehicle, out for delivery, delivered.

Nobody writes a scan because time passed. They write one because the parcel changed hands. So the
count on your page answers exactly one question — *how many separate operations touched this
parcel* — and nothing else.

## Measured scan counts, by shipping model

Average tracking events per parcel, measured on parcels tracked on the 24hTrack platform over a
90-day window ending 2026-10-19:

| Shipping model | Example lane | Avg. scans | Median days to delivered | 80% within |
|---|---|---|---|---|
| Local warehouse, domestic leg only | Shenzhen forwarder with EU/US warehouses | ~6 | 1 | 3 days |
| Regional parcel carrier, one country | Iberian domestic carrier | ~4 | — | — |
| Cross-border, forwarder hands to local post | China → US/EU economy air | ~12 | ~22 | — |
| Cross-border, operator runs its own local network | China → Africa | ~18 | 12 | 16 days |
| Cross-border with regional hub handover | China → US via regional hub | ~17 | 10 | 17 days |
| Cross-border, densest reporting | China → US, multi-hub | ~25 | 8 | 10 days |

Read the first and last rows together. The six-scan lane delivers in a **median of one day**. The
twenty-five-scan lane takes **eight**. More scans did not mean slower, and fewer scans did not mean
broken — they describe different journeys, not different service quality.

Two things follow:

1. **A short list is usually a short journey.** No flight, no customs entry, no international
   handover means there is simply less to report.
2. **A long list is usually a long relay, reporting honestly.** A carrier that publishes twenty
   events is telling you more, not performing worse.

## Why the gaps are not missing scans

If scans mark handovers, silence marks the stretches where nothing changes hands. The two long
quiet periods on a cross-border parcel are **the flight** and **the customs queue**. A plane does
not scan your box hourly; a customs officer does not log each day it waits.

Across delivered parcels, the median longest silent stretch is about **4 days**, and the 90th
percentile is about **10** — 58% of parcels go three or more days with no scan at all, and 27% go a
full week. See [`data/silent-gap-by-carrier.csv`](../data/silent-gap-by-carrier.csv).

A multi-day gap in the middle of an international timeline is the single most common reason people
believe a parcel is lost, and it is normal.

## When the company name changes partway down

On a lot of cross-border timelines the company name changes near the end. A forwarder flies the
parcel in, then later scans read as your national postal service or a regional delivery hub you
have never heard of.

That is the **handover**, and it almost always sits right after the customs line. Examples visible
in real scan text:

- A Shenzhen air-lane forwarder whose US parcels finish on USPS facility scans and end with
  "Delivered, In/At Mailbox".
- A Chinese fulfilment provider whose US parcels pass through a named regional hub —
  arrived, departed, loaded on vehicle, out for delivery.
- An operator with its own African networks that *does* deliver, but where "delivered" frequently
  means **collected from a named pickup site**, not handed over at your address.

It is the same parcel. See
[handover-scan-delivered-to-carrier.md](handover-scan-delivered-to-carrier.md).

## What to read instead of the count

Three questions settle almost every case:

1. **What does the newest scan say**, in plain words?
2. **Where did it happen** — is that place closer to you than the one before it?
3. **How old is it?**

A two-day-old scan on a parcel crossing an ocean is fine. A two-week-old scan on a parcel already in
your own city is not.

## A practical rule for when to chase

| What you see | What it means | What to do |
|---|---|---|
| Newest scan is a customs line | The slowest, most variable step | Give it longer; check for a duty request |
| Newest scan is in your country, 7+ days old | The local leg has stalled | Chase it — contact the seller, who holds the contract |
| Newest scan says "delivered" but nothing arrived | May be a handover or a pickup point | Read the scan location before assuming loss |
| **No scan has ever appeared** | Label exists, parcel not handed over | Ask the shop for the collection date |

That last row is not a carrier problem. The shop holds the shipping contract with the carrier — you
do not.

## One number, the whole chain

Many carrier websites only show their own leg, so a parcel that changed hands looks like it stopped
at the border. A universal tracker such as [24hTrack](https://www.24htrack.com) detects the carrier
from the number and shows the whole chain, including the handover scans, free and without a
sign-up — which is the difference between a timeline that looks like it died at customs and one
that shows the local hub that picked it up.

## Related guides

- [Why Your International Parcel Looks Like It's Going in Circles](international-parcel-journey-explained.md)
- [Why Is My Tracking Not Updating?](tracking-not-updating.md)
- [Why a Tracking Page Comes Back Blank](why-tracking-page-is-blank.md)
- ["Delivered to final mile carrier": the handover scan](handover-scan-delivered-to-carrier.md)
- [Ordered from China, but tracking only shows local cities](overseas-warehouse-tracking.md)
