# DIY RO Water Purifier — Known Problems (Pre-Research)

A running list of problems people hit when building or living with a DIY RO purifier, collected from Bilibili tutorials & comment sections, 什么值得买 build posts, and open-source BOMs. Each entry notes **where it came from** and **whether a solution was mentioned** at the source.

> Status: pre-research draft. Sources are being expanded; entries will be re-tagged against the agreed analysis dimensions.

## Sources

| ID | Type | Reference |
|----|------|-----------|
| S1 | Bilibili — 1000G DIY build | `BV1oW421X7bA` |
| S2 | Bilibili — "保姆级" full tutorial | `BV1VmkjBCEWd` |
| S3 | Bilibili — 马达师 install videos | `BV1RMakeJE2n`, `BV1uZYveoEEx` |
| S4 | Bilibili — 齐哥净化论 "劝退" video + comments | `BV152421K7KD` |
| S5 | 什么值得买 — build posts | `post/628668`, `post/a83060p0` |
| S6 | Open-source BOM | `magic0whi.github.io/water-purifier` (~¥456.6) |

---

## Problems

### Leaks & flooding
1. **Transparent/plastic filter housings and plastic tees crack and flood.** — Source: S4 (comments), S3. *Solution mentioned:* yes — use metal/quality fittings; add a leak protector (漏水保护器) / auto-shutoff; don't over-tighten.
2. **No unattended flood protection by default.** If a line bursts while you're away, nothing stops the flow. — Source: S4 (comments); user question. *Solution mentioned:* partial — leak protectors and water-stop valves exist; needs dedicated research (open item).
3. **Quick-connect push fittings leak if tube is cut unevenly or not seated.** — Source: S2, S3. *Solution mentioned:* yes — cut square, insert fully, use the lock clips.

### Water safety & quality
4. **Stale water ("陈水") sits in the membrane/line between uses, raising first-draw TDS.** — Source: S4. *Solution mentioned:* yes — flush/zero-stale-water designs, run a few seconds before drinking.
5. **Standing water in a pressure tank breeds bacteria (secondary contamination).** — Source: user concern; S4. *Solution mentioned:* partial — go tankless, or add UV sterilization (needs validation).
6. **Cheap faucets/fittings may leach lead or other metals.** — Source: S4 (comments). *Solution mentioned:* yes — use certified lead-free faucets (304 stainless / food-grade).
7. **Local source water varies; a design that works elsewhere may not suit your water.** — Source: S4. *Solution mentioned:* yes — test local TDS/hardness first, size filtration accordingly.

### Components & matching
8. **Pump and RO membrane must be matched (pressure vs. flux); a mismatch kills output or wastes the membrane.** — Source: S1, S3. *Solution mentioned:* yes — match pump pressure to membrane GPD rating.
9. **Pressure tank is a wear item (bladder fails over time).** — Source: S4. *Solution mentioned:* partial — tankless avoids it; otherwise plan to replace.
10. **High waste-water ratio (clean:waste) wastes water and money.** — Source: S4, S1. *Solution mentioned:* yes — higher-flux membranes and better designs reduce the ratio.
11. **Filter/membrane lifespan is hard to track without instrumentation.** — Source: S5, S6. *Solution mentioned:* partial — control boards with TDS/life monitoring (S6).

### Install & portability
12. **Under-sink installs are fiddly and hard to redo when moving.** — Source: user concern; S3. *Solution mentioned:* partial — angle-valve tee tap-in is quicker; an integrated unit would help (design goal).
13. **Loose-parts rigs (parts screwed to a plate) are bulky and ugly, often hidden in a dirty corner.** — Source: S5, user concern. *Solution mentioned:* partial — enclosed single-box build (design goal, not yet common).
14. **Waste water needs somewhere to drain.** — Source: user question; S3. *Solution mentioned:* yes — route to the sink drain pipe via a saddle/clamp.

### Cost & effort
15. **DIY can cost as much as a cheap finished unit once you buy quality parts.** — Source: S4 ("劝退" angle), S6 (~¥456.6 BOM). *Solution mentioned:* partial — DIY wins on customization/repairability, not always on price.
