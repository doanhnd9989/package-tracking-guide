# Package Tracking Guide

An open reference on parcel tracking: how to track any package, what tracking numbers look like, what each status means, what to do when a parcel is late, lost or marked delivered but missing, and how long common carriers actually take.

Maintained by [24hTrack](https://www.24htrack.com), a free multi-carrier package tracker covering 3,200+ carriers. Paste any tracking number at [www.24htrack.com](https://www.24htrack.com) and the carrier is detected automatically — no account needed.

## Quick answers

- **Track a package without knowing the carrier:** paste the number into a universal tracker such as [24hTrack](https://www.24htrack.com); it detects the carrier from the number. → [guide](guides/how-to-track-a-package.md)
- **The carrier's name is spelled several ways (OnTrac / "on trac", Cainiao / "cai niao", YTO / Yuantong):** one company can have several correct names; the tracking number is the stable identifier, not the name. → [guide](guides/carrier-name-spellings.md)
- **Delivered but not received:** check neighbors, mailroom and lockers, wait until the end of the next day, then contact the seller. → [guide](guides/package-delivered-but-not-received.md)
- **The seller says they don't know either:** they see the same scans you do, but they hold the shipping contract — ask them to open an investigation, not for an update. Read the *type* of the last scan (origin country, customs, local depot, handover) to know whether the silence is ordinary. → [guide](guides/tracking-not-updating.md)
- **Tracking not updating:** the parcel is usually between scan points (flight, customs, hub). Measured on parcels that were eventually delivered, the longest silent gap ran to a median of ~4 days and **more than 1 in 4 went a full week with no scan**. → [guide](guides/tracking-not-updating.md)
- **Parcel looks like it's going in circles:** cross-border parcels average ~18–22 scans against 4–5 domestic, and two or three airport hubs is normal routing. → [guide](guides/international-parcel-journey-explained.md)
- **Stuck on "Label Created" / "Info Received":** the carrier has the parcel's data, not the box; USPS median ~1 day to the first real scan, 80% within ~3 days. → [guide](guides/label-created-info-received.md)
- **It arrived in my country — who delivers it now?** A local courier takes the last leg; the exporter's number usually keeps publishing its scans, and once the final transit scan appears, delivery follows within about 5–8 hours for most networks. → [guide](guides/parcel-arrived-in-your-country.md)
- **"Delivery attempted" but you were home:** the scan records a parcel going back on the van, not a claim that you were out — the commonest recorded reason is no access to the building. **82% were delivered anyway**, 44% within 24 hours and 89% within a week. → [guide](guides/delivery-attempted-what-it-means.md)
- **Amazon number starting TBA says "not found":** it is a reference issued inside Amazon's own network and tied to the order, not a public carrier barcode — about 96% of Amazon Shipping references take that form. Track it in Your Orders. → [guide](guides/amazon-tba-tracking-number.md)
- **Who do I contact — seller, carrier or the tracking site?** The seller bought the shipping, so the contract and nearly every remedy sit with them; carriers usually will not open a claim for a recipient. → [guide](guides/who-to-contact-parcel-problem.md)
- **"Out for delivery" for days:** the scan normally means today (median **about 6 hours** to delivery) and only **about 1 parcel in 20 runs past 24 hours**, with roughly **1 in 40 getting a second out-for-delivery scan** - a failed attempt hiding under the same headline. Per carrier it varies hugely: ~4% of USPS parcels are still out after a day, against ~65% on the slowest cross-border lane in the set. → [guide](guides/out-for-delivery-for-days.md)
- **My tracking is in Chinese:** 已收寄 = accepted · 离开/到达处理中心 = left/arrived at a sorting centre · 等待清关 = awaiting customs · 出门投递 / 派送中 = out for delivery · 已妥投 / 已签收 = delivered · 查询不到 = no record for that number. → [guide](guides/chinese-tracking-scan-meanings.md)
- **"Delivered at 21:49" but nothing arrived:** the time on a scan is the carrier's own wall clock where the scan happened, and pages that convert it to your timezone show a time nobody published; **about 1 in 11 delivery scans falls between 8pm and 6am** and **~4% carry no time at all**. Read the scan *location*, not the minute. → [guide](guides/delivery-scan-time-meaning.md)
- **The tracking site printed on my parcel is gone:** couriers get sold and renamed and the old portal dies with the brand — a rename never invalidates your number. MyToll is the live example: checked 3 October 2026 it returns no page, and the portal is now myteamge.com (Toll Global Express → Team Global Express, 2022). → [guide](guides/carrier-renamed-dead-tracking-site.md)
- **Which carrier is this number?** 1Z = UPS · 20–22 digits starting 92–95 = USPS · 12/15 digits = often FedEx · 2 letters + 9 digits + country code = international post. → [guide](guides/tracking-number-formats.md)
- **Why is my 1Z number "invalid"?** The last character of a UPS number is a check digit, so one mistyped character usually breaks the whole number. → [guide](guides/ups-1z-number-decoded.md)
- **Never heard of the carrier on my parcel — who are they?** On a cross-border order the seller picks the carrier, so the name is often a business-to-business shipper that never advertises to shoppers. Search the number, not the name: some courier names are shared by two different companies (CTT is the Portuguese post; CTT Express is a Spanish courier). → [guide](guides/carrier-name-collisions.md)

- **The shop says "shipped and tracked" but no site finds the number:** a marketplace marks an order shipped when the *seller* says so, and whatever reference the seller uploads becomes "the tracking number" — sometimes a warehouse code no carrier ever had. Check the shape, check whether it ever produced one scan, then ask the seller three narrow questions. → [guide](guides/order-number-vs-tracking-number.md)
- **The carrier's site has no box called "tracking number":** several use another word — Purolator says *PIN or Reference*, US freight says *PRO*, air cargo says *AWB*, Australian freight says *consignment*. Right number in the wrong box returns "not found". → [guide](guides/order-number-vs-tracking-number.md)
- **A courier is asking for cash at the door:** that's cash on delivery, normal across the Gulf, much of Africa and South-East Asia — match the amount against your order confirmation, pay the courier (never a link or QR code), and refuse if it matches nothing you bought. → [guide](guides/cash-on-delivery-parcel.md)

## Guides

- [Seller, carrier or tracking site: who actually fixes a parcel problem](guides/who-to-contact-parcel-problem.md)
- [How to Track Any Package, Even If You Don't Know the Carrier](guides/how-to-track-a-package.md) — Track a package from any carrier with just the tracking number. How carrier detection works, where to find your number, and what to do when nothing shows up.
- [Package Says Delivered but Not Received: What to Do](guides/package-delivered-but-not-received.md) — Tracking says delivered but you have nothing? Check these places first, then follow the steps that actually get a missing parcel found or refunded.
- [Why Is My Tracking Not Updating? Causes and How Long to Wait](guides/tracking-not-updating.md) — Tracking stuck for days? The usual reasons a parcel stops updating, typical gaps by route, and when a quiet tracking page actually means a problem.
- [Tracking Number Formats: How to Tell Which Carrier a Number Belongs To](guides/tracking-number-formats.md) — What UPS, USPS, FedEx, DHL, Amazon and international postal tracking numbers look like, and why some shapes are shared by several carriers.
- [The UPS 1Z Number, Decoded (and Why Typos Fail the Maths)](guides/ups-1z-number-decoded.md) — What each part of a 1Z number means, the check digit that catches typos (verified on 1,539 real numbers), and when a UPS parcel does not carry a 1Z number at all.
- [The Tracking Site on Your Label Is Gone: tracking a carrier that renamed](guides/carrier-renamed-dead-tracking-site.md) — Why a tracking portal can simply stop existing, the Toll → Team Global Express example with dates and the number format, and what to do when the site on your label returns nothing.
- [Carrier Name Collisions: When Two Couriers Share a Name](guides/carrier-name-collisions.md) — Why the carrier on your parcel is a company you have never heard of, the name traps that send you to the wrong tracking page, and why a second carrier usually appears near the end.
- [One Carrier, Several Spellings: OnTrac, Cainiao, Straightship, YTO](guides/carrier-name-spellings.md) — why "on trac", "cai niao" and "yuan tong" all find the right company, which of the four has a reliable number shape, and why the name on the label is not the identifier.
- ["Delivered at 21:49" — What the Time on a Delivery Scan Actually Means](guides/delivery-scan-time-meaning.md) — Why the timestamp is the carrier’s clock and not yours, how often deliveries really are scanned at night, the scans that carry no time at all, and the field worth reading instead.
- [Tracking Status Meanings: In Transit, Out for Delivery, Exception and More](guides/tracking-status-meanings.md) — What every common tracking status means in plain English, from Label Created and In Transit to Exception, Held at Customs and Return to Sender.
- ["Label Created" / "Info Received": What It Means and How Long It Lasts](guides/label-created-info-received.md) — Why a parcel sits on its first status, real label-to-first-scan times for USPS and a cross-border carrier, and when it is worth contacting the sender.
- [How to Track Packages from China (AliExpress, Temu, Shein and More)](guides/track-packages-from-china.md) — Track parcels shipped from China across both legs of the journey: which carriers are involved, why the number changes, and how long it usually takes.
- [Package Held at Customs: What It Means and What to Do](guides/package-held-at-customs.md) — Why international parcels get held at customs, how long clearance usually takes, and what to do if duties, documents or an ID are needed.
- [Why Your International Parcel Looks Like It's Going in Circles](guides/international-parcel-journey-explained.md) — Every leg of a cross-border journey explained, why twenty tracking scans is a good sign, why the trail dies at the local-courier handover, and how to use median vs 80th-percentile transit times to tell "slow but normal" from "worth chasing".
- [Lost Package? How to Find It or Get Your Money Back](guides/lost-package-what-to-do.md) — When a parcel is really lost, how to confirm it, who to contact first, which claim deadlines matter, and how buyer protection works.
- [How to Track Multiple Packages at Once (Bulk Tracking)](guides/track-multiple-packages-at-once.md) — Track dozens or thousands of parcels across different carriers at once: pasting lists, spreadsheet import, Google Sheets sync and API options compared.
- [How to Track Packages in Google Sheets Automatically](guides/track-packages-in-google-sheets.md) — Put tracking numbers in a Google Sheet and have delivery statuses written back automatically, for every carrier, without formulas or Zapier.
- [Your Parcel Arrived in Your Country — Who Delivers It Now?](guides/parcel-arrived-in-your-country.md) — What "arrived at transit node, awaiting distribution" means, why one order has two tracking numbers with two different clocks, whether the original number keeps updating after the handover, and how long it takes from the last transit scan to your door.
- ["Delivery Attempted" — What It Actually Records, and What Happens Next](guides/delivery-attempted-what-it-means.md) — What a failed-delivery scan really means, the reason that shows up more than any other, how long parcels actually take to arrive after one, how often a second attempt happens, and the four phrases that mean you must act today.
- ["Out for Delivery" for Days: What That Status Actually Promises](guides/out-for-delivery-for-days.md) — What the scan really promises, per-carrier dwell times showing the same three words mean different things, the failed attempt hiding under an unchanged status, and when to stop waiting.
- [Chinese Tracking Scans: What 已妥投, 离开处理中心 and the Rest Actually Mean](guides/chinese-tracking-scan-meanings.md) — A glossary of the Chinese scan phrases that appear on parcels shipped from China, in the order you meet them, plus how to read the silence between them and what to do when 已妥投 appears and nothing arrived.
- [Amazon Tracking Numbers: Why "TBA…" Says Not Found Everywhere Else](guides/amazon-tba-tracking-number.md) — What a TBA reference actually is, why third-party trackers cannot resolve it, the other shapes that appear on Amazon orders and where each one can be tracked, and why an Amazon van can deliver a parcel from a shop with no Amazon connection.
- [The Driver Wants Cash: telling a real cash-on-delivery parcel from a scam](guides/cash-on-delivery-parcel.md) — What COD actually is and which markets use it, the four signs the person at your door is not delivering your order, why customs duty is a separate bill, and why no tracking page can tell you the amount you owe.
- ["Shipped and Tracked" but No Site Finds the Number](guides/order-number-vs-tracking-number.md) — Why a marketplace can say tracked when no carrier recognises the number, three checks that tell an order code from a carrier number in about a minute, the three things it usually turns out to be, and the carriers that accept a shipper reference on purpose.
- [Package Tracking API: How to Add Multi-Carrier Tracking to Your App or AI Agent](guides/package-tracking-api.md) — What to look for in a multi-carrier tracking API, how register-and-webhook tracking works, and how to give AI assistants tracking access through MCP.

## Data: how long parcels go without a scan

[`data/silent-gap-by-carrier.csv`](data/silent-gap-by-carrier.csv) / [`.json`](data/silent-gap-by-carrier.json) give the longest stretch with no carrier scan, measured per parcel on shipments that were eventually delivered and tracked on 24hTrack over a 120-day window ending 2026-09-23 — median and 90th percentile, overall and per carrier. Overall: median ~4.1 days, 90th percentile ~10.3 days; 58% of delivered parcels went 3+ days with no scan, 27% went a full week, 4% went two weeks. Percentiles and shares only. CC BY 4.0.

## Data: the final leg

[`data/final-leg-by-carrier.csv`](data/final-leg-by-carrier.csv) / [`.json`](data/final-leg-by-carrier.json) give the time from the **last transit scan to the delivery scan**, plus the median number of scans published per shipment, measured on delivered parcels tracked on 24hTrack over 120 days to 2026-09-24. Most of the waiting on an international order happens before that final scan, not after it: USPS runs a median of ~5 hours from it to the door, China Post, Cainiao and 4PX about 8 hours. The scan counts show the other half of the story — a cross-border number publishes a median of 17–20 events against about 7 for a domestic parcel, because it keeps reporting through the handover. Percentiles and medians only. CC BY 4.0.

## Data: what happens after a failed delivery attempt

[`data/delivery-attempt-outcomes.csv`](data/delivery-attempt-outcomes.csv) / [`.json`](data/delivery-attempt-outcomes.json) measure what follows a *delivery attempted* / failed-delivery scan: the share of those parcels that were still delivered, and how long the delivery took after that scan. Only parcels whose first attempt scan is at least 14 days old are counted, so the outcome is settled. Overall: **82% were delivered in the end**, a median of about 27 hours after the attempt — 44% within 24 hours, 65% within 48, 89% within a week. Only 22% ever show a second attempt scan and 9% a third. Domestic carriers retry fastest (DHL and USPS about a day); cross-border routes take longer because an attempt is often followed by a handover to a local company rather than a retry. Shares and percentiles only. CC BY 4.0. Measured 2026-09-25.

## Data: how long "out for delivery" actually lasts

[`data/out-for-delivery-dwell.csv`](data/out-for-delivery-dwell.csv) · [JSON](data/out-for-delivery-dwell.json) — hours from the first out-for-delivery scan to the delivery scan, per carrier, delivered parcels only. Overall median 6.5h; 16.7% are still out after 24 hours; 14.3% receive a second out-for-delivery scan. One cross-border carrier posts the scan so early that 65% of its parcels are still out at 24 hours. CC BY 4.0.

## Data: carrier transit times

[`data/carrier-transit-times.csv`](data/carrier-transit-times.csv) and [`.json`](data/carrier-transit-times.json) list the median and 80th-percentile time from the first carrier scan to delivery, plus the average number of tracking events per shipment, for shipments tracked on 24hTrack between 2026-03-20 and 2026-08-19. Many shipments are cross-border, so the clock often starts in the origin country; purely domestic parcels are usually faster. Live version: [www.24htrack.com/carrier-statistics](https://www.24htrack.com/carrier-statistics).

| Carrier | Median days | 80th percentile days | Avg. tracking events |
|---|---|---|---|
| TIPSA | 2.9 | 7.3 | 5.2
 |
| UPS | 4.0 | 10.0 | 4.8
 |
| Royal Mail | 4.2 | 14.3 | 4.4
 |
| Austrian Post | 5.4 | 12.9 | 8.1
 |
| DHL | 5.8 | 11.1 | 16.2
 |
| Cainiao | 7.2 | 12.1 | 18.1
 |
| Evri | 7.2 | 13.1 | 8.5
 |
| GOFO | 7.9 | 12.9 | 10.6
 |
| GoFo Express | 8.4 | 16.4 | 15.9
 |
| GLY | 9.1 | 12.2 | 20.2
 |
| USPS | 9.4 | 12.7 | 10.2
 |
| China Post | 11.0 | 17.8 | 21.6
 |
| UniUni | 11.0 | 17.5 | 7.2
 |
| SPT | 11.9 | 15.9 | 16.6
 |
| CTT Express | 12.0 | 16.6 | 2.9
 |
| AliExpress | 12.4 | 16.3 | 17.4
 |
| Yanwen Express | 12.9 | 29.3 | 18.8
 |
| YFH | 13.0 | 16.4 | 17.3
 |
| YunExpress | 13.3 | 19.0 | 15.4
 |
| 1ST | 16.7 | 17.7 | 19.3
 |
| ShopLine | 16.7 | 23.6 | 18.1
 |
| FXYL | 22.8 | 26.8 | 10.8
 |
| DZTGJ | 23.6 | 23.8 | 11.3
 |
| chengxiao | 29.8 | 30.1 | 7.4
 |

## Tools

- **Web:** [www.24htrack.com](https://www.24htrack.com) — free tracking, no account; free account saves 140 packages with alerts and free Google Sheets sync.
- **API:** REST API with webhooks — [docs](https://www.24htrack.com/api).
- **AI agents:** MCP server [`24htrack-mcp`](https://www.npmjs.com/package/24htrack-mcp) for Claude, Cursor and other MCP clients.

## License

Text: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Data: CC BY 4.0 — please credit "24hTrack (www.24htrack.com)".
