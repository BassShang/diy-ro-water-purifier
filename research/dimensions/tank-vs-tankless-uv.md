# Tankless High-Flux vs. Small Tank + UV

Should the countertop box be **tankless** (400–800 GPD membrane, direct output) or have a **small tank with UV**? This page covers membrane and pump flow ratings and the conditions behind them, first-draw ("stale water", 陈水) TDS, bacterial regrowth measurements, and UV-C LED module specs.

> Evidence key as in [leak-protection.md](leak-protection.md): **[official]** · **[post]** · **[paper]** · **[excerpt]** (search excerpt only) · ⚠️ uncertain. Pages read 2026-10-18 (UTC+8).

## 1. Membrane ratings: read the test conditions first

Chinese and US datasheets rate membranes under **different conditions**, so "600G" from two makers is not the same thing.

| Membrane | Rated flow | Test conditions | Rejection (avg / min) | Recovery | Size | Source |
|---|---|---|---|---|---|---|
| DuPont FilmTec TW30-1812-75 | 75 GPD (≈12 L/h, ±20 %) | **50 psi**, 250 ppm NaCl, 25 °C | 98 % | 15 % | 1.8 × 12" | [Lenntech PDF](https://www.lenntech.com/Data-sheets/Dow-Filmtec-TW30-1812-75.pdf) [official] — ⚠️ listed as discontinued by several resellers ([excerpt]) |
| DuPont FilmTec TW30-3012-500 | 500 GPD (1.3 L/min), tolerance +25 / −15 % | **70 psi**, 250 ppm NaCl, 25 °C | 98 % / 96 % | 40 % | 298 mm × 74.9 mm, for 3.0–3.05" housings | [Lenntech PDF](https://www.lenntech.com/Data-sheets/DuPont-FilmTec-TW30-3012-500-L.pdf) [official] |
| Vontron (汇通) ULP1812-75 | 75 GPD | 60 psi, 250 ppm NaCl | 98 % / 96 % | 15 % | — | [Vontron EN product table](https://en.vontron.com/Product/60.html) [official] |
| Vontron ULP3012-400 | 400 GPD | **100 psi**, 250 ppm NaCl | 98.5 % / 96.5 % | 40 % | — | same |
| Vontron ULP3012-600 | 600 GPD (2.27 m³/d) | 100 psi, 250 ppm NaCl | 98 % / 96 % | 50 % | — | same |
| Vontron ULP3012-800 | 800 GPD | 100 psi, 250 ppm NaCl | 97 % / 95 % | 50 % | — | same (⚠️ some rows of this page render garbled; ULP3013 / ULP3113 rows not reproduced) |
| Ovay (澳维) 2012-400 | 400 GPD | **100 psi, 1000 µS/cm GB 34914 test water**, 25 °C | 93 % | 68–70 % | Ø48 × 298 mm, 0.84 m² | [Ovay household catalogue 2026 (PDF)](https://www.ovayhydro.com/wp-content/themes/ovay-membrane/assets/downloads/ovay-household-product-catalog-2026.pdf) [official] |
| Ovay 3012-600 / 3013-600 / 3013-800 | 600 / 600 / 800 GPD | same as above | 93 % | 68–70 % | — | same |
| Ovay 3013-1000 | 1000 GPD | same | 93 % | 68–70 % | Ø68 × 333 mm, 2.2 m² | same |
| Ovay 3213-1200 | 1200 GPD (catalogue: 3.15 L/min) | same | 93 % | 68–70 % | Ø76.5 mm | same |
| Ovay 4013-2000 | 2000 GPD | same | **91 %** | — | — | same |

All three makers state **max 45 °C** feed and **free chlorine < 0.1 ppm** (hence carbon pre-filtration) on the sheets above.

**Takeaways**
- "600G" from a Chinese ULP membrane is rated at **100 psi** with high recovery (68–70 %) and **93 %** rejection on GB 34914 water. The DuPont 500G is rated at 70 psi with 98 %. Expect real output below the label: faucet pressure from a 24 V pump is typically lower than 100 psi, and output drops in cold water.
- One DIY explainer claims output drops "about 5 % per °C colder" ([多环保 duohuanbao](https://www.duohuanbao.com/archives/537371.html)) [post]. ⚠️ Not cross-checked against a manufacturer temperature-correction table.

## 2. What a tankless box actually delivers at the faucet

| Claim | Value | Source / quality |
|---|---|---|
| 400G ≈ 1 L/min, 600G ≈ 1.5 L/min, 800G ≈ 2 L/min | marketing rule of thumb | [知乎 LTE T1 review](https://www.zhihu.com/tardis/bd/art/660539808) — sponsored-style ⚠️ |
| 400G ≈ 1.05 L/min; 75G ≈ 197 mL/min; a 13G tank holds ~5–6 L usable | arithmetic + experience | [duohuanbao](https://www.duohuanbao.com/archives/537371.html) [post] |
| LTE T1 800G: 2.52 L/min, 65 % recovery | vendor claim | [知乎 LTE T1 review](https://www.zhihu.com/tardis/bd/art/660539808) ⚠️ |
| 75G + 3G tank build: 1.5 L kettle filled in 33 s from the tank | measured by builder | [什么值得买 post/a83060p0](https://post.smzdm.com/p/a83060p0/) [post] |

Arithmetic check: 600 GPD = 2271 L/day ÷ 1440 min ≈ **1.58 L/min** at rated conditions, so "1.5 L/min" for 600G is the **best case**, not a typical value.

## 3. Pumps (needed for any tankless 400–800G design)

| Pump | Electrical | Flow / pressure | Source |
|---|---|---|---|
| Lefoo (力夫) LFP600GPD, 24 V DC | working current ≤2.8–3.7 A; max ≤4.0–4.2 A (variant-dependent) | ≥2800–3250 mL/min; bypass 0.85–1.1 MPa | [Lefoo LFP600GPD](https://www.lefoo.com/products/24v-dc-ro-booster-pump-lfp600gpd/), [LFP600GPD-A](https://www.lefoo.com/products/24v-dc-ro-booster-pump-lfp600gpd-a/) [official] |
| Lefoo commercial diaphragm series (LFP300–600G, CN page) | e.g. LFP1600W ≤3.5 A | ≥3200 mL/min, 0.62 MPa; page claims components meet NSF / FDA | [lefoo.cn](https://www.lefoo.cn/products/lfp300-600gshangyongyoushuagemozengyabeng.html) [official] |
| LDW-type 600 GPD brushless pump (EU retailer) | 24 V, 3.6 A; **duty: 12 h on / 30 min rest**, 2000 h life; needs a ≥4 A PSU | ≈3 L/min | [osmounity.de](https://osmounity.de/en/600-GPD-LDW-Brushless-booster-pump/BP-23-102) [shop] |
| 24 V 4.5 A "600 GPD" pump (EU retailer) | 24 V, 4.5 A | 3.8 L/min, 1.9 kg | [wasser-shop24.de](https://www.wasser-shop24.de/products/booster-pumpe-24v-4-5a-12h-600-gpd) [shop] |
| Delta / 三角洲 5-chamber 400–600G pumps | ⚠️ "≤2.5 A, ≥2.6 L/min" for EC-203-400A from a reseller excerpt only | 37 dB claim | trade PR [sohu](https://www.sohu.com/a/405105134_120001238) ⚠️ |

**Implication:** a 600G tankless build needs a **24 V / ≥4 A** supply (≈100 W) for the pump alone, and the pump is the main noise source on the countertop.

## 4. Stale water (陈水) in tankless systems — measured

| Setup | Observation | Fix used | Source |
|---|---|---|---|
| 75G tank build, feed TDS ≈630 | First cups after overnight: **38 / 80 / 70 / 23 / 17 / 15** ppm | Explains the "水驱" (small-tank pure-water flush) principle used by brand machines | [post/a83060p0](https://post.smzdm.com/p/a83060p0/) [post] |
| 600G tankless DIY | First water TDS ≈80 vs ≈10 steady state | NO/NC 科博 valve pair + delay board dumps the first 20 s | [数码之家 thread-523748](https://www.mydigit.cn/thread-523748-1-1.html), [thread-524319](https://www.mydigit.cn/thread-524319-1-1.html) [excerpt] |
| yuunt ESP32 board v2.0, 800G Vontron membrane on a 600G pump | TDS rose to ~60 if water was drawn within 200 s after production stopped | 5 s forward flush, back-flush every 120 s; a small tank is used **only as flush-water source, not for drinking**; T33 post-carbon made optional because of bacterial-colony concerns | [oshwhub yuunt/600g](https://oshwhub.com/yuunt/600g) [official project page] |
| LTE T1 (commercial) | "Zero stale water" by sending permeate back to the membrane inlet | — | [知乎 review](https://www.zhihu.com/tardis/bd/art/660539808) ⚠️ |

So "tankless" in practice still needs either a **first-water dump** (wastes water, needs a drain valve) or a **small pure-water reservoir for flushing**. Without one of these the first glass after idle is noticeably worse.

## 5. Bacteria: tanks and post-carbon are where regrowth shows up

**2019 white paper on secondary microbial contamination of purifiers** (China Household Electrical Appliances Research Institute + 威凯 testing), reported by the China Membrane Industry Association ([membranes.com.cn](https://www.membranes.com.cn/xingyedongtai/gongyexinwen/2019-08-23/37374.html)). Six-month accelerated test, 1800 L throughput, total colony count at the outlet:

| Configuration | Outlet colonies (CFU/mL) |
|---|---|
| Tank + post **carbon block** | 3.3 × 10⁴ |
| Tank + post **granular carbon** | 1.9 × 10⁴ |
| Tankless + post carbon block | 7.1 × 10³ |
| Tankless + post granular carbon | 7.3 × 10² |
| Tap water (reference) | < 1 |

GB 5749-2022 limit for comparison: **100 CFU/mL** (see [water-safety-standards.md](water-safety-standards.md)).
⚠️ Caveats: this is an accelerated lab protocol, not field data. It is an industry press release, and its funding or vendor involvement was not checked. The same article says in post-filter tests **LED-UV performed only "fairly ordinary"**, behind UV mercury lamp (99.84 %) and microporous / hollow-fibre filtration (99.6–99.8 %). The article cites field surveys too: CDC Tianjin reported an **18.8 %** exceedance rate for RO units, and a Fudan Shanghai study found **>50 %** of units over the limit. ⚠️ Those were not traced to the primary papers.

**Field study, Ahvaz (Iran), 6-stage domestic RO with post-carbon and mineral cartridges** ([PMC8172727](https://pmc.ncbi.nlm.nih.gov/articles/PMC8172727/)) [paper]: outlet HPC climbed to about **5500–6000 CFU/mL within a month** of filter change; mean outlet counts (1807 / 3026 CFU/mL) were higher than the inlet (287 / 166).

**Anecdote:** a 6-year-old pressure tank opened by a builder showed only a thin slime ring ([post/a83060p0](https://post.smzdm.com/p/a83060p0/)). This is one case and doesn't count against the measured data.

⚠️ Not read: a 1989 Canadian paper on RO-unit bacterial counts ([cdnsciencepub m89-178](https://cdnsciencepub.com/doi/full/10.1139/m89-178), fetch timed out) and a 2005 CNKI paper ([CNKI](http://en.cnki.com.cn/Article_en/CJFDTOTAL-HJYJ200502022.htm), excerpt only).

## 6. UV-C LED flow-through modules

| Module | Electrical | Flow range | Claimed performance | Physical | Source |
|---|---|---|---|---|---|
| Klaran WR2-24V-2U-B1 (Crystal IS) | 24 V, 8 W typ (4.5–12.5 W) | 0.5–3.8 L/min | 3-log E. coli and 4-log Pseudomonas at 2 L/min, UVT@265 nm ≥95 % | 38 cm³ chamber, 125 g, 104 × 57 mm, 4 kPa drop at 2 L/min, max 100 psi | [Klaran WR2 datasheet 2022](https://cisuvc.com/wp-content/uploads/2024/01/Klaran-WR2-100422.pdf) [official]. **Marked DISCONTINUED** in [2026 datasheet](https://cismaterials.com/wp-content/uploads/2026/07/DS_Reactors_B1_20260325.pdf) |
| Agua Topone EC-12 (Ningbo, CN) | 12 / 24 V, ≤4.8 W, 85 / 115 mW optical | up to 4 L/min | 99.99 % per SGS report under its own conditions; built-in flow switch; 5000 h LED life | 1/4" or 3/8" quick-connect, 1.2 MPa pressure test | [atouvcled.com EC-12](https://atouvcled.com/product/ec-12/) [official] |
| 杰生 JS-M211 (Ma'anshan, CN) | 12 V / 200 mA, 270–280 nm, 80–120 mW | max 6.5 L/min | 99.99 % | — | ⚠️ search excerpt of [datasheet PDF](http://www.jasonsemicon.com/u/705140ae-ce63-4ed7-8b0d-bdd49e92cf0e/file/6377109961715205378766.pdf) only; the download did not complete |

**Independent data on flow vs kill:** US EPA researchers tested flow-through UV-C LED reactors at 265 and 278 nm ([Water 2025, 17, 2965](https://www.mdpi.com/2073-4441/17/20/2965)) [paper]:
- Residence time fell from 3.5 s at 1 L/min to 0.9 s at 4 L/min.
- E. coli: >5-log at 1 L/min, but only >2-log at 4 L/min (at 1/6 power).
- Heterotrophic bacteria at full power and 4 L/min: 2.5–3-log.
- Inactivation is **non-linear in flow**, and 265 nm beat 278 nm on heterotrophic plate counts.

Reference doses: NSF/ANSI 55 Class A = **40 mJ/cm²**, Class B = 16 mJ/cm² ([ANSI blog](https://blog.ansi.org/ansi/nsf-ansi-55-2024-ultraviolet-uv-water-treatment/)). No LED module above publishes an NSF 55 certification. ⚠️

**Implications for UV in this project**
- A dispense-path UV LED sized for **≤2 L/min** fits a 400–600G tankless box. At higher flows the dose drops fast, so keep faucet flow restricted.
- The user's requirement "any tank must have UV" is consistent with the data: tank and post-carbon are the regrowth hotspots. UV **in the tank** (Philips ADD6910 style) and UV **at the outlet** (flow-through, after any post-carbon) address different points. The outlet position protects the last metres of tubing too.
- Because the white paper rates LED-UV only "ordinary", consider pairing UV with **dropping the post-carbon (T33)** or moving it before the tank. The oshwhub board author made T33 optional for the same reason.

## 7. Decision summary

| | Tankless 600–800G | Small tank (3–5 L) + UV |
|---|---|---|
| Size on countertop | Larger membrane housing (3012/3013), bigger pump and PSU | Small 1812 membrane and pump (one 75G build used a 24 V 1.6 A PSU); tank adds volume |
| Instant flow | ≈1–1.5 L/min best case | Fast while tank has water (kettle in 33 s, 75G build) |
| Stale water | Needs flush logic / first-water dump | Tank water is "stale" by design; UV + turnover matter |
| Bacteria (white-paper lab data) | Lower (10²–10³ CFU/mL with post-carbon) | Higher (10⁴ with post-carbon) without disinfection |
| Feeds a heater? | Low flow makes first-cup TDS higher; a tank is suggested for 管线机 ([duohuanbao](https://www.duohuanbao.com/archives/537371.html)) | Better suited |
| Electrical | 24 V ≥4 A | 24 V 1.6 A PSU in one 75G build ([post/a83060p0](https://post.smzdm.com/p/a83060p0/)) |

A hybrid is also documented: tankless high-flux production plus a **small pure-water reservoir used only for membrane flushing**, as on the [yuunt board](https://oshwhub.com/yuunt/600g).
