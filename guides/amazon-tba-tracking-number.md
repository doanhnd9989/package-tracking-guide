# Amazon Tracking Numbers: Why "TBA…" Says Not Found Everywhere Else

**Short answer:** a number beginning **TBA** is a reference issued inside Amazon's own delivery
network and tied to the order it belongs to. It is not a public carrier barcode, so third-party
tracking sites generally cannot resolve it — and there is nothing wrong with your number. Track it
in **Your Orders** or at track.amazon.com. If your Amazon order shows a different shape — `1Z…`, a
22-digit number, or a cross-border code — then another carrier is completing the delivery, and that
one *can* be tracked anywhere.

---

## The shapes, and what each one means

| What you see | Who is carrying it | Where it can be tracked |
|---|---|---|
| `TBA` + 12 digits | Amazon's own delivery network | Your Orders / track.amazon.com |
| `TBC` + 12 digits | Same, smaller group | Your Orders / track.amazon.com |
| `UK4` + 8 digits | Amazon Shipping UK | Your Orders; some universal trackers |
| `1Z` + 16 characters | UPS | Any universal tracker |
| 22 digits starting `9` | USPS | Any universal tracker |
| `YT…`, `LP…CN`, `4PX…` | A cross-border carrier | Any universal tracker |

Among references labelled **Amazon Shipping** on the 24hTrack platform, about **96% begin with
TBA** and a further ~2% with TBC — so the TBA case is the norm, not an edge case. Amazon Shipping
UK is a separate set: **99% of those start `UK4`** followed by eight digits.

## Why a TBA cannot be looked up elsewhere

Public carrier barcodes are designed to be scanned and queried by anyone in the chain — that is what
makes a UPS or USPS number work on any tracking site. A TBA reference is not that. It is created
inside Amazon's network, keyed to the order, and Amazon's own tracking page asks for the tracking ID
directly rather than publishing it as a lookup-able barcode.

So the sequence people hit — paste into tracking site → "not found" → assume the number is fake or
the site is broken — has a third explanation that is almost always the right one: the number is
real, and it belongs to exactly one system.

## The confusing part: an Amazon van, a non-Amazon shop

Amazon Shipping is a service Amazon sells **to businesses** so they can ship their own orders over
Amazon's logistics network — including orders placed on the seller's own website or on a different
marketplace. The van at your door is that same network.

Two consequences that surprise people:

- A parcel can arrive on an Amazon vehicle from a shop with **no Amazon connection at all**.
- A `TBA` number can appear on an order you did **not** place through Amazon. In that case Your
  Orders will not show it either — the shop that sold you the item is the one holding the record.

## What to do, by situation

**Your number starts with TBA or TBC.** Open Your Orders, choose the order, select Track package.
That is the only route that resolves it. If you bought from a non-Amazon shop, ask that shop.

**Your number is a 1Z, a 22-digit number, or a cross-border code.** Another carrier is doing the
delivery. Paste it into any universal tracker — for example
[24hTrack](https://www.24htrack.com), which detects the carrier from the number itself across
3,200+ carriers, free and with no sign-up.

**It says delivered and it is not there.** Give it 24 to 48 hours. Drivers sometimes mark a parcel
delivered slightly ahead of the drop, and it may be with a neighbour, behind a gate, or in a
building's mail room. A delivery photo, when one exists, usually shows where it was left. If it
still has not appeared, raise it with Amazon — Amazon holds the delivery record for these
shipments, and a tracking site cannot investigate or replace an order.

**It says delivery attempted.** Most attempted parcels arrive anyway, typically the next day — see
["Delivery Attempted" — What It Actually Records](delivery-attempted-what-it-means.md). For a TBA
parcel specifically, no third-party site can arrange a redelivery; Your Orders is the route.

## What no tracking site can do — for any carrier

Worth stating plainly, because it saves a lot of wasted messages:

- It cannot contact the driver or the local delivery station.
- It cannot see or change your delivery address.
- It cannot arrange a redelivery or release a held parcel.
- It cannot open a claim. The **seller** bought the shipping, so the seller is the party that can.

A tracking site shows you every scan the carrier publishes, in one place and one format. That is
the whole job.

## FAQ

**Why does my Amazon tracking number not work on tracking sites?**
Because a reference beginning TBA is not a public carrier barcode. It is issued inside Amazon's
delivery network and tied to your order, so third-party trackers generally cannot resolve it.
Nothing is wrong with the number.

**What does an Amazon tracking number look like?**
Most commonly the letters TBA followed by 12 digits; about 96% of Amazon Shipping references we see
take that form, with a smaller group starting TBC. Amazon Shipping UK codes start UK4 plus eight
digits.

**Can I track an Amazon package without signing in?**
Yes, if you have the tracking ID — track.amazon.com asks only for the ID. Signing in to Your Orders
gives more detail, and it is the only route if you do not have the number to hand.

**My Amazon order shows a 1Z number. Is that normal?**
Yes. It means UPS is completing the delivery on Amazon's behalf, and UPS's own tracking — or any
universal tracker — will answer it.

**Is Amazon Shipping the same as the Amazon van that delivers to my house?**
They overlap without being the same thing. Amazon Shipping is the service Amazon sells to
businesses; the van is the network doing the delivery. That is why an Amazon vehicle can deliver a
parcel from a shop with no Amazon connection.

---

*Shape proportions measured on parcels tracked with [24hTrack](https://www.24htrack.com),
September 2026. Shares only — no parcel counts. Released under CC BY 4.0.*
