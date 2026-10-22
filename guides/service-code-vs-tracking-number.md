# The code you were given has no digits — that's a service name, not a tracking number

Some of the strings people try to track cannot possibly be tracking numbers, and you can tell in
two seconds without asking anyone.

Strings like `ASD-US-F`, `ASD-US-M`, `ePacket`, `Economy Delivery` or `Standard` are **service
codes**. They name the shipping product that was bought. The identical string sits on every single
parcel sent that way, so there is nothing for any tracking site to look up, and no carrier API
will ever resolve one. Every site will tell you "not found", and every site will be right.

This is common enough to show up in search traffic: people type service codes into search engines
expecting a tracking page, land somewhere, and leave no better off.

---

## The two-second test: count the digits

| What you're holding | Looks like | Verdict |
|---|---|---|
| A service / product code | Letters and hyphens, few or no digits — `ASD-US-F`, `ePacket` | Not trackable, ever |
| A shop order reference | Short, often prefixed — `ORD-77421`, `#10024` | Usually not trackable |
| A real tracking number | Mostly digits, normally 10–22 characters | Trackable |

A tracking number identifies **one physical parcel**, so it has to carry enough digits to be
unique across millions of them. A service code identifies a **tariff**, so it does not.

If the thing in your hand has **no digits at all**, stop looking for a tracking site that accepts
it. There isn't one.

---

## Three fields that travel together and get mixed up

A checkout, a warehouse system, a label API and a notification email all pass these around at the
same time:

- **service / product code** — the tariff that was purchased. A handful exist per carrier.
- **order reference** — identifies the order inside the shop's own database. One per order.
- **tracking number** — identifies one parcel in a carrier's network. One per parcel.

They are all short alphanumeric strings arriving in the same message, and an email template that
interpolates the wrong one still renders perfectly. That is why this reaches you looking official.

---

## What to do instead

1. **Go back to the shipping confirmation** and look for the longest, most digit-heavy string.
   That is the candidate.
2. **Check the shape against the carrier.** For example, Asendia USA numbers are typically 13
   characters — two letters, nine digits, two letters, usually starting `AS` and ending `US`.
   UPS is `1Z` plus 16 characters. A USPS domestic number is a long run of digits.
3. **If all you have is a service name, the parcel number never reached you.** The sender has it.
   Ask them for "the carrier tracking number", naming the carrier if you know it — that phrasing
   gets a better answer than "tracking info".
4. **Paste it without picking a carrier.** On [24hTrack](https://www.24htrack.com) the carrier is
   detected from the number itself, free and with no account, which matters when the parcel has
   been handled by a forwarder you have never heard of.

---

## A word about guessing

You will find pages confidently explaining what the trailing letter in a code like `ASD-US-F`
stands for. Carriers do not generally publish those mappings, and we are not going to invent one.
It does not matter for tracking anyway: whatever the letter means, the string still identifies a
service rather than your parcel.

---

## FAQ

**Can a service code ever be tracked?**
No. It describes a product, not a parcel, so there is nothing for it to resolve to.

**My order reference has digits in it. Is that trackable?**
Sometimes, which is why it is worth pasting. A few carriers accept a sender's reference as a
lookup key, occasionally paired with your postcode. If the carrier says it has no record, that is
a real answer — unlike a site that refuses to try.

**Why did the shop send me this instead of a number?**
Usually because the parcel had not been handed to the carrier yet when the email went out, so no
number existed. The service was known; the parcel was not.

**The number is mostly digits and still says not found.**
Then it is probably a genuine number that has not been scanned yet. A number exists from the
moment a label is bought, but tracking only begins when the carrier physically takes the parcel.
Give it a couple of working days before treating it as wrong.
