# Water-Safety Standards & Home Testing

What "safe" means for the output of a home RO in China, which product standards apply, and what a DIY builder can realistically test at home.

> Evidence key as in [leak-protection.md](leak-protection.md). Pages read 2026-10-18 (UTC+8).

## 1. Drinking-water quality: GB 5749-2022

Selected limits from Table 1 ([FAOLEX copy of GB 5749-2022](https://faolex.fao.org/docs/pdf/chn222304.pdf)) [official text]:

| Parameter | Limit |
|---|---|
| Total coliforms | not detected |
| Heterotrophic plate count (菌落总数) | **≤100 CFU/mL** (500 for small / dispersed supplies) |
| Arsenic | 0.01 mg/L |
| Lead | 0.01 mg/L |
| Nitrate (as N) | 10 mg/L |
| Turbidity | 1 NTU |
| TDS | 1000 mg/L |
| Free chlorine | ≤2 mg/L; ≥0.3 at plant outlet; ≥0.05 at tap |

**Relevance:** measured RO outlets can exceed the 100 CFU/mL HPC limit, especially with tanks and post-carbon ([tank-vs-tankless-uv.md §5](tank-vs-tankless-uv.md)). TDS is a taste/aesthetic parameter here, not a safety one.

## 2. Purifier product standards

### GB 34914-2021 — water efficiency of RO purifiers (mandatory)

From the full text ([renrendoc copy](https://www.renrendoc.com/paper/529272312.html)):

| Grade | Recovery (净水产水率) | Rated total throughput |
|---|---|---|
| Grade 1 | ≥65 % | ≥4000 L |
| Grade 2 | ≥55 % | ≥3000 L |
| Grade 3 (minimum) | ≥45 % | ≥2000 L |

- Required RO removal: hardness ≥90 %, conductivity ≥85 %.
- Test water: 1000 ± 100 µS/cm, hardness 250 mg/L, 25 °C, 0.24 MPa.
- The tank is removed during the test, and flush water counts toward input.
- Units with ≥1 L/min output are tested 8 h on / 16 h off.
- **Out of scope:** units ≥3 L/min, or ≥2 m tall / ≥100 kg.

**Relevance:** Ovay's 68–70 % recovery rating on GB 34914 water ([catalogue](https://www.ovayhydro.com/wp-content/themes/ovay-membrane/assets/downloads/ovay-household-product-catalog-2026.pdf)) is aimed at Grade 1. The 1:3 waste ratio of the 75G DIY build ([post/a83060p0](https://post.smzdm.com/p/a83060p0/)) is about 25 % recovery, below Grade 3. A DIY box isn't legally rated, but this is a useful yardstick.

### GB/T 30307 — household RO purifiers

- GB/T 30307-2013 was replaced by **GB/T 30307-2023**, effective 2024-04-01 ([SAMR listing](https://openstd.samr.gov.cn/bzgk/std/newGbInfo?hcno=313A22C80CC97F7244A8132481B55F1C)).
- The 2013 edition reportedly required ≥85 % rejection and ≥30 % recovery ⚠️ (excerpt). The 2023 content was not read. ⚠️

### Hygiene approval (涉水批件)

Drinking-water treatment products sold in China need a health-safety approval. The 2001 Ministry of Health RO hygiene spec sets removal requirements for specific contaminants (As, Cd, Cr⁶⁺, F, Al, nitrate, CCl₄, CHCl₃) rather than a TDS figure ⚠️ (excerpt). Related NHC notice: [nhc.gov.cn](https://www.nhc.gov.cn/zwgkzt/pwsjd1/201107/52324.shtml).

### US/NSF equivalents

| Standard | What it covers | Source |
|---|---|---|
| NSF/ANSI 58 (RO) | ≥75 % average TDS reduction at 750 mg/L NaCl, 50 psig, in a 7-day test that includes a 2-day stagnation period (captures "TDS creep") | [WCP Online](https://wcponline.com/2021/12/15/tds-reduction-testing-under-nsf-ansi-42-and-nsf-ansi-58/) |
| NSF/ANSI 42 | Aesthetic claims; a TDS claim means ≤500 mg/L output from 1500 mg/L input | same |
| NSF/ANSI 55 | UV systems: Class A 40 mJ/cm², Class B 16 mJ/cm² | [ANSI blog](https://blog.ansi.org/ansi/nsf-ansi-55-2024-ultraviolet-uv-water-treatment/) |
| NSF/ANSI 372 | Lead-free materials, weighted lead ≤0.25 % | [NSF](https://www.nsf.org/knowledge-library/nsf-ansi-can-372-technical-requirements) |
| GB 18145-2014 (CN faucets) | Lead leaching ≤5 µg/L; limits on 17 metals; effective 2014-12-01 | [chinanews](https://www.chinanews.com/gn/2014/06-06/6254481.shtml) |

## 3. Home testing: what works

| Method | What it tells you | Reliability | Source |
|---|---|---|---|
| **TDS pen** | Conductivity only. Good for checking the membrane: output ≤5 % of feed TDS = membrane OK (DIY rule of thumb) | Good for trend; **low TDS ≠ safe**, since bacteria and many organics don't register | [上海科学技术情报研究所 sist.org.cn](https://www.sist.org.cn/fwzl/syaq/zxytz/kpzx/202009/t20200901_2304104.html) (WHO sets no TDS guideline value; <600 mg/L tastes good); rule of thumb from [duohuanbao](https://www.duohuanbao.com/archives/537371.html) |
| Inline dual TDS probes on the controller | Continuous feed vs permeate; detects stale-water spikes and membrane ageing | Same caveat | [oshwhub yuunt board](https://oshwhub.com/yuunt/600g), [VahaC/EspHome-TDS-and-Flow-meter](https://github.com/VahaC/EspHome-TDS-and-Flow-meter) |
| Home test kits | SFPUC evaluation: coliform, nitrate, nitrite and iron kits had **>80 % agreement with the lab**; lead, copper, chlorine and pesticides were mixed; pH, hardness and alkalinity were poor. Bacteria tests take ~48 h | Medium | [SFPUC](https://www.sfpuc.gov/zh-TW/accounts-services/water-quality/understanding-your-tap-water/home-test-kits) |
| **CMA-accredited lab test** | HPC, coliforms, metals per GB 5749 | High; send positives from home kits here | SFPUC page (recommends confirming with a certified lab); CMA = China's lab accreditation mark ⚠️ no specific lab price found |

## 4. Suggested test plan for this build (derived)

1. **At commissioning and each move:** feed and permeate TDS. Expect ≥90–95 % rejection. Log the first-draw TDS after an overnight idle to tune the flush logic ([tank-vs-tankless-uv.md §4](tank-vs-tankless-uv.md)).
2. **One month after commissioning** (the regrowth window seen in the [Ahvaz study](https://pmc.ncbi.nlm.nih.gov/articles/PMC8172727/)): coliform kit + a lab HPC test on first-draw water from the faucet, compared with GB 5749's 100 CFU/mL.
3. **If a tank is used:** the same HPC test on tank water, with UV on and off, to check the UV actually helps.
4. **Faucet:** buy one with a GB 18145 or NSF 372 claim instead of testing for lead at home, since home lead kits were "mixed" in the SFPUC evaluation.
