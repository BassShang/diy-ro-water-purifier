# Bilibili 「DIY净水器」 Video Survey: Index

Survey of Bilibili videos returned by searching **「DIY净水器」 sorted by play count (最多播放)**, taken in order from highest to lowest. Each relevant video gets an architecture write-up in this folder. Plays come from the Bilibili search API on **2026-10-18 (UTC+8)**.

> ⚠️ **Read this first: evidence level varies a lot.** Bilibili started answering this box with **HTTP 412** (anti-crawler block) a few minutes into the run, right after the search pages were fetched. One retry after a ~6-minute back-off also failed, so **all Bilibili access was stopped** under the project's rate-limit rule. As a result, **no new videos were downloaded, no frames were extracted, and no comments (including pinned BOMs) were read in this run.** The write-ups use only what was legitimately available (see *Method & sources* below). Every file states exactly which sources it used, and anything not seen is marked *not verifiable* or *unverified*.
>
> Evidence key: **T** = audio transcript (auto, approximate) · **D** = text description (Bilibili or original YouTube) · **S** = real in-video screenshots · **C** = uploader cover image only.

> **2026-10-19 enrichment (Asia/Shanghai), pass 1:** anonymous view + reply APIs succeeded for BV1nGUYY9ES7 (#04). yt-dlp webpage download then returned **HTTP 412**; that pass stopped. #04 updated from view/comments only (no new frames).
>
> **2026-10-19 enrichment (Asia/Shanghai), pass 2 (~12:05–12:09):** anonymous view + reply APIs succeeded for BV1RhPCeLEHP (#05) including pinned comment + CNKB FPD-360P product photo. yt-dlp webpage download again returned **HTTP 412**; the run stopped immediately (no retries). #05 updated from view/comments only (no in-video frames). Remaining priority videos were not fetched.

> **2026-10-19 enrichment (Asia/Shanghai), pass 3 (~13:09–13:11):** anonymous view + reply APIs succeeded for BV1Dz421U7CZ (#06) (pinned 乐天鹅800G vs 小米800G affiliate links; hot thread on 零陈水/纯水泡膜). yt-dlp webpage download returned **HTTP 412**; the run stopped immediately (no retries, no further videos). #06 updated from view/comments only (no in-video frames).

## Index (relevant videos, by plays)

| # | Search pos. | Title | Uploader | Plays | Architecture (one-liner) | BOM? | Diagram? | Evidence | File |
|---|---|---|---|---|---|---|---|---|---|
| 01 | 2 | 滤芯竟然这么便宜，我们自己 DIY 了一台满配净水器！ (We DIY'd a fully-loaded purifier) | 先看评测 | 1,672,300 | PP(5-layer) → sintered carbon → pump → custom RO 2.8 m² "1000G" → UF → post carbon; tankless + small external zero-stale-water tank; optional instant-hot faucet; enclosed tower (commercial product) | Price only (¥1499; BOM cost > ¥1000) | No | T, D, S | [01](01-BV1oW421X7bA.md) |
| 02 | 3 | 【迷瞪】自己动手，安个净水器吧 (Install a purifier yourself) | Mr迷瞪 | 528,896 | PP → GAC → CTO → tee{UF via PRV → wash tap; pump(50G) → RO 50G → check → HPS → T33 → mineral → alkaline} → pressure tank; open rack, 24 V board | In pinned comment (not fetched) | Wiring colors told | T | [02](02-BV1C54y1v7mC.md) |
| 03 | 6 | 小白DIY净水器，秒杀品牌机？ (Beginner DIY vs brand) | TESTV官方频道 | 376,421 | LPS → PP → CTO → UF → tee{wash tap; solenoid → pump → RO 75G → check → HPS → T33} → pressure tank; 18 s waste solenoid; no leak protection | No ("over ¥1000" total) | Drawn in video (not captured) | T, D, C | [03](03-BV1ao4y1W7J7.md) |
| 04 | 8 | 我老婆老说…今天做一个净水器 (Purifier to impress my wife) | 帅农鸟哥 | 267,616 | Stainless box, manual pour-in; sand/stone + bamboo charcoal canisters (comments); non-RO gravity/multi-media | No (pinned = tea promo) | No | D, C | [04](04-BV1nGUYY9ES7.md) |
| 05 | 11 | 自己动手攒一台净水器有多简单 (How easy is DIY) | 西安无忧水务净水 | 239,912 | Housings + RO (unverified chain); **18 s CNKB FPD-360P combo waste valve** (pinned photo); wrong valve → no pure water | Waste valve only (CNKB FPD-360P-DC24V); no full BOM | No | D | [05](05-BV1RhPCeLEHP.md) |
| 06 | 12 | diy通用滤芯净水器，成本便宜10倍，真的好用吗? (Universal-filter purifiers: any good?) | 哏工侃智能 | 223,487 | Review: 乐天鹅800G 通用滤芯 vs 小米800G 定制滤芯 (pinned); 零陈水/纯水泡膜 discussed in comments | Affiliate links only (not DIY BOM) | No | D | [06](06-BV1Dz421U7CZ.md) |
| 07 | 15 | 花了500，我DIY了一台反渗透式净水器 (¥500 RO DIY) | Michael_8396 | 176,831 | 3×10" → pump → top RO housing + inline post; status-display board; pressure tank (cover) | Pinned (not fetched); ¥500 total | No | C (audio has no speech) | [07](07-BV1M24y1a7Nk.md) |
| 08 | 17 | 75G五级净水器DIY教程 (75G 5-stage tutorial) | 不喝奶的鱼 | 164,927 | 5-stage, 75G RO, booster pump, pressure tank, control kit (title + cover) | No | No | C | [08](08-BV1Re4y1r7mw.md) |
| 09 | 18 | 【vlog】净水器怎么自己安装？搬家拆机之后你还装的回去吗 (Reinstall after moving) | 甄莱斯 | 150,154 | Relocation/reinstall vlog; angle valve + dedicated faucet + drain (cover) | No | No | C | [09](09-BV1UuUKBnEAo.md) |
| 10 | 20 | 沉浸式DIY手搓RO反渗透净水器教程 (Immersive RO build) | 马达师 | 141,242 | Raw TDS → 3×10" → tee{wash tap; gauge → LPS → solenoid → pump → RO → check → HPS → tee(tank) → T33 → pure TDS}; waste solenoid → drain; **leak probe auto-stop**; steel stand | No | Full verbal recap | T, C | [10](10-BV1RMakeJE2n.md) |
| 11 | 21 | DIY净水器三代编年史 (Three generations of DIY purifiers) | 水智狮 | 115,859 | Market overview; cover shows integrated LTE-600G universal-cartridge box | No | No | D, C | [11](11-BV1a82uYTEKD.md) |
| 12 | 22 | 买净水器不知道怎么选…组装净水器、DIY 净水器教程 (Seller one-minute tutorial) | 钦选净水器 | 114,112 | Universal filters + dedicated faucet; rest unverified | No | No | — | [12](12-BV1cJb96cEmn.md) |
| 13 | 24 | 100块组装无电纯水机超详细教程 (¥100 no-electric RO) | 西安无忧水务净水 | 97,480 | **Pump-less** mains-pressure RO: inline pre → RO → inline post carbon (cover) | ¥100 total | No | C | [13](13-BV1dCXLYVEZC.md) |
| 14 | 25 | 为什么把小米净水器改装成通用滤芯？ (Xiaomi → universal filters) | 另一半净水科技 | 97,232 | Brand Xiaomi machine with cartridge bays tubed out to external generic housings (cover) | No | No | C | [14](14-BV1ZG411g73g.md) |
| 15 | 27 | 手把手教你安装净水器，新手友好 (Install tutorial) | 锦程0319 | 85,363 | 75G kit, frame or hanging-plate versions (seller description) | Kit prices ¥680 / ¥549 | No | D | [15](15-BV18m421j7A6.md) |
| 16 | 29 | 净水器DIY，小白必看！ (DIY tutorial) | 锦程0319 | 79,254 | Same 75G kits (seller description) | Kit prices ¥680 / ¥549 | No | D | [16](16-BV1vr421t7t8.md) |
| 17 | 32 | diy组装家用净水器ro反渗透超滤水机（3/1） (RO + UF DIY, part 1) | 无聊的改造 | 63,862 | RO + UF dual outlet (series titles); solenoid, pressure switch, LCD controller, pump (cover) | No | No | C | [17](17-BV1X3411c74Z.md) |
| 18 | 33 | 我为什推荐你 DIY 一台净水器 \| 保姆级教程系列（1） (Why DIY, series part 1) | 温特的移动城堡 | 62,646 | Motivation episode; 3×10" rack unit with gauge + RO controller (cover); 7-part series covers switches, leak protector, waste ratio | No | No | C | [18](18-BV1mF15YuEfh.md) |
| 19 | 34 | DIY净水器3年使用体验分享 (3 years of use) | 红星小学中队长 | 59,322 | Compact plate-mounted pumped RO with inline cartridges; "¥50/year" running cost (cover) | No | No | C | [19](19-BV1wDdGYXEPt.md) |
| 20 | 35 | DIY净水器原理丨详细全过程分享 (DIY purifier principles, reprint) | 不喝奶的鱼 | 58,410 | 10" 5 µm → [carbon/resin] → 1 µm; pump after 1st housing; RO 1812 + flow restrictor; HPS + solenoid + check + LPS; tank → T33 | No | **Yes (cover diagram)** + full text | D (YouTube original), C | [20](20-BV1ri4y1k71v.md) |

**Stopped at rank 20** (search position 35). The target of 20 relevant videos was reached, but most entries are shallow because of the access block. Next in line by plays (not analyzed): BV1Pkr8BhEvf (st冰雪香飘飘, "0陈水" RO principles, 57,091), BV144dUBsEmv, BV1ypmZYFEyu, BV1xwAWe6EVz, BV1z3411K7QS, …

## Skipped (not about building a household drinking-water purifier)

Search positions 1–35, decided from title, description, and tags (videos not watched):

| Search pos. | BV | Title | Uploader | Plays | Reason |
|---|---|---|---|---|---|
| 1 | BV1mDd8Y1EJX | 自制净水器 (Homemade water filter) | 科学散装户 | 5,931,165 | Kids' science experiment (description: hands-on experiments for children; category 科学科普) |
| 4 | BV1wK4y1v79f | 【迷瞪】净水器大起底，消费者该怎么选 (Purifiers exposed: how to choose) | Mr迷瞪 | 395,730 | Buyer's guide / explainer, not a build (it's the prequel to #02) |
| 5 | BV1E1YteQEPB | 男人利用玻璃瓶与塑料瓶制作太阳能净水器 (Solar still from bottles) | 老叔工坊 | 393,782 | Solar-still craft, not a household purifier |
| 7 | BV15z4y1E7FN | 【开箱】主流台式净水器到底哪一款更适合你？ (Countertop purifier unboxing) | 嘉琦Jacky | 356,974 | Brand countertop unboxing / review |
| 9 | BV14dj36pE34 | 自制净水过滤器水质检测来啦 (Homemade filter water test) | 阿嘟的美食 | 248,618 | Craft filter water test (54 s) |
| 10 | BV1ELMcz6EQf | 可自行DIY的净水器？碧云泉小积木评测体验 (碧云泉 review) | 朴雨夏树 | 245,199 | Brand product review |
| 13 | BV16vHXzRERH | 换芯成本堪比DIY？海尔甜美净水器实机测评 (Haier review) | Wilson学长 | 200,397 | Brand product review |
| 14 | BV1KuSRYFEwz | 【算账】谁是净水器刺客？…31款 (31 brands compared) | 单毅讲装修 | 186,833 | Brand comparison / shopping guide |
| 16 | BV1zk9qY7EaW | 前置过滤器DIY省钱攻略 (Pre-filter DIY savings) | Q姐和老6 | 173,237 | Whole-house pre-filter, not a drinking purifier |
| 19 | BV1N7411y72s | 【千万不要玩】上课想喝水怎么办？先diy一个净水器 (Toy) | 千万不要玩 | 149,852 | Kids' toy |
| 23 | BV1Pf4y1B7jS | 【原始建造】…兄弟俩速成物理净水器 (Primitive build) | JungleSurvival | 104,723 | Primitive / bushcraft filter |
| 26 | BV1PMj8z7EUg | 618净水器怎么选？…易开得…真实测评 (易开得 review) | 小菘蓝聊家电 | 90,372 | Brand product review |
| 28 | BV1B241epEfm | 买在某宝买的DIY净水器，乐天鹅的 (Bought LTE unit) | 明天要说早安 | 83,321 | 30 s clip of a purchased pre-built unit (TDS reading only) |
| 30 | BV1Gp4y1P7d9 | 用木炭和沙子，在非洲部落过滤脏水 (Charcoal and sand, Africa) | 环华十年 | 74,688 | Charcoal and sand field filter (travel) |
| 31 | BV1raAczcEV4 | 自制净水器过滤江水，结果差点翻车 (River-water filter) | 三户三户 | 74,450 | Craft filter experiment |

## Common patterns so far

These are based only on what was verified (transcripts for 02, 03, 10; text for 01, 20). Cover-only entries are treated as weak, consistent evidence.

1. **The canonical DIY layout** (02, 03, 10, 20; consistent with the covers of 07, 08, 17, 18, 19): 3 × 10" pre-filters (PP + carbon) → **LP switch → inlet solenoid → booster pump → RO → check valve → HP switch** → **pressure tank** → T33 post carbon → faucet. RO concentrate goes through a **waste solenoid / flow restrictor** to the drain. A generic **24 V control board** ties it together. Tank builds use small membranes (**50G in 02, 75G in 03**).
2. **Dual outlet is common:** a tee after the pre-filters feeds a separate tap with pre-filtered or UF water for washing (02, 03, 10; 17 by title). It's useless for a countertop drink-only unit but explains the extra tee in many BOMs.
3. **Pressure-tank placement matters:** 10 explicitly puts the tank **between the RO and the T33** (never after, to keep carbon fines out of the tank). 20 likewise puts the T33 after the tank, partly to handle water that sat too long. Neither applies UV to the tank.
4. **UV sterilization:** not mentioned in any verified source. Water-safety measures seen are instead the **post-carbon position** (10), a **UF guard in front of the post carbon** against bacteria creeping back from the outlet (01, citing papers and industry experts it doesn't name), and **zero-stale-water flushing** (01).
5. **Leak/flood protection is rare:** only 10 uses a board **leak probe that stops the machine**. 03 flooded an office and lists "no leak protection" as its main shortcoming. 15/16 (seller) and the 温特 series (18, by tags) treat leaks as a key pain point.
6. **Tankless high-flux (≥600G) is essentially absent from home builds.** It appears only in the commercial product 01 (marketed 1000G, plus a small external zero-stale-water tank) and the integrated LTE-600G box on 11's cover.
7. **Portability:** every home build is an **open rack or hanging plate**. A single enclosed box shows up only in commercial products (01, 11). One vlog (09) is specifically about reinstalling after a move. Pump-less RO (13) and compact plate builds (19) are the smallest footprints seen.
8. **Heating:** only 01 (an optional separate instant-hot faucet).
9. **Most common pitfalls** (verified): threaded joints leaking (needs enough PTFE tape), push-fit tubes not fully seated, a cartridge installed backwards (no flow, solenoid gets hot), inlet and waste solenoids confused, RO pure and waste ports swapped, carbon fines on first use (flush), and no LP switch (pump runs dry when the water supply cuts out).
10. **Cost signals:** ¥100 (pump-less, 13), about ¥500 (07), seller kits ¥549–680 for 75G (15/16), "over ¥1000" for a beginner who overbought (03), and ¥1499 for the commercial 1000G unit (01).

## Method & sources

- **Search:** `api.bilibili.com/x/web-interface/search/type?search_type=video&keyword=DIY净水器&order=click`, pages 1–4 (80 results), fetched 2026-10-18 about 12:31 UTC+8 with an anonymous visitor cookie (not signed in).
- **Block:** the next request (video `view` API) got **HTTP 412**. One probe after a ~6-minute back-off was also 412, so Bilibili access was stopped completely (rate-limit rule: sequential, throttled, back off, then stop if it repeats).
- **Fallbacks used (not Bilibili servers):**
  - **BiliPlus** public mirror API for description and publish date.
  - BiliPlus **image mirror** for the uploader covers.
  - **Audio files** saved by an earlier run (2026-10-17) for 01, 02, 03, 07, 10, re-transcribed with faster-whisper `small` + VAD. Every transcript-derived fact is marked approximate.
  - Player screenshots of 01 from the earlier run.
  - Public **YouTube** pages for 01 (`M-m6Hqr0EB8`, description) and 20 (`13AZ_KRE73g`, the original of the reprint). YouTube refused video downloads with a bot check.
- **Screenshots:** files in `img/` named `-cover-` are **uploader covers, not in-video frames**. Only the two 01 images are real player frames.
- **To finish this survey properly** (from a network that Bilibili doesn't block): download each video at low resolution, extract frames, read pinned comments and BOMs (02, 05, 07), and upgrade the C-level entries.
