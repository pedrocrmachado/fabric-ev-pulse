# fabric-ev-pulse

**Europe's EV charging gap & network expansion opportunities** — an end-to-end
Microsoft Fabric analytics engineering project.

> **Status:** In active development. Built as a portfolio project demonstrating
> a realistic analytics engineering workflow on Microsoft Fabric.

## The business question
Where is EV adoption outpacing charging infrastructure across Europe, and which
markets are the strongest expansion opportunities for a charging network operator?

## Headline KPIs
- **EVs on the road per public charge point**, by country (infrastructure strain)
- **Expansion opportunity rank** — high adoption + thin charging = top targets
- **Operator market share** & **fast-charge (≥50 kW) share**, by country

## Architecture
Medallion (Bronze → Silver → Gold) on a Fabric Lakehouse + OneLake, served through
a semantic model into Power BI.

`[architecture diagram coming in /assets]`

## Tech stack
Microsoft Fabric · OneLake · Lakehouse · Delta tables · Data Factory Pipelines ·
PySpark Notebooks · SQL · Semantic Model · Power BI

## Data sources
| Source | Description | License |
|---|---|---|
| [Open Charge Map API](https://openchargemap.org) | Public EV charging stations | OCM data licence (attribution) |
| [IEA Global EV Data Explorer](https://www.iea.org/data-and-statistics/data-tools/global-ev-data-explorer) | EV sales/stock by country & year | CC BY 4.0 |

## Known limitations
- Open Charge Map is a **current snapshot**; IEA adoption is an **annual series**.
  The headline ratio compares latest IEA stock against current charge-point counts.
  See `/docs/architecture.md` for full assumptions.

## Repo structure
See folders above. Notebooks are exported from Fabric for reviewability.

---
*Author: Pedro Machado & Hugo Pereira· Built 2026*
