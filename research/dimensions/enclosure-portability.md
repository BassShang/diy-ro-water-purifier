# Enclosure & Portability

Goal: one clean-looking box that sits on the counter, connects to the under-sink angle valve with a tee, and can be unplugged and carried to the next rental flat. This page covers reference dimensions of integrated commercial units, how they are built inside, and DIY layout advice.

> Evidence key as in [leak-protection.md](leak-protection.md). Pages read 2026-10-18 (UTC+8).

## 1. Reference sizes of integrated units

| Unit | Type | W × D × H (mm) | Notes | Source |
|---|---|---|---|---|
| Xiaomi 米家 Q600 | Under-sink tankless RO, heater in faucet | **471 × 148 × 406** | Inlet 0.1–0.4 MPa, water ≥4 °C, needs a 220 V outlet and a 25–35 mm faucet hole. PPC cartridge ≤24 months, RO ≤60 months. 30 min flush on new filters. Manual says noise is below the 65 dBA national limit | [Xiaomi Q600 manual](https://cdn.cnbj1.fds.api.mi-img.com/ics-resources/articles/6127661763e068617e0711bb.html) [official] |
| LTE / 乐天鹅 T1 | Semi-DIY "universal" box | **465 × 161 × 410** | Takes standard 10" cartridges in 90° quick-open housings and 1812/3012/3013/3213 membranes. Integrated manifold (水路板). Delta / 柏繁 pump. 800G version claims 2.52 L/min and 65 % recovery. Built-in leak cut-off at ~2 L | [知乎 review](https://www.zhihu.com/tardis/bd/art/660539808) ⚠️ sponsored-style; [ZOL 600G listing](https://detail.zol.com.cn/water-purification-unit/index1980019.shtml) (not fetched) |
| Philips ADD6910 | **Countertop**, no plumbing: user fills a 4 L raw-water tank | **232 × 250 × 424** | 1.5 L pure-water tank with UV-C LED; 2200 W instant heating up to 95 °C; HK$2,316–3,388 | [hkele.com.hk](https://hkele.com.hk/ADD6910) [shop] |
| Haier GR1899 管线机 (heating dispenser fed by an RO) | Wall / counter | 310 × 437 × 72 | 2200 W; see [heating.md](heating.md) | [Haier](https://www.haier.com/xjd/jsj/20200229_116310.shtml) [official] |

Observations
- The two plumbed tankless boxes converge on roughly **47 × 15–16 × 41 cm**, about the size of a large book standing up. That's a realistic target for a countertop DIY box with 3 × 10" pre-filter housings plus a 3012/3013 membrane.
- The Philips is narrower because it has no pre-filter housings or booster-pump train for mains feed. It is a tank-fed design, not plumbed.
- ⚠️ No weights were found for the Q600 or LTE T1 in the sources read.

## 2. What makes integrated units compact and leak-resistant

- **Integrated manifold (水路板)** replaces most tube runs and push-fit joints. DIY posts name "fewer joints" as the main reliability advantage of brand machines ([post/a83060p0](https://post.smzdm.com/p/a83060p0/); [知乎 LTE review](https://www.zhihu.com/tardis/bd/art/660539808)). An off-the-shelf manifold for DIY use wasn't found. ⚠️
- **Quick-turn cartridges**: LTE uses 90° quick-open housings; Q600 uses composite cartridges. Both mean cartridge changes don't need a housing wrench.
- **Leak cut-off is built in** on LTE (see [leak-protection.md](leak-protection.md)).

## 3. DIY layout guidance found

| Topic | Advice | Source |
|---|---|---|
| Mounting style | Builders compare a **hanging back-plate** and a **rack/frame**; use 304 stainless screws | [post/a83060p0](https://post.smzdm.com/p/a83060p0/) [post] |
| Base-plate size | A 400 × 450 mm base board for a 3-stage + RO layout; 3分 (3/8") housings recommended; CCK tubing and 崧泉 housings; total ¥300–800 | [post/ak3ld3z8](https://post.smzdm.com/p/ak3ld3z8/) ⚠️ excerpt; article style suggests machine-written |
| Tubing size | A commenter recommends **3分 (3/8") tubing for the pre-filters at ≥400G**, because 2分 restricts flow | comment on [post/a83060p0](https://post.smzdm.com/p/a83060p0/) [post] |
| Housing material | Transparent first-stage housings burst more easily | [duohuanbao](https://www.duohuanbao.com/archives/537371.html) [post] |
| Angle-valve tee | Copper or stainless, **never zinc alloy** | [duohuanbao](https://www.duohuanbao.com/archives/537371.html); [post/a83060p0](https://post.smzdm.com/p/a83060p0/) |
| Existing frame | One builder reused a commercial machine's shell, frame and tank, and assembled in "about an hour" | [post/a5kl5rnk](https://post.smzdm.com/p/a5kl5rnk/) [post] |
| Auto inlet/drain module for countertop | A Taiwanese countertop RO (Hetta) sells an optional module that auto-fills and drains, so it can be plumbed or used standalone | [futurelab.tw](https://futurelab.tw/products/nouristone-hetta-ro) ⚠️ excerpt only |

Not read: a newsmth 400G tankless DIY thread (HTTP 403).

## 4. Portability checklist (derived; not from a single source)

Each item below follows from facts cited above or in the other dimension pages.

1. **Hose interface**: three quick-connect lines (feed in from the tee, drain out, pure water out to faucet) through one panel. Use John-Guest-style push-fit bulkheads, and cut tubes square ([problems.md](../../problems.md) item 3).
2. **Move procedure**: close the angle valve → depressurise by opening the faucet → disconnect → keep membranes wet. Ovay and DuPont sheets forbid drying and freezing. ⚠️ Membrane storage wording was not quoted in this round; check the datasheet before relying on it.
3. **Inlet pressure range** must be checked at each new flat. The Q600 accepts 0.1–0.4 MPa ([Xiaomi manual](https://cdn.cnbj1.fds.api.mi-img.com/ics-resources/articles/6127661763e068617e0711bb.html)). A Taiwanese installer SOP says to add a reducer above 3 kg/cm² and a pump below 1.5 kg/cm² ([彰鴻](https://www.chwater.com.tw/productsin426.html)).
4. **Drip tray + leak probe + mechanical puck** inside the box ([leak-protection.md](leak-protection.md)).
5. **One mains plug**: a 24 V PSU (≥4 A for a 600G pump, see [tank-vs-tankless-uv.md](tank-vs-tankless-uv.md)). An instant heater would need its own ~10 A mains circuit ([heating.md](heating.md)).
6. **Drain**: a drain saddle on the sink tailpiece; [problems.md](../../problems.md) item 14.
