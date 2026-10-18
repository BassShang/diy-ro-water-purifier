# DIY RO Water Purifier

A personal project to design and build a **countertop reverse-osmosis (RO) direct-drink water purifier** from scratch — one that actually fits how I live.

## Why

I rent and move often, so off-the-shelf purifiers don't quite work for me:

- **Under-sink units** are a pain to install and uninstall every time I move.
- **Countertop units with a manual refill tank** are inconvenient and the standing water tends to breed bacteria.
- Most designs end up hidden in a dark corner and feel dirty.

I want something that **taps directly into the under-sink angle valve**, installs and uninstalls in minutes, has a **simple structure with minimal maintenance**, and is clean enough to leave out in the open.

## Goals

- **Portable** — easy to disconnect and take along when moving.
- **Direct-connect** — hooks into the existing water line via a tee/angle valve, no manual refilling.
- **Safe to drink** — RO filtration; any stored water must be protected (e.g. UV sterilization); claims backed by standards (GB 5749) and filter specs, not guesses.
- **Low maintenance** — simple, few consumables, minimal water changes.
- **Open design option** — possibly packaged as a single enclosed unit instead of loose parts.

## Open Questions

- Tankless (direct-flow) vs. small tank with UV sterilization?
- Add post-heating (instant hot/warm water) like a Philips unit, or keep it cold-only?
- Enclosed single-box build vs. open rack/mounting plate?

## Approach

Before committing to a design, we're first defining the **analysis dimensions** used to evaluate existing DIY builds and their trade-offs, then surveying real-world builds against those dimensions.

### Analysis Dimensions (draft)

**Structure / water path**
- Number of filter stages (PP, UDF granular carbon, CTO carbon block, RO, post-carbon T33)
- RO membrane flux (e.g. 400G / 600G / 1000G)
- Tank vs. tankless (pressure tank)
- Post-activated-carbon stage (taste polishing)
- Water intake (angle valve / faucet vs. manual tank)

**Water safety**
- UV sterilization
- Stored water / secondary contamination risk
- Faucet & fitting materials (lead leaching)
- Waste ratio and stale-water flushing

**Portability / maintenance**
- Degree of integration (loose parts on a plate vs. single enclosed box)
- Install/uninstall difficulty when moving
- Filter-change / maintenance frequency

**Heating**
- Heating: none / instant / storage

**Smart / electronics**
- Control board, TDS monitoring, IoT, leak protection

**Frame / enclosure**
- Open mounting plate / stainless rack / closed enclosure

**Cost**

## Status

Early exploration. Collecting and analyzing real DIY builds (video tutorials, build posts, BOMs) and documenting common pitfalls and their solutions.

## Research

- [Bilibili 「DIY净水器」 video survey: architecture index](research/videos/README.md)
- [Design-dimension research: leak protection, tank vs tankless + UV, enclosure, heating, parts, standards](research/dimensions/README.md)
