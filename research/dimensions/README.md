# Design-Dimension Research — Index & Key Takeaways

Non-Bilibili research (official datasheets, standards, papers, 什么值得买 / 数码之家 / 知乎 build posts, open-source projects) on the six dimensions that drive the design of a **portable, countertop, angle-valve-fed DIY RO purifier**. It complements the [Bilibili video survey](../videos/README.md) and [problems.md](../../problems.md).

Every fact on the dimension pages links to its source. ⚠️ marks anything uncertain, sponsored-looking, or seen only as a search excerpt. Read 2026-10-18 (UTC+8).

| Dimension | Page |
|---|---|
| Leak / flood protection | [leak-protection.md](leak-protection.md) |
| Tankless high-flux vs small tank + UV | [tank-vs-tankless-uv.md](tank-vs-tankless-uv.md) |
| Enclosure & portability | [enclosure-portability.md](enclosure-portability.md) |
| Instant post-heating | [heating.md](heating.md) |
| Core-part brands & prices | [brands-parts.md](brands-parts.md) |
| Water-safety standards & home testing | [water-safety-standards.md](water-safety-standards.md) |

## Key takeaways

1. **Bacteria regrow after the membrane, mostly in tanks and post-carbon.** In a 2019 accelerated test, tank + post carbon block reached 3.3 × 10⁴ CFU/mL, while tankless + granular carbon reached 7.3 × 10² CFU/mL. Both are above GB 5749's 100 CFU/mL; tap water was <1 ([membranes.com.cn](https://www.membranes.com.cn/xingyedongtai/gongyexinwen/2019-08-23/37374.html)). A field study saw outlet HPC reach ~5500–6000 CFU/mL within a month ([PMC8172727](https://pmc.ncbi.nlm.nih.gov/articles/PMC8172727/)).
2. **UV-C LED works, but only at modest flow.** EPA data: E. coli >5-log at 1 L/min vs >2-log at 4 L/min, and 265 nm beats 278 nm ([MDPI Water 2025](https://www.mdpi.com/2073-4441/17/20/2965)). Off-the-shelf modules are rated 0.5–4 L/min, e.g. [Klaran WR2](https://cisuvc.com/wp-content/uploads/2024/01/Klaran-WR2-100422.pdf) (now discontinued) and [EC-12](https://atouvcled.com/product/ec-12/).
3. **Membrane "G" ratings aren't comparable across makers.** Chinese ULP 600G is rated at 100 psi, 93 % rejection, 68–70 % recovery ([Ovay](https://www.ovayhydro.com/wp-content/themes/ovay-membrane/assets/downloads/ovay-household-product-catalog-2026.pdf)). DuPont 500G is rated at 70 psi with 98 % ([TW30-3012-500](https://www.lenntech.com/Data-sheets/DuPont-FilmTec-TW30-3012-500-L.pdf)). 600 GPD ≈ 1.58 L/min is the ceiling, not typical faucet flow.
4. **Tankless still needs flush logic.** Measured first-draw TDS was ~60–80 vs ~10 steady. The fixes used are a timed first-water dump or a small pure-water reservoir used only for back-flush ([oshwhub yuunt/600g](https://oshwhub.com/yuunt/600g), [数码之家](https://www.mydigit.cn/thread-523748-1-1.html)).
5. **Leak protection should be two independent layers, both fail-closed.** A mechanical swelling puck on the feed (no power; trips at ~3–5 cc) plus a probe on the controller that drops the NC inlet solenoid and the pump. A smart-home build using an energise-to-close NO valve was criticised for failing open on power loss ([smzdm a5kl5rnk](https://post.smzdm.com/p/a5kl5rnk/)).
6. **Instant heating is a separate 220 V product class.** 2200 W gives ≈0.42 L/min at ≥90 °C ([Haier GR1899](https://www.haier.com/xjd/jsj/20200229_116310.shtml): 25 L/h). Thick-film dispenser modules are often rated **≤0.05 MPa** and TDS <60 ppm ([Gida](http://www.gi-da.com/product/7_37)), so they belong after a tank or pump, not inline on the RO line.
7. **Target envelope ≈ 47 × 15–16 × 41 cm.** That is the size of the Xiaomi Q600 and LTE T1 integrated tankless boxes ([Xiaomi manual](https://cdn.cnbj1.fds.api.mi-img.com/ics-resources/articles/6127661763e068617e0711bb.html); [LTE review ⚠️](https://www.zhihu.com/tardis/bd/art/660539808)). Their compactness and reliability come from an integrated manifold that cuts out most joints.
8. **Electrical sizing:** a 600G pump draws ~3–4 A at 24 V, so use a PSU of at least 4 A ([Lefoo](https://www.lefoo.com/products/24v-dc-ro-booster-pump-lfp600gpd/); [osmounity](https://osmounity.de/en/600-GPD-LDW-Brushless-booster-pump/BP-23-102)). A 75G build ran on 24 V 1.6 A ([smzdm a83060p0](https://post.smzdm.com/p/a83060p0/)).
9. **A TDS pen checks the membrane, not safety.** Use coliform kits (>80 % agreement with lab in the [SFPUC evaluation](https://www.sfpuc.gov/zh-TW/accounts-services/water-quality/understanding-your-tap-water/home-test-kits)) and a lab HPC test against GB 5749.

## Design implications (proposed, for discussion)

| Requirement | Implication |
|---|---|
| Portable / renter | One box, three quick-connect lines (feed, drain, pure) on one panel. Copper or stainless angle-valve tee. Keep the membrane wet between moves. Check inlet pressure (0.1–0.4 MPa class) at each flat. |
| Easy install & uninstall | Mechanical leak puck and tee travel with the box. No permanent plumbing beyond the tee and a drain saddle. |
| Minimal maintenance | Standard 10" cartridges in quick-turn housings. Consider dropping post-carbon (T33), since it is a regrowth hotspot. Inline dual TDS for membrane health. |
| Tank must have UV | If a tank is used: UV in the tank **and/or** a flow-through UV at the outlet, sized ≤2 L/min. Tankless 400–600G with flush logic plus outlet UV is the lower-bacteria baseline. |
| Instant heating | Phase 2 / separate module. Lowest risk: feed a certified 管线机. DIY: small UV tank → low-pressure pump → thick-film module with built-in dry-fire protection, on its own mains circuit. |
| Leak safety | Mechanical puck + controller probe in an internal drip tray. NC inlet solenoid. Latch faults until manual reset. |
| Clean look | Enclosure ≈ 47 × 16 × 41 cm. Opaque housings. Hide the pump; it is the main noise source. |
| China parts | Vontron / Ovay membrane, Lefoo / Delta pump, 科博 electrics, 崧泉 housings, CCK tubing (see [brands-parts.md](brands-parts.md)). |

## Not verified in this round

- Mainland retail prices (Taobao and JD need login; no sign-in was used). A few prices are from excerpts or older builder posts.
- 杰生 JS-M211 UV module datasheet (download failed; specs from excerpt). Delta EC-203 pump specs (excerpt only).
- Primary papers behind the Tianjin CDC 18.8 % and Fudan >50 % exceedance figures. 1989 Canadian paper (timeout) and 2005 CNKI paper (excerpt only).
- GB/T 30307-2023 content. Scope of GB/T 4706.19-2024 for instant dispensers.
- LTE T1 specs come from a sponsored-style review. No weights found for integrated units.
- newsmth 400G tankless thread (403). Bilibili was not accessed at all for this page.
