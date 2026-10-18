# Instant Post-Heating

Can the DIY box offer near-boiling water like the user's Philips unit? This page covers which heater types exist, their real flow at a given power, pressure limits, dry-fire protection, and safety standards.

> Evidence key as in [leak-protection.md](leak-protection.md). Pages read 2026-10-18 (UTC+8).

## 1. Physics first: 2200 W gives about 0.4 L/min of near-boiling water

Heating water from ~20 °C to ~95 °C (ΔT ≈ 75 K):
`2200 W ÷ (4186 J/(kg·K) × 75 K) ≈ 0.007 kg/s ≈ 0.42 L/min ≈ 25 L/h` (ideal, no losses; calculation, not a source quote).

This matches published specs:

| Product | Power | Hot output | Pressure | Other | Source |
|---|---|---|---|---|---|
| Haier GR1899 管线机 | 2200 W | **≥90 °C at 25 L/h** (≈0.42 L/min) | inlet **0.1–0.4 MPa** (mains-pressure feed) | quartz-tube heater; 310 × 437 × 72 mm | [Haier](https://www.haier.com/xjd/jsj/20200229_116310.shtml) [official] |
| 米阳 Miyoung MGX-1012 管线机 | 2200 W | 20 L/h | — | ¥980 list price | [miyoung.com.cn](http://www.miyoung.com.cn/product/proshow_213.html) [official] |
| Philips ADD6910 | 2200 W | up to 95 °C | tank-fed | 1.5 L UV-C pure tank | [hkele.com.hk](https://hkele.com.hk/ADD6910) [shop] |
| Xiaomi Q600 | — ⚠️ heater power not noted | max 95 ± 2 °C | 0.1–0.4 MPa system | Heater inside the faucet; hot path is flow-limited. On first use the first 60 s is unheated, and 5 s after each power-up. Child lock for ≥50 °C. The manual says recovery ratings don't apply to hot water | [Xiaomi Q600 manual](https://cdn.cnbj1.fds.api.mi-img.com/ics-resources/articles/6127661763e068617e0711bb.html) [official] |

So **hot output is about 1/3 to 1/4 of a 600G RO's cold output**, and the heater (not the RO) sets the hot-water rate. 2200 W at 220 V is **≈10 A**. Check that the kitchen outlet and plug are rated for it continuously. ⚠️ This is a calculation; no outlet rating was checked for a specific rental.

## 2. Heater types

Gida (吉达) compares quartz-tube, PTC/MCH ceramic and thick-film heaters for instant water ([gi-da.com news/16_153](http://gi-da.com/news/16_153)) [official, vendor]. Thick film is the type it sells for instant dispensers. A 知乎 净热一体 (purify + heat) buyer's guide also recommends thick film ([知乎](https://www.zhihu.com/tardis/bd/art/646512417)) ⚠️ marketing. The same guide recommends ≥800G, BPA-free parts, no scale-inhibitor cartridge, and heat sterilisation over UV.

### Example DIY-purchasable module — Gida "20 thick-film module"

From [gi-da.com product/7_37](http://www.gi-da.com/product/7_37) [official]:

| Parameter | Value |
|---|---|
| Supply | 220 V |
| Power | 2100 W rated (2200 W at 45 °C inlet) |
| **Rated pressure** | **≤0.05 MPa** → for gravity/pump-fed dispensers, **not** for mains/RO-line pressure |
| Feed water | TDS **<60 ppm**, hardness <4°, 5–38 °C |
| First hot water | 3–6 s |
| Protections | no-water, freezing, over-temperature, dry-fire; error E1 at 103 °C |
| Leakage current | ≤0.25 mA |
| Life | ≥500 h at 0 bar |
| Size | 280 × 180 × 125 mm |

**Implication:** the low-pressure rating means this class of module must sit **after a tank or a dispensing pump**, not inline on the pressurised RO output. The TDS limit means it should only ever see RO water. A 知乎 Q&A says the same: feed a 管线机 RO water only ([知乎 answer](https://www.zhihu.com/tardis/jm/ans/2038705049367475621), ⚠️ excerpt). A mains-pressure heater like the Haier GR1899 (0.1–0.4 MPa) is a different, pressure-rated product.

## 3. Dry-fire / safety logic used by heater makers

Jaye (嘉业) describes these anti-dry-burn strategies for thick-film heaters ([jaye-heater.com](https://cn.jaye-heater.com/info/anti-dry-burning-strategy-of-thick-film-heater-74876429.html)) [official, vendor]:
1. **Flow meter**: no flow, no power.
2. **NTC rate check**: e.g. if the reading jumps too fast, or doesn't reach about 60 °C within 5 s, assume dry and cut off.
3. **Outlet over-temperature cut** at about 103–105 °C.
4. **Surface thermistor / thermal fuse** on the heating film.

The Xiaomi Q600 manual's "first 60 s unheated" and "5 s after power-up" behaviour looks like the same idea: confirm flow before heating ([manual](https://cdn.cnbj1.fds.api.mi-img.com/ics-resources/articles/6127661763e068617e0711bb.html)). ⚠️ That is our interpretation; the manual doesn't state the reason.

## 4. Standards

- **GB/T 4706.19-2024** (household appliance safety, particular requirements for liquid heaters) replaces GB 4706.19-2008, effective **2026-08-01** per the SAMR listing ([openstd.samr.gov.cn](https://openstd.samr.gov.cn/bzgk/std/newGbInfo?hcno=99D6FFCB80ADF44B192FD0C98654BE8A)). ⚠️ Its exact scope for instant-heat dispensers wasn't read. Group standards T/CAS 831-2024 and T/DZJN 07-2019 also cover instant-heat drinking-water appliances ⚠️ (titles from search excerpts only).
- Patents for hot-water sterilisation of the faucet or line exist, e.g. a steam-sterilising faucet ([xjishu 202310086312](https://www.xjishu.com/zhuanli/40/202310086312.html)) and hot-water flushing ([xjishu 202410158372](https://www.xjishu.com/zhuanli/11/202410158372.html), excerpt). ⚠️ Applicants were not checked.

## 5. Tank vs tankless for feeding a heater

A DIY guide says a tank suits a 管线机 better, because tankless flow is small and first-cup TDS is high ([duohuanbao](https://www.duohuanbao.com/archives/537371.html)) [post]. Combined with the ≤0.05 MPa rating of thick-film dispenser modules, the **Philips-style architecture** is the one that matches the parts: RO → small UV tank → low-pressure pump → thick-film heater → outlet.

## 6. Design implications

- Treat heating as a **separate 220 V module** with its own fusing, earth, leakage protection and dry-fire logic. Keep it physically and electrically apart from the 24 V RO controller.
- **Lowest-risk option:** buy a certified 管线机 / instant dispenser (e.g. Haier GR1899 class, 0.1–0.4 MPa, 2200 W) and feed it from the DIY RO. **DIY option:** a small UV tank + low-pressure pump + thick-film module with built-in protections (e.g. the Gida module), never inline on the pressurised RO line.
- Expect ~0.35–0.42 L/min hot at 2200 W. Fine for a cup or a kettle-sized pour; not a bulk-fill tap.
