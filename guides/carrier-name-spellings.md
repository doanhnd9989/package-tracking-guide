# One carrier, several spellings: OnTrac, Cainiao, Straightship, YTO

Some carriers are hard to track because nobody knows who they are. These four are hard to track for the opposite reason: people know exactly who they are and still cannot spell them.

That matters, because almost everyone starts by searching the carrier's **name**. If the name you type is not the name the company uses, you land on the wrong page, or on no page at all — and you conclude something is wrong with your parcel when nothing is.

## The short version

**The number identifies the carrier. The name does not.** A tracking number is issued by a carrier's own system. A name is a label a seller typed into an order field, translated from another language, or inherited from a company that has since been renamed. When they disagree, trust the number.

## The four, and what they actually are

All details below come from each company's own website.

| What people type | The company's own name | What it is |
|---|---|---|
| "on trac", "on track", "fastrac ontrac" | **OnTrac** (one word) | A United States parcel carrier built for e-commerce last-mile delivery. Its own site calls it "The #1 Alternative Carrier Network for Ecommerce" and the largest alternative carrier network in the country. |
| "cai niao", "cacainia", "caiaino", "cainiao kargo takip" | **Cainiao** | The logistics arm of Alibaba Group — the network behind most parcels bought on AliExpress, Taobao and Tmall. |
| "straight ship", "straighship", "starship shipping" | **Straightship** (one word) | A logistics company headquartered in Burnaby, British Columbia, moving goods between Asia — China in particular — and North America. |
| "yuan tong", "yuantong", "au-yto" | **YTO Express** / **圆通速递** (Yuantong Express) | A Chinese express company based in Shanghai, listed in Shanghai and Hong Kong, delivering to more than 150 countries and regions through partners. |

Note the fourth row: the people spelling it "wrong" are right. Yuantong is the English spelling of the company's Chinese name; YTO is the abbreviation it uses abroad. Both are correct names for the same carrier. In Australia the same operation also appears written as **AU-YTO**.

## Why carrier names are so slippery

Three reasons, none of which is your fault:

1. **Companies rename and merge.** The network delivering your parcel today may have been printed on an older label under a different name. See [carrier-renamed-dead-tracking-site.md](carrier-renamed-dead-tracking-site.md).
2. **One company can have two correct names** — a legal name in one language and a trading name in another. That is the YTO / Yuantong case, and it repeats across most Chinese and Japanese carriers.
3. **The label names the carrier the *sender* used.** On a long route that company usually hands the parcel on again, so the company that knocks on your door may never appear on the label. This is the normal pattern for Cainiao.

## Does the number have a recognisable shape?

Sometimes. It is worth knowing which case you are in, because the answer changes what you should do.

| Carrier | Shape | Reliable enough to go on? |
|---|---|---|
| Straightship | Five letters then 13 digits, 18 characters total; most begin **STRCA** | Yes — one shape dominates what we see |
| OnTrac | Mixed. Some start with **D**, many are all digits | No — treat shape as a hint only |
| YTO Express | Mixed. Several prefixes in regular use | No |
| Cainiao | Mixed, because the parcel may carry a partner's number | No |

The pattern behind the mixed ones is the same in each case: large carriers absorb other networks, inherit their numbering, and carry partner numbers for cross-border legs. A single clean "format" only exists for carriers that issue every number themselves.

For carriers whose format *is* fixed, see [tracking-number-formats.md](tracking-number-formats.md) and [ups-1z-number-decoded.md](ups-1z-number-decoded.md).

## What to do instead of searching the name

1. **Paste the number first.** A universal tracker such as [24hTrack](https://www.24htrack.com) detects the carrier from the number itself — 3,200+ carriers, free, no sign-up. Spelling is irrelevant to it.
2. **Read the whole event list, not the latest line.** On a Cainiao parcel the handover to a local carrier is usually written there in plain language, which tells you who to talk to about the final leg.
3. **If nothing recognises the number at all**, consider that it may not be a tracking number. Sellers often send an order reference instead — see [order-number-vs-tracking-number.md](order-number-vs-tracking-number.md).

## When the name *does* matter

One moment: when something has gone wrong and you need a human.

Even then, the carrier is usually not the party to contact. The shipping contract belongs to the seller who booked the shipment, not to you, so they are the one who can open a trace or send a replacement. What you want to carry into that conversation is not the carrier's name — it is the number, the time of the last scan, and the place it happened. See [who-to-contact-parcel-problem.md](who-to-contact-parcel-problem.md).

## FAQ

**Is "On Trac" a different company from OnTrac?**
No. Same carrier, two spellings, and only one of them is the company's own.

**Is Yuantong the same as YTO Express?**
Yes. 圆通速递 (Yuantong Express) is the registered name; YTO is the abbreviation used internationally. AU-YTO is the same operation in Australia.

**My Cainiao tracking says delivered — who actually delivered it?**
Almost certainly a local carrier in your own country that Cainiao handed the parcel to near the end of the journey. The handover is normally visible in the full event list.

**My number does not match any of these shapes. What now?**
Then it may not be a carrier's number at all. Go back to the seller and ask specifically for the carrier's own tracking number, and for the carrier's name as the carrier spells it.

---

*Maintained by the team at [24hTrack](https://www.24htrack.com), a free multi-carrier package tracker. Corrections welcome via issues.*
