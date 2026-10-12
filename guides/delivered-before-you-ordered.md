# "Delivered" on a Date Before You Ordered: Why a Stranger's Delivery Shows Under Your Number

**Short answer:** compare the date on the *Delivered* scan with the date you placed your order. If the delivery happened **before** you ordered, that scan is not your parcel — the tracking number is being shown with history from a previous use, and your own shipment simply has no scans yet.

## The ten-second test

1. Find the date on the Delivered line.
2. Find the date you placed your order.
3. Delivery date earlier than order date → it is not your parcel. Stop reading the city.

The town is the part that alarms people, and it is the part that tells you nothing. The date is the proof.

## Why a tracking number can carry someone else's trip

A tracking number looks personal — long, unique, printed on your own label. It is not a name. It is a string in a fixed format with a finite number of combinations, issued at enormous volume.

US postal numbers, for example, are 22 digits beginning with 9 (most often 92 or 94). That single shape covers about **96%** of the USPS numbers seen on the 24hTrack platform. A format that rigid, at that volume, means strings get reissued.

The second half of the explanation is **retention**, and it is the part almost nobody is told.

USPS states on its own help pages:

> "Currently, access to tracking information for non-signature items is limited to 120 days. Tracking information for signature items is available for 2 years."

So if the carrier's own system only holds ordinary parcel history for roughly four months, a *Delivered* line from seven months ago is **not coming from the carrier's live record**. It is coming from whichever site you are looking at, out of a copy that site saved at the time and never cleared.

## Why two tracking sites disagree about one parcel

This is the same fact seen from the other side, and it is why a second opinion makes things worse instead of better.

- One site asks the carrier **now** and finds nothing yet, because your label exists but nobody has physically scanned your box into the network.
- The other site shows what it **stored months ago**, when the number was in use by someone else.

Neither is lying. One of them is old. When a carrier's own website says *tracking not available* while a third-party page shows a delivery from last spring, the blank answer is the one describing today.

## What not to do

- **Do not report a theft.** The delivery you are reading happened to another person, in another place, months ago. A claim built on that scan describes an event with no connection to your order.
- **Do not open a refund dispute using it as evidence.** You would be arguing about a parcel that genuinely was delivered — just not yours.
- **Do not accuse the seller of shipping to the wrong address.** That address was never on your order.

## What actually helps

- Check the **carrier's own website** for the same number and note exactly what it says. "Nothing yet" is information, not failure.
- Ask the seller for the **acceptance scan** — the moment the carrier physically took the parcel. That is the first event that is genuinely yours, and sellers can often see it when buyers cannot.
- Watch for the **first scan dated after your order**. The moment one appears, the stale history stops mattering: the number is narrating your trip now.

## How often does this happen?

Measured on the 24hTrack platform: of the tracking numbers added over the last two months, roughly **1 in 500** had its newest scan dated more than two months before the number ever reached the platform.

It is rare. It is also, every time, a buyer who believes their parcel was handed to a stranger in another state — which is exactly why nobody recognises the pattern when it happens to them.

## For developers

If you ingest carrier events keyed on the tracking number, your own database reproduces this. Guard it by comparing each event date against the moment the shipment entered your system, and refusing to promote anything meaningfully older:

```js
const STALE_DAYS = 30;

function partitionEvents(events, anchorISO, staleDays = STALE_DAYS) {
  const cutoff = new Date(new Date(anchorISO).getTime() - staleDays * 864e5);
  const current = [], priorUse = [];
  for (const e of events) {
    const cleaned = String(e.date || '').replace(/\[[^\]]*\]/g, '').trim().replace(' ', 'T');
    const d = new Date(cleaned);
    if (Number.isNaN(d.getTime())) { current.push(e); continue; } // never hide what you failed to parse
    (d < cutoff ? priorUse : current).push(e);
  }
  return { current, priorUse };
}
```

Two rules worth keeping: **fail open** (an unparseable date must not delete a customer's history), and **keep the old events** — partition and label them rather than deleting, so the customer can see that the earlier history is not theirs.

## Related

- [Why is my tracking not updating?](tracking-not-updating.md)
- [Another site shows a different scan — who's wrong?](tracking-sites-disagree.md)
- [Stuck on "Label Created" / "Info Received"](label-created-info-received.md)
- [Package says delivered but not received](package-delivered-but-not-received.md)

---

*Data from the [24hTrack](https://www.24htrack.com) platform. Retention figures quoted from USPS's own help pages. Text: CC BY 4.0.*
