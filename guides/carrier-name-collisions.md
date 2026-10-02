# Carrier Name Collisions: when two couriers share a name, and how to tell them apart

Some of the hardest tracking numbers to deal with are not the ones that go missing. They are the ones from a company you have never heard of — or worse, from a company whose name is also somebody else's.

This guide covers how to work out who actually has your parcel, and the name traps that send people to the wrong tracking page.

## The short version

**Search the number, not the name.** A tracking number is issued by the carrier's own system and carries that carrier's format. A name is just a label somebody typed into an order field. When the two disagree, the number is right.

## Why you have never heard of the carrier

On a cross-border order you do not pick the carrier — the seller does. Sellers choose cross-border shippers that sell to businesses and never advertise to shoppers, so a name that is completely unfamiliar to you can be a large, long-established company.

Examples of the pattern (all details from each company's own site):

| Carrier | What it actually is |
|---|---|
| JCEX | JCEX International Logistics, a Chinese cross-border shipper founded in 2000, headquartered in Hangzhou; says it reaches 200+ countries and regions |
| 247Express | A Vietnamese express courier, the brand of Cong ty Co phan Hai Bon Bay, operating since 2005 |
| Whistl | A UK logistics provider — business mail, parcels through its Parcelhub arm, and fulfilment |

None of these advertise to consumers. All of them turn up on consumer parcels.

## The name traps

### 1. Two companies, one name

**CTT** is the Portuguese post (ctt.pt). **CTT Express** is a Spanish courier (cttexpress.com). Different companies, different networks, different tracking systems. A number issued by one will not be recognised by the other.

If you search just "CTT tracking" you have a coin-flip chance of landing on the wrong one, and the wrong one will tell you your number does not exist — which reads exactly like "your parcel is lost".

**Fix:** search the carrier name *with the country*, or skip the search entirely and paste the number into a universal tracker.

### 2. The name is also an ordinary phrase

**247Express** is a real Vietnamese courier. But type "247 tracking" into a search engine and most of what comes back is about *round-the-clock* tracking, because that is what the words mean in English. The company and the concept compete for the same search.

**Fix:** add the country ("247 express vietnam tracking"), or use the number.

### 3. The initials belong to a bigger company in another industry

Short carrier names collide with well-known brands outside logistics. If the first page of results is about a completely different kind of business, you are probably searching a shared initialism rather than a rare carrier.

**Fix:** add the word "courier" or "logistics" and the country.

## How to read a number's shape

Carriers issue numbers in patterns. Learning the shape of yours lets you tell two numbers apart at a glance:

- **Letters + digits + letters**, e.g. three letters, ten digits, two letters. The trailing letters often encode the destination, so the *same* carrier can issue codes ending in different pairs.
- **Two letters + nine digits + two letters** (like `RB123456789CN`) is the international postal format, UPU S10. The last two letters are the country of origin.
- **`1Z` + sixteen characters** is UPS.
- **Twenty-two digits starting with 9** is a USPS IMpb label.

A caution for developers and anyone writing documentation: do not state a format unless one shape genuinely dominates the numbers you have seen for that carrier. Mixed baskets are common, because merchants file anything into a carrier field. Saying "it is eleven digits" when only half of them are is a guess dressed as a fact.

And never publish a real tracking number as an example — it identifies a real shipment to a real address. Publish the shape.

## Expect a second carrier near the end

Most cross-border shippers do not deliver to your door. They carry the parcel out of the origin country, through export and customs, and then hand the final leg to a courier or post in your country.

So the closing entries on a cross-border journey often read like a domestic carrier's: a nearby depot, then a mailbox, a parcel locker, a front door. Sometimes a second tracking number appears at that point.

This means two things:

1. **A page that stops updating is usually a handover, not a loss.** The first company no longer has your parcel, so it has nothing more to add. A stopped page and a stopped parcel look identical from the outside.
2. **One shipment can legitimately have two numbers.** If you are given a second one, switch to it — from the handover onwards it is the live one.

## When to act, and who to ask

- **Quiet at the start** — normal. Nothing appears until the carrier physically receives the parcel from the seller, which can be days after you were given the number.
- **Quiet in the middle** — normal. Nothing is scanned while a parcel is on an international leg or waiting in customs.
- **Quiet for two weeks with no change at all** — ask the **seller**, not the carrier. Cross-border shippers work for the merchant, not for you; the merchant holds the shipment record and is usually the only party who can open a case.

Be wary of any call, text or email demanding a payment to release a parcel. That pattern follows courier brands closely. Never pay from a link; check on the company's own site.

---

*Part of the [open package tracking guide](../README.md). You can check any tracking number free, with the carrier detected automatically, at [24hTrack](https://www.24htrack.com).*
