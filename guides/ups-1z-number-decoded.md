# The UPS 1Z Number, Decoded (and Why Typos Fail the Maths)

> Part of the free package tracking guide. You can check any number for free, with no account, at https://www.24htrack.com

A UPS parcel number is 18 characters: `1Z`, then 16 more letters and digits. That much is widely known. What is less known is that the final character is not part of the identifier at all — it is a check digit computed from the 15 characters before it. That single fact explains most "invalid tracking number" complaints.

## Short answer

A UPS parcel number is `1Z` + 16 alphanumeric characters, 18 in total, with no spaces or dashes. Reading left to right after `1Z`: six characters are the shipper's account number, two digits are the service level, eight characters identify the package, and the last digit is a check digit. Because of that check digit, a number with a single mistyped character is usually mathematically invalid rather than merely "not found yet". Not every UPS parcel carries a 1Z number: economy services that hand the last mile to a national postal service, and freight shipments, use other formats.

## The layout

```
1Z  999AA1  01  2345678  4
│   │       │   │        └── check digit
│   │       │   └────────── package identifier
│   │       └────────────── service level (e.g. 03 ground, 01 next day air)
│   └────────────────────── shipper account number (6 chars)
└────────────────────────── fixed prefix
```

Two practical consequences fall out of this layout.

**Parcels from the same shop share their first eight characters.** The shipper account is part of the number, so every label a given seller prints opens the same way. People sometimes report this as a bug ("all my numbers look identical") — it is the account number, working as designed.

**The service level is the only part that says anything about speed**, and the sender chose it when they bought the label. No amount of refreshing changes it.

## The check digit, measured

The last character validates the rest. The algorithm is public: map letters to digits, weight alternate positions, and the final digit makes the total come out even against a modulus.

```python
def ups_check_ok(tn: str) -> bool:
    body = tn[2:].upper()
    if len(body) != 16 or not body[15].isdigit():
        return False
    total = 0
    for i, ch in enumerate(body[:15]):
        v = int(ch) if ch.isdigit() else ((ord(ch) - 65) % 10 + 2) % 10
        total += v if i % 2 == 0 else v * 2
    return (10 - total % 10) % 10 == int(body[15])
```

We ran this over every UPS number added to our platform in the last 60 days — **1,539 numbers, and every single one passed.** Not most of them. All of them.

So when a tracking site says a 1Z number is invalid, the number itself is usually broken, and the usual culprits are the characters that look alike when a number is read off a screen or a printed label:

- `0` (zero) and `O` (letter O)
- `1` (one) and `I` (letter I)
- `5` and `S`
- `8` and `B`

Copy the number rather than retyping it. If you must type it, those four pairs are where to look first.

## When a UPS parcel does not have a 1Z number

This is the part that confuses people, because the parcel is genuinely moving and the number genuinely is not a 1Z one.

- **Economy services.** On the cheapest services the carrier moves the parcel most of the way and then hands it to the national postal service for the final mile. The number you were given is often the postal one.
- **Freight.** Freight shipments use a different reference entirely — usually shorter, usually all digits.
- **A seller's own reference.** Some shops hand you an internal order code and label it "tracking number". It is not a tracking number in any carrier's system, and no tracking site will ever recognise it.

If you are not sure which of these you are holding, paste the number into a universal tracker and let the shape be read for you.

## FAQ

### How many characters is a UPS tracking number?

Eighteen: `1Z` plus sixteen letters and digits, with no spaces or dashes.

### Do all UPS tracking numbers start with 1Z?

No. Parcel numbers do. Economy services that hand the final mile to a postal service, and freight shipments, use other formats.

### Why do all my parcels from one shop start with the same characters?

The six characters after `1Z` are the shipper's UPS account number. Same seller, same account, same opening.

### Is the last digit of a UPS number meaningful?

Yes — it is a check digit calculated from the other characters, which is why a single typo usually makes the whole number invalid rather than simply unknown.

### Can I check a UPS number without creating an account?

Yes. Paste it into [24hTrack](https://www.24htrack.com/carriers/ups) and you get the status and the full list of scans, free, with no sign-up.

---

*Maintained by the team at [24hTrack](https://www.24htrack.com), a free package tracker covering 3,200+ carriers. Licensed CC BY 4.0.*
