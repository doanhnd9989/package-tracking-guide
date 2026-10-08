# Why Two Tracking Sites Disagree About the Same Parcel

A customer sends a screenshot: another tracking site already shows a scan that yours does not have. Who is wrong?

Usually neither. There are four separate reasons two pages can legitimately differ, and three of them are about how parcels move, not about data quality.

## 1. Every tracking page is a copy

The carrier is the only writer. Every tracking page — the carrier's own site, a marketplace order page, any universal tracker — is a copy of what the carrier had published at the moment that copy was made. Two copies made minutes apart can disagree, and neither is lying.

Practical consequence: the useful thing to show a customer is **when you last checked**, next to the status. That answers the question they are actually asking ("is this stale?").

## 2. One shipment is often two or more numbers

On a cross-border order, one company carries the parcel out of the country it was posted in, and the postal carrier where the buyer lives delivers it — frequently under a second, local number the first carrier never sees.

The handover is visible in the data. Typical international postal sequence:

```
Export customs clearance started
Departure from office of exchange
Left from departure country/region
Arrival in the country of destination
```

After `Arrival in the country of destination`, the original number often goes quiet permanently. That is not a failure — the parcel simply stopped being that carrier's to move. A site showing a "newer" line may be showing the second leg.

## 3. The last two letters are the issuing country

International postal numbers use the S10 format: two letters, nine digits, two letters. **The trailing pair identifies the postal operator that issued the number — not the destination.**

| Suffix | Issued in | Means the parcel is going to… |
|---|---|---|
| `CA` | Canada | anywhere |
| `BE` | Belgium | anywhere |
| `IE` | Ireland | anywhere |
| `NL` | Netherlands | anywhere |
| `GB` | United Kingdom | anywhere |

A buyer in Spain holding a number ending `BE` bought from a seller who posted it in Belgium. Nothing is wrong.

This matters in code too: naming the field `country` or `destination` instead of `issuedBy` produces real routing and support bugs.

## 4. One carrier can have more than one number format

Length-based validation is the most common way a valid number gets rejected. Canada Post publishes two formats on its own support pages:

| Format | Used for |
|---|---|
| 16 digits, no letters | items delivered inside Canada |
| 13 characters (S10) | items to the US and internationally, plus prepaid envelopes and labels |

Both are valid Canada Post numbers. A form that accepts only 16 digits rejects every international and prepaid-label customer.

## Quiet gaps are normal, and measurable

Nothing is scanned while a parcel is in the air or waiting in a customs queue, so there is genuinely nothing to publish. Measured on the 24hTrack platform:

| Carrier | Typical longest quiet gap | Share going a full week with no scan |
|---|---|---|
| Canada Post | about 4 days | about 1 in 6 |
| bpost (Belgium) | about 7 days | about half |
| An Post (Ireland) | about 11 days | about two thirds |

If your alerting treats "no movement for 7 days" as an exception, it will fire on perfectly healthy international orders.

## What to do, in order

1. **Read the newest line, not the timestamp.** The words tell you which leg the parcel is on.
2. **If the newest line is the sender's electronic notice** ("Electronic information submitted by shipper", "We have received information about your incoming item from the sender"), the carrier does not have the parcel yet. Chase the shop.
3. **If it shows arrival in your country**, your own postal service is holding it. They are who can answer.
4. **If it says delivered and nothing arrived**, check a mailbox, locker or safe spot and any card first. Lines like "Delivered to your community mailbox, parcel locker or apt./condo mailbox" (Canada Post) and "delivered to your safe spot" (An Post) are completed deliveries, just not into your hands.

## See also

- [Parcel arrived in your country](parcel-arrived-in-your-country.md)
- [International parcel journey explained](international-parcel-journey-explained.md)
- [Label created / info received](label-created-info-received.md)
- [Package delivered but not received](package-delivered-but-not-received.md)

---

Figures are medians and shares measured on the [24hTrack](https://www.24htrack.com) platform. Canada Post number formats come from Canada Post's published support pages. Licensed CC BY.
