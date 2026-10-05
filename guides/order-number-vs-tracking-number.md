# "Shipped and tracked" but no site finds the number

Your order page says **shipped**. It may even say **tracked**, and it gives you a number. You paste that number into every tracking site you can find and every one returns nothing.

The order page is not lying to you. The number you were given may simply not be a carrier tracking number.

---

## Why a shop can say "tracked" when no carrier knows the number

A marketplace marks an order as shipped the moment the **seller** tells it the order shipped. Along with that, the seller uploads a reference.

- Sometimes that reference really is the carrier's number.
- Sometimes it is the seller's own code for the job, out of their own warehouse system.

The platform displays whatever it was handed. It does not go and check that a carrier somewhere in the world recognises it. So "shipped and tracked" describes **what the seller claimed**, not what a courier confirmed.

---

## Three checks, about a minute

### 1. Does the shape match any carrier's published format?

Real carrier numbers follow published patterns:

| Shape | Usually |
|---|---|
| `1Z` + 16 alphanumeric | UPS |
| 20–22 digits starting 92–95 | USPS |
| 12 or 15 digits | often FedEx |
| 2 letters + 9 digits + 2-letter country code (e.g. `LK047979948FR`) | international post — last two letters are the **origin** country |
| 12 characters, commonly 3 letters + 9 digits | Purolator (Canada) |

A number that matches no carrier's format anywhere is usually an internal reference. You do not have to memorise these — a universal tracker such as [24hTrack](https://www.24htrack.com) detects the carrier from the number itself.

### 2. Has it ever produced a single scan?

A real carrier number normally produces at least one line within a few days of being created, even if that line only says *Label Created* or *Information Received*. **One line is enough** — it proves a carrier has the number in its system.

Weeks of complete emptiness, with no line at all, is the signal that matters. That is the pattern an internal code produces, because no carrier ever had it.

### 3. Ask the seller three narrow questions

"Where is my parcel?" invites a copy-and-paste reply. Ask instead:

1. **Which carrier physically has it?**
2. **The number exactly as printed on the label** — not as typed into the order page.
3. **Was the number replaced after dispatch?**

Those three are hard to answer with a template, and any one of them usually unblocks you.

---

## What it usually turns out to be

1. **The seller's own order or warehouse code.** Means something only inside their building.
2. **A consolidator job number.** Issued while your parcel waits to be combined with others. When it is finally handed to a carrier, a real number is created and the old one is never updated.
3. **A real number created early and not yet scanned.** Looks identical from the outside — which is exactly why the shape check is worth doing first.

---

## The exception: carriers that accept the shipper's reference on purpose

A few carriers will take the shipper's own code deliberately. Purolator is the clearest example: its own tracking box asks for **"a PIN or Reference"**, and a Reference there is a code of up to 15 characters that the shipper chose. On a Purolator shipment, a short word or an order code can genuinely work.

On most carriers it cannot. Trying it costs nothing — try once, then stop retrying and go ask the seller.

---

## What not to do

Do not spend a fortnight refreshing. If a number has never produced a line, refreshing produces nothing, because there is nothing behind it to update.

The clock that **does** matter is the marketplace's own. Buyer-protection windows expire whether or not the tracking ever worked. Open the dispute while the window is still open — you can always close it when the parcel turns up.

---

## FAQ

**Is "shipped" on my order page proof the parcel exists?**
No. It means the seller marked it shipped. The parcel may be printed-label-only, or waiting at a consolidator.

**My number worked on one site and not another. Which is right?**
Usually both: one site resolved the carrier and the other did not. If a universal tracker also finds nothing, the number itself is the problem.

**The seller sent a new number a week later. Why?**
Common with consolidated freight: the first code was internal, and a carrier number was only issued when a carrier physically took the parcel. The old number will never update.

**How long should I wait before treating it as a bad number?**
If there is no scan of any kind after about five days, treat it as a data problem rather than a delivery problem. The question to the seller changes completely.

---

*Part of the [package tracking guide](../README.md). Checks and formats verified against carriers' own tracking pages, October 2026.*
