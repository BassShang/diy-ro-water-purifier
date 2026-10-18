# Core Parts: Brands and Prices (China-mainland focus)

Which brands DIY builders name for each part, the official specs found, and the few prices that could be verified. Taobao and JD item pages require login, so **most mainland retail prices could not be verified** in this round. Prices below are either from builder posts (dated) or official / overseas listings.

> Evidence key as in [leak-protection.md](leak-protection.md). Pages read 2026-10-18 (UTC+8). Prices are as stated at the source and may be years old.

## 1. Part-by-part

| Part | Brands named | Evidence / spec | Price seen | Source |
|---|---|---|---|---|
| RO membrane | **汇通 Vontron**, **澳维 Ovay**, DuPont/Dow FilmTec | Full rating table in [tank-vs-tankless-uv.md](tank-vs-tankless-uv.md) | ⚠️ not verified | [Vontron](https://en.vontron.com/Product/60.html), [Ovay catalogue](https://www.ovayhydro.com/wp-content/themes/ovay-membrane/assets/downloads/ovay-household-product-catalog-2026.pdf), [DuPont TW30-3012-500](https://www.lenntech.com/Data-sheets/DuPont-FilmTec-TW30-3012-500-L.pdf) [official] |
| Booster pump | **力夫 Lefoo**, **三角洲 Delta**, 邓元 (75G builds), 柏繁 (in LTE T1) | Lefoo LFP600GPD: 24 V, ≤2.8–3.7 A, ≥2.8–3.25 L/min. Delta: 5-chamber 400–600G, 37 dB and CQC / 涉水批件 claims | ⚠️ not verified (EU retail for a similar 600G pump: see osmounity) | [Lefoo](https://www.lefoo.com/products/24v-dc-ro-booster-pump-lfp600gpd/) [official]; [Delta PR, sohu](https://www.sohu.com/a/405105134_120001238) ⚠️; [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| Solenoids & pressure switches | **科博 CNKB / Kebo** | Inlet NC valve, waste valves, HP/LP switches; official catalogues online | "about ¥10 each" (builder, ~2020) | [chinakebo.com](https://www.chinakebo.com/product/dcf/), [cnkb.cc](https://cnkb.cc/Product/gykg/) [official]; [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| Housings (10" & membrane) | **崧泉 Song Chuan** (Taiwan), 苏尔 / Surprue | 崧泉 EG-14WW 10" housing: PP body and cap, 1/4" / 3/8" / 1/2" ports, **NSF**; burst pressure not published. Surprue claims burst **>3 MPa** for its large whole-house PP housing | ⚠️ | [ro-housing.com.tw](https://www.ro-housing.com.tw/eip/product_ro_info.php?id=246&kind=61&series=62) [official]; [surprue.com](https://surprue.com/channels/69.html) [official, whole-house products — not the small RO housings] |
| Fittings, waste-ratio valve | **中荷** (NSF claimed by builder) | — | ⚠️ | [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| Tubing | **CCK** | 3分 tubing for pre-filters at ≥400G (commenter) | ⚠️ | [post/a83060p0](https://post.smzdm.com/p/a83060p0/); [post/ak3ld3z8](https://post.smzdm.com/p/ak3ld3z8/) (excerpt) |
| Pressure tank | **光跃** 3G, **沛毅** | 光跃 3G ≈ ¥60; 沛毅 costs ~¥100+ more | builder, ~2020 | [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| Post-carbon | 崧泉 T33 (NSF) | Note: post-carbon is a bacterial regrowth hotspot ([tank-vs-tankless-uv.md](tank-vs-tankless-uv.md)) | — | [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| 24 V PSU | **冠宇达** 24 V 1.6 A (for 75G) | 600G pumps need ≥4 A ([osmounity](https://osmounity.de/en/600-GPD-LDW-Brushless-booster-pump/BP-23-102)) | — | [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| UV-C LED module | Klaran (US, WR2 discontinued), 宁波 Agua Topone EC-12, 杰生 JS-M211 | see [tank-vs-tankless-uv.md](tank-vs-tankless-uv.md) | ⚠️ not verified | [atouvcled EC-12](https://atouvcled.com/product/ec-12/) [official] |
| Thick-film heater module | 吉达 Gida, 嘉业 Jaye | see [heating.md](heating.md) | ⚠️ | [gi-da.com](http://www.gi-da.com/product/7_37) [official] |
| Leak protector | generic 2分 / 3分 | see [leak-protection.md](leak-protection.md) | NT$249–600 in Taiwan; ⚠️ mainland ¥2.8–5.4 (excerpt only) | [麗水](https://www.liwater.com.tw/CON/20938/detail-36a91770-e86e-11ec-8ab6-0309d1b4b0db) |
| Faucet | 304 stainless, lead-free | Comply with GB 18145-2014 (lead leaching ≤5 µg/L) or NSF/ANSI 372 (weighted lead ≤0.25 %) | — | [chinanews on GB 18145-2014](https://www.chinanews.com/gn/2014/06-06/6254481.shtml); [NSF 372](https://www.nsf.org/knowledge-library/nsf-ansi-can-372-technical-requirements) |
| Angle-valve tee | copper or stainless; **avoid zinc alloy** | — | — | [duohuanbao](https://www.duohuanbao.com/archives/537371.html); [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| Controller | open-source ESP32 boards | yuunt 600–800G board; whole build ~¥700–800 (excerpt) | ⚠️ | [oshwhub](https://oshwhub.com/yuunt/600g); [数码之家 thread-410291](https://www.mydigit.cn/thread-410291-1-1.html) (excerpt; page timed out) |

## 2. Whole-build cost references

| Build | Cost | Source |
|---|---|---|
| 75G + 3G tank, mid-tier parts (爱董小白) | about ¥600, plus ~¥200 for top-tier parts. Measured rejection 97.8 % (646 → 14 ppm), waste TDS 782, waste ratio 1:3 | [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| Generic 3-stage + RO on a base board | ¥300–800 | [post/ak3ld3z8](https://post.smzdm.com/p/ak3ld3z8/) ⚠️ excerpt / machine-written style |
| 600–800G ESP32 tankless | ≈¥700–800 | [数码之家](https://www.mydigit.cn/thread-410291-1-1.html) ⚠️ excerpt |
| Open-source BOM (from earlier survey) | ~¥456.6 | [problems.md](../../problems.md) source S6 |
| For comparison: commercial 管线机 alone | ¥980 list (米阳 MGX-1012) | [miyoung](http://www.miyoung.com.cn/product/proshow_213.html) |
| For comparison: Philips ADD6910 countertop (HK) | HK$2,316–3,388 | [hkele](https://hkele.com.hk/ADD6910) |

## 3. Selection rules distilled from sources

1. **Pressure-bearing plastics** (housings, tees) are the flood risk: prefer opaque PP NSF housings over transparent ones, and metal tees over zinc ([duohuanbao](https://www.duohuanbao.com/archives/537371.html)).
2. **Size the pump and PSU together**: 600G needs ~3–4 A at 24 V ([Lefoo](https://www.lefoo.com/products/24v-dc-ro-booster-pump-lfp600gpd/)). Mind duty-cycle limits like 12 h on / 30 min off ([osmounity](https://osmounity.de/en/600-GPD-LDW-Brushless-booster-pump/BP-23-102)).
3. **Match membrane to pump**: the yuunt board runs an 800G membrane on a 600G pump ([oshwhub](https://oshwhub.com/yuunt/600g)); see also [problems.md](../../problems.md) item 8.
4. **Check certification claims on the parts that touch water**: NSF on 崧泉 housings is stated by the maker; the 中荷 NSF claim comes only from a builder post. ⚠️
