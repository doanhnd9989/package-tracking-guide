# Your parcel stopped at a number: reading a postal tracking history

Courier tracking names places in words — a depot, a city, a sorting centre. Postal tracking often names them as **numbers**, and the first time you see one it reads like an error code rather than a building.

It is a building. Postal services identify their own offices by number, and the number that your history has stopped on is usually the most informative thing on the page.

## The four lines that do most of the work

Taking a cross-border postal history as the example, these are the entries that recur:

| What you see | What it means |
|---|---|
| *Dispatch* / *Otprema* / *Отпрема* | The item **left** that office. It is moving. |
| *Receipt* / *Acceptance* | The item was **taken into** the network at that office. |
| A five-digit office number + **office of exchange** | The national gateway for international mail. |
| A five-digit office number + **customs** | The customs post. The item is with the authorities. |

The two gateway lines are the ones worth recognising, because they are the two stages in a postal journey that **go quiet by design**.

## Office of exchange: a hand-over, not a journey

An office of exchange is where one country's postal service hands items to another country's. Everything crossing the border passes through one on the way out and another on the way in.

Nothing is being driven anywhere while an item sits there. Two organisations are reconciling bags and paperwork, and the receiving side will not scan the item until it has formally accepted it. A record resting on an office-of-exchange line for a couple of days is doing exactly what the stage is for.

## Customs post: not the carrier's clock

Where a postal service has a dedicated customs office, you will see it as its own numbered location. A record sitting there is not with a courier at all — the wait is set by the customs authority, and the postal service cannot scan the item forward until it is released.

This matters for who you ask. Nobody at the postal service can speed up a customs queue, and a tracking site cannot see inside one.

## The one line that genuinely wants something from you

Everything above is waiting. One line is not:

> **Unsuccessful delivery attempt** — *Neuspešan pokušaj uručenja*, *Recipient is not available at the address*

That means somebody tried, failed, and is now **holding** your item. Holding periods are finite. This is the line to act on, usually by arranging redelivery or collecting from the named office, and it is the only one where waiting costs you something.

## Why your number does not end in your own country's code

The other thing that makes a correct number look wrong.

International postal numbers use the UPU S10 pattern: **two letters, nine digits, and a two-letter country code** — for example `RR123456789CN`. That trailing code is the country the item was **posted in**, and it never changes.

So if something was posted abroad and delivered to you, the number keeps the *sender's* country code for the entire journey. A parcel posted in Denmark and delivered in Serbia stays a Danish number. Your own postal service picks it up at the office of exchange and keeps writing on the same number.

Two consequences:

- A number ending in a country that is not yours is **not** evidence of a wrong number.
- The history will change language partway down, because a second postal service started writing in its own. That is the hand-over, not a glitch. (See [tracking page not in English](tracking-page-not-in-english.md).)

## How to read your own page in ten seconds

1. Find the **last** line, not the elapsed time.
2. If it names an office of exchange or customs — it is in a hand-over or a queue. Wait.
3. If it says dispatch — it is moving between offices and the next scan may be a day or more away.
4. If it says a delivery was attempted — act today.
5. If the number does not end in your country's code — that is normal for anything posted abroad.

The elapsed clock is the least informative thing on the page. In postal networks, the **place** is the explanation.

---

Related: [international parcel journey explained](international-parcel-journey-explained.md) · [tracking number formats](tracking-number-formats.md) · [package held at customs](package-held-at-customs.md) · [tracking not updating](tracking-not-updating.md)

Maintained by [24hTrack](https://www.24htrack.com) — a free tracker across 3,200+ carriers. Paste any tracking number and the carrier is detected from the number itself, no account needed. CC BY 4.0.
