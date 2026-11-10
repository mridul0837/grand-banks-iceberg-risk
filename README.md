# Grand Banks Iceberg Risk

**Ready by March: planning for both quiet and extreme iceberg years at Newfoundland's four offshore oil platforms.**

Team 5's entry for the CPA DnA Case Competition 2026 (October 24–25, 2026). We used historical iceberg sightings and production data to show how Hibernia, Hebron, Terra Nova and SeaRose spot, tow and avoid icebergs, and we built a simple March 31 rule for planning each spring season.

**Tools:** Python (Jupyter) for data cleaning and analysis · Power BI for the dashboard · PowerPoint for the presentation

---

## The question

The number of icebergs that drift onto the Grand Banks changes a lot from year to year. Some years see only a few, and others see well over a thousand. How should the four offshore platforms prepare when they don't know in advance which kind of year is coming?

## Two kinds of platform

| Platform type | Fields | Share of daily oil | Defence against icebergs |
|---|---|---|---|
| Fixed concrete (GBS) | Hibernia, Hebron | **86.85%** (~$14.4M/day) | Can't move. They have to spot icebergs early and tow them away. |
| Floating ship (FPSO) | Terra Nova, SeaRose | **13.15%** (~$2.2M/day) | Can disconnect from the wells and sail away, on a timed countdown. |

Daily values use 2025 production at the 2025 average Brent price ($69.14/bbl).

## Key findings

1. **More icebergs in the ocean doesn't mean more near the rigs.** The extreme year (2014, 1,546 icebergs in the region) had **111** close calls within 50 km. The median year (2012, 499 in the region) had **154**.
2. **Danger near the rigs peaks in April**, one month before the peak of icebergs crossing 48°N.
3. **Platforms share the threat.** On **581** occasions, the same iceberg threatened Hebron and Terra Nova on the same day. The two are 8.2 km apart, and Terra Nova can sail away but Hebron can't.
4. **Towing works, but not every time.** About 22% of tow ropes slip off. Towing still deflects the iceberg 86% of the time, and 99% of tows avoid downtime.
5. **Many icebergs show up late.** Of the **1,555** icebergs that came within 50 km of a platform, **40.6%** had no earlier sighting in the log: their first record was already their closest point. The typical tracking time from first sighting to closest point was 38.3 hours.
6. **Satellites are filling the gap.** Radar satellites, which see through fog and cloud, spotted 13.6% of icebergs in 2021, up from almost none before 2017.
7. **Production held in the extreme year.** In 2014, spring output averaged 225.8K bbl/d, compared with 211.5K bbl/d for the rest of the year. The low point (153.6K bbl/d in August) came from planned maintenance, not ice.

## Recommendation: decide on March 31

On March 31, count the icebergs that have crossed 48°N and choose the response for the spring season:

| Year type | Icebergs past 48°N | Response |
|---|---|---|
| Quiet | fewer than 10 | Share one tracking map and one support vessel. |
| Uncertain | 10–199 | Keep surveillance flights and tow vessels on standby. |
| Extreme | 200+ | Coordinate radar-satellite monitoring and flights, and pool support vessels. |

In every type of year, the four platforms share tracking and vessels, and each platform's Offshore Installation Manager (OIM) keeps the final say on disconnecting.

## Method

- **Data:** the case data pack from the organisers, covering iceberg sightings, platform locations, production and oil prices. The raw data isn't included in this repo.
- **Reference years:** from the 1997–2021 record of icebergs crossing 48°N, we picked a quiet year (2006), a median year (2012) and an extreme year (2014).
- **Close call:** an iceberg sighting within 50 km of a platform.
- **Cleaning:** done in Python, with every data change written down so that each count, join and assumption could be defended.
- **Dashboard:** the cleaned data feeds the Power BI report.

## What's in this repo

| File | What it is |
|---|---|
| [`iceberg-risk-dashboard.pbix`](iceberg-risk-dashboard.pbix) | Power BI dashboard. Open it with [Power BI Desktop](https://www.microsoft.com/power-platform/products/power-bi/desktop), which is free on Windows. |
| [`iceberg-risk-slides.pdf`](iceberg-risk-slides.pdf) | Presentation slides. You can view these right on GitHub. |
| [`iceberg-risk-slides.pptx`](iceberg-risk-slides.pptx) | The same slides as an editable PowerPoint file. |

## Team

This was a team project by Team 5. I'm grateful to my collaborators:

- **Varvara Korotnytska**
- **Mitchell Delaney**
- **Fayez Faruk**

Repo maintained by Rakib Hossain ([@mridul0837](https://github.com/mridul0837)).

---

*This is student competition work. It isn't operational guidance, and we have no connection to the platform operators.*
