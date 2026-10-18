# Leak / Flood Protection

Research for the DIY countertop RO purifier. Scope: concrete leak-protection products and circuits a home builder in mainland China can use, where they sit in the water path, and how they fail.

> Evidence key: **[official]** manufacturer or standards page · **[post]** user build post (什么值得买 / 数码之家 etc.) · **[shop]** retailer listing · **[patent]** patent text · **[excerpt]** seen only as a search-engine excerpt because the page itself could not be fetched (treat as weaker) · ⚠️ = uncertain / not verified.
> All pages were read on 2026-10-18 (UTC+8). No Bilibili, Taobao, or JD logins were used; Taobao item pages redirect to a login wall, so Taobao prices below are search-excerpt-only.

## 1. The three families of protection

| Family | How it works | Needs power? | Where in the water path | Sources |
|---|---|---|---|---|
| **Mechanical swelling leak protector (漏水保护器 / 漏水断路器)** | A dry sponge/cotton puck sits in a small box on the cabinet floor. When it absorbs about **3–5 cc** of water it swells and pushes a spring-loaded plug that blocks the inlet. Reset = dry up, insert a new puck, press down. | No | On the **feed line, right after the angle-valve tee**, before the first housing. The box must sit at the **lowest point** where leaked water collects. | Taiwan retailers [shop]: [麗水](https://www.liwater.com.tw/CON/20938/detail-36a91770-e86e-11ec-8ab6-0309d1b4b0db), [松下淨水生活館](https://www.watershop.com.tw/shop/product/losu3/), [彰鴻](https://www.chwater.com.tw/productsin426.html), [水精靈](https://www.aquawin.com.tw/cht/products/leak-detector-c26410.htm); FAQ by installer [普德 Buder](https://buderwater.com/en/%e6%95%85%e9%9a%9c%e6%8e%92%e9%99%a4-2/) |
| **Probe + normally-closed (NC) inlet solenoid on the RO board** | Two conductive probes on the floor or in a drip tray; the controller cuts the 24 V supply to the NC inlet solenoid (and the pump) when the probes see water. | Yes (24 V) | Probes at the lowest point inside the enclosure or drip tray; the NC solenoid is the **existing inlet solenoid** of the canonical layout. | Survey video 10 in [../videos/README.md](../videos/README.md) (board leak probe stops the machine); open-source boards below |
| **Smart-home water sensor linked to a solenoid** | A wireless water sensor (e.g. Aqara/绿米, Zigbee) triggers a smart plug that powers or unpowers a separate solenoid valve. | Yes (mains + gateway + network) | Separate valve on the feed line; sensor on the cabinet floor. | [什么值得买 post/a5kl5rnk](https://post.smzdm.com/p/a5kl5rnk/) [post] |

There is also a fourth, **built-in** variant in integrated commercial boxes: the LTE/乐天鹅 T1 review says a patented structure "cuts the inlet after about 2 L of leakage" ([知乎 article, sponsored-style review](https://www.zhihu.com/tardis/bd/art/660539808)). ⚠️ Mechanism not described; vendor claim only.

## 2. Concrete parts, specs and prices

### Mechanical protector

| Item | Spec seen | Price seen | Source |
|---|---|---|---|
| 漏水斷路器 (2分 / 3分 versions) | Box 8.5 × 3.3 × 5.0 cm; withstands **10 kg (≈1 MPa)**; trips on ~3–5 cc | NT$249 | [麗水](https://www.liwater.com.tw/CON/20938/detail-36a91770-e86e-11ec-8ab6-0309d1b4b0db) [shop] |
| Same type, 3分 | Same text as above | NT$600 (list NT$800) | [松下淨水生活館](https://www.watershop.com.tw/shop/product/losu3/) [shop] |
| 2分 mechanical protector | "Once the cotton swells it can't be reused; must be in a dry place" | NT$300 | [彰鴻](https://www.chwater.com.tw/productsin426.html) [shop] |
| 水精靈 C-264-10, 3/8" | Quick-connect, double-sided tape mount; sponge replacement costs NT$20–30 | Not listed | [水精靈](https://www.aquawin.com.tw/cht/products/leak-detector-c26410.htm) [shop] |
| Replacement cotton puck | Cotton, ~1–1.8 cm | NT$35 | [水易購](https://www.gaujiuh.tw/product/product&product_id=929) [shop] |
| Mainland Taobao listings (2分/3分 "漏水保护器 膨胀棉") | — | ⚠️ ¥2.8–5.4 per unit, spare cotton from ~¥2.98 | Search-engine excerpt only; item pages need login ([example URL](https://pcdetail.taobao.com/MHp3bFdVUzFFckxuTkN5N2xrVHVRZz09.html)) [excerpt] |

DIY users do install these: 爱董小白 used a **3分 protector** and notes 3分 versions are harder to find than 2分 ([post/a83060p0](https://post.smzdm.com/p/a83060p0/)) [post]. Another 什么值得买 how-to calls it "the first line of defence" and warns that in humid southern China the cotton needs periodic replacement ([post/ak3ld3z8](https://post.smzdm.com/p/ak3ld3z8/)) [excerpt; ⚠️ article style suggests it may be machine-written].

### Electronic protection

| Item | Spec seen | Price seen | Source |
|---|---|---|---|
| Aqara (绿米) water-immersion sensor, Zigbee, two stainless screws as probes; wires can be extended from the screws | — | ¥99 on JD at time of the 2019 post | [post/a5kl5rnk](https://post.smzdm.com/p/a5kl5rnk/) [post] |
| CNKB / 科博 RO solenoids (inlet NC valve, waste combination valve, HP/LP switches) | 24 V NC inlet valve = open when powered, closed when unpowered | — | [科博 solenoid catalogue](https://www.chinakebo.com/product/dcf/) [official]; DIY posts describe 科博 as a first-tier electrical brand at "about ¥10" per part ([post/a83060p0](https://post.smzdm.com/p/a83060p0/)) [post] |
| Normally-open (NO) solenoid | "About 3× the price of a normally-closed valve" | — | [数码之家 thread-523748](https://www.mydigit.cn/thread-523748-1-1.html) [excerpt] |
| Board with built-in leak alarm | A commenter says a DIY "main board with leak alarm" costs about ¥120 | ⚠️ single comment | Comment on [post/a5kl5rnk](https://post.smzdm.com/p/a5kl5rnk/) [post] |

### Open-source controllers that already have the right inputs

| Project | What is useful here | Source |
|---|---|---|
| **yuunt 600–800G zero-stale-water board** (ESP32, GPL-3.0) | Lower board drives 4 solenoids (inlet, waste, back-flush, storage) + 1 pump via MOSFETs (no relays), reads LP switch, tank HP switch, faucet HP switch, flow meter, 2× TDS with NTC. 24 V in. Pairs with an upper ESP32 board. **No dedicated leak input is listed**, but spare GPIO/inputs could be repurposed. ⚠️ | [oshwhub 主控板](https://oshwhub.com/yuunt/600g), [oshwhub 下板](https://oshwhub.com/yuunt/600g-xia-ban) [official project page] |
| **OsmoBuddy** (ESP32-C3, ESPHome) | 4 × 24 V valve outputs (main inlet + flush), 3 pressure transducers, float-switch inputs; the author stresses the **main inlet valve must be a reliable direct-acting valve** because it is the one that must not fail. Reef-aquarium oriented. | [GitHub blueacro/reefvolt-osmobuddy](https://github.com/blueacro/reefvolt-osmobuddy) |
| **BallValveController** (ESP32-C3) | Leak-sensor input forces the valve to its default state **without the home-automation host**; 9 V battery returns the motorised valve to default on power loss. | [GitHub hansrune/BallValveController](https://github.com/hansrune/BallValveController) |
| **Qinyuan (沁园) patent CN200710070531** | Battery-powered leak circuit + **latching** solenoid on the inlet; the sensor sits at the lowest point of the purifier; manual reset button. Shows that a latching valve avoids continuous coil current. | [xjishu patent text](https://www.xjishu.com/zhuanli/40/200710070531.html) [patent] |

## 3. Failure modes (what goes wrong)

1. **Fail-open wiring.** The Aqara build used a **normally-open 220 V valve that is energised to close**. If power, Wi-Fi, gateway or smart plug fails during a leak, nothing closes. A commenter flagged exactly this and recommended NC valves ([post/a5kl5rnk](https://post.smzdm.com/p/a5kl5rnk/)). The counter-argument in the same thread is that NC valves stay powered (coil wear, and "no water during a power cut"). In the RO layout this trade-off doesn't apply: the NC inlet solenoid is already only energised while the machine is producing water.
2. **Single point of failure in the controller.** Probe-based protection only works if the board, PSU and firmware work. The mechanical puck needs no power, so it covers power-loss scenarios. The two are complementary, not alternatives.
3. **Nuisance trips from humidity.** Installers report the puck can pop in a damp cabinet ([Buder FAQ](https://buderwater.com/en/%e6%95%85%e9%9a%9c%e6%8e%92%e9%99%a4-2/)); humid southern climates need more frequent puck replacement ([post/ak3ld3z8](https://post.smzdm.com/p/ak3ld3z8/), excerpt).
4. **Pucks are single-use**: once swollen, they must be replaced ([彰鴻](https://www.chwater.com.tw/productsin426.html)).
5. **Placement.** Water has to reach the sensor. Both the Qinyuan patent and the retailer texts put it at the **lowest point / where water collects**; a leak that sprays outside the cabinet or down the back of the enclosure may never reach it. For an enclosed countertop box, this argues for an **internal drip tray with the probe and puck in it**.
6. **Pressure-tank or housing bursts are faster than any sensor.** Cracked housings and tees are the first leak problem listed in this project's [problems.md](../../problems.md) (items 1–3). Leak protection limits damage; it doesn't replace pressure-rated parts.
7. **Protection only covers the feed line.** If the drain hose pops off the sink tailpiece, concentrate still flows while the pump runs. Probe → board → solenoid **and pump** shutdown covers this case; the mechanical puck on the feed also stops it once it trips.

## 4. Design implications for this project

- **Use both layers:** (a) a **mechanical swelling protector** on the feed line right after the angle-valve tee (cheap, no power, survives a dead PSU); (b) a **floor/drip-tray probe on the controller** that drops the NC inlet solenoid **and the pump**.
- Keep every shut-off **fail-closed**: NC solenoid on the inlet, so loss of 24 V stops water. Avoid smart-plug + NO valve schemes.
- Put the puck box **inside the enclosure's drip tray** (or directly under it on the cabinet floor) so leaks inside the box reach it. Test it with a few cc of water during commissioning.
- Firmware idea (not verified anywhere): latch the leak fault until a manual reset, like the Qinyuan patent does with its reset button.
- Keep spare pucks in the moving kit; they're consumables.
