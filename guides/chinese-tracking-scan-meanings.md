# Chinese Tracking Scans: What 已妥投, 离开处理中心 and the Rest Actually Mean

If your parcel shipped from China, part of your tracking page will be in Chinese. Nothing is broken and nothing is lost. A tracking page is a log, and a line is written at one moment only: when a person or a machine physically handles the parcel. For the first half of a China-origin journey those handlers are Chinese sorting centres, Chinese customs and a Chinese airline, so the entries are written in the language of the system recording them. English usually starts only once the destination country's network takes over.

A timeline that is half Chinese and half English is not a glitch. It is the handover, made visible.

## The glossary, in the order you meet it

### Collection and the first scan

| Chinese | English | What it tells you |
|---|---|---|
| 已收寄 | Item accepted | The network physically has the parcel. This, not your payment, is when the clock starts. |
| 已收货 | Goods received | Same idea, used by consolidators rather than the post. |
| 已入库 | Received into warehouse | The parcel is at a consolidation warehouse waiting for a shipment to fill. |

### Moving inside China

| Chinese | English | What it tells you |
|---|---|---|
| 到达处理中心 | Arrived at a sorting centre | Normal. Repeats several times on one journey. |
| 离开处理中心 | Departed a sorting centre | Normal. The pair above and below repeat as the parcel moves hub to hub. |
| 邮件到达处理中心 / 邮件离开处理中心 | Arrived at / departed a sorting centre | Identical events. 邮件 simply means "mail". |
| 进入分拨中心 / 离开分拨中心 | Arrived at / departed a distribution centre | Same thing at a different type of facility. |
| 干线中转 | Line-haul transfer | On a long-distance truck or rail leg between cities. |

### Customs and the flight

| Chinese | English | What it tells you |
|---|---|---|
| 出口清关完成 | Export customs clearance completed | China has released it. |
| 等待清关 | Awaiting customs clearance | Queued. Can sit unchanged for days and usually needs nothing from you. |
| 航班已飞 / 航空公司启运 | Flight departed | The longest silence of the whole journey starts about here. |
| 目的国清关完成 | Customs cleared in the destination country | The one worth waiting for. After this the local network takes over and English usually begins. |
| 境外进口海关留存待验 | Held by destination import customs for inspection | Selected for a check. Normally clears on its own; act only if you are asked for a document or a payment. |

### Delivery

| Chinese | English | What it tells you |
|---|---|---|
| 出门投递 | Out for delivery | A courier is carrying it today. |
| 派送中 | Out for delivery | Same meaning, different carrier's wording. |
| 已妥投 | Delivered | |
| 已签收 | Delivered, signed for | |
| 派送失败 / 妥投失败 / 未妥投 | Delivery failed | An attempt was made and did not succeed. This is **not** a delivery. |

### The one that looks alarming and is not

| Chinese | English | What it tells you |
|---|---|---|
| 查询不到 | No information found | The carrier holds no record for that number. That is different from saying the parcel is gone — it usually means the number belongs to a different leg of the journey, or nothing has been scanned yet. |

## How to read the silence

Counting days tells you how impatient you are. The **type** of the last scan tells you whether anything is wrong.

- Last scan is a Chinese sorting centre or 航班已飞 — the parcel is on a line-haul or a flight. This is where journeys go quiet for the longest, because nothing is being handled, so nothing is scanned. Waiting is correct.
- Last scan is 等待清关 — queued at customs. Normal, unless you were asked for duties or a document; that is the one silence waiting on **you**.
- Last scan is 目的国清关完成 or a depot in your own country, and then nothing for about a week — that is the one genuinely worth chasing.
- 查询不到 on a number the seller gave you — check you were given the tracking number and not the order number.

## "已妥投" but nothing arrived

Treat it exactly as you would an English "delivered" scan:

1. Give it a day. Delivered scans are sometimes recorded slightly ahead of the drop.
2. Check neighbours, parcel lockers and the building's mail room.
3. Then go back to the **seller**, not the carrier. The seller paid for the shipping, so they are the carrier's customer, and most carriers will not open an investigation for the recipient.

Quote the last scan with its date and place when you do. A concrete timeline gets a real answer; "it never came" gets a template.

## Why half-translated is worse than untranslated

If you build tracking software, one rule matters more than the dictionary: translate a line fully or leave it exactly as the carrier wrote it.

`包裹已签收，如有疑问请联系收件人` contains a phrase most glossaries have (已签收, delivered and signed for) and a clause most do not (*if you have questions, contact the recipient*). Replace only the first and the user reads "Delivered (signed for)，如有疑问请联系收件人", which looks like broken software and hides the half you failed to read — a half that may carry an instruction.

A useful boundary: a run of four or more Han characters is a clause, not a place name (深圳 is two, 东莞市 is three, 如有疑问请联系收件人 is ten). If a run that long survives your replacements, hand back the original.

---

Maintained by [24hTrack](https://www.24htrack.com) — a free package tracker for 3,200+ carriers. Paste any tracking number and the carrier is detected automatically, no sign-up; recognised Chinese scan lines are shown in English on the timeline.

Related: [How to track packages from China](track-packages-from-china.md) · [Tracking status meanings](tracking-status-meanings.md) · [Why is my tracking not updating](tracking-not-updating.md)
