# karta-pobytu-wait-times

Open data: how long Polish voivodeship offices take to decide residence-permit (karta pobytu) applications, **according to the offices' own written replies** to public-information requests by [Expat Essentials Poland](https://expatessentials.pl/).

**Edition:** November 2026 · **Offices with data:** 10 of 16 · **Periods:** decisions issued in 2025 and 1 Jan–30 Sep 2026 · **Licence:** [CC BY 4.0](LICENSE)

## Headline (temporary residence, average days to decision)
| Office | 2025 | 2026 (Jan–Sep) | Change |
|---|---|---|---|
| Kraków | 183 | 250 | +67 (+36.6%) |
| Olsztyn | 211 | 279 | +68 (+32.2%) |
| Rzeszów | 246 | 314 | +68 (+27.6%) |
| Poznań* | 340 | 340 | 0 |
| Łódź | 324 | 384 | +60 (+18.5%) |
| Warsaw | 271 | 429 | +158 (+58.3%) |
| Szczecin | 466 | 462 | −4 (−0.9%) |
| Opole | 604 | 498 | −106 (−17.5%) |
| Gorzów Wlkp. | 494 | 518 | +24 (+4.9%) |
| Bydgoszcz | 545 | 539 | −6 (−1.1%) |

\*Poznań gave approximate values. No figures yet: Białystok, Gdańsk, Katowice, Kielce, Lublin, Wrocław.

## Files
- `data/karta_pobytu_wait_times_by_office.csv` – 16 rows, one per voivodeship
- `data/karta_pobytu_wait_times_long.csv` – 153 rows, one per figure in a letter
- `data/karta_pobytu_wait_times.json` – both, plus metadata

Column definitions and limitations: see the dataset card (`README.md` in the Hugging Face version) and the report: https://expatessentials.pl/karta-pobytu-waiting-times-november-2026-report/ (EN) · https://expatessentials.pl/uk/terminy-karty-pobytu-lystopad-2026-zvit/ (UK).

## Method
Identical requests under the Polish Access to Public Information Act were sent to all 16 offices on 7 Oct 2026. Figures were copied exactly from the replies (8–22 Oct 2026). Nothing is estimated or interpolated.

## Cite
Expat Essentials Poland (2026). *Karta pobytu waiting times in Poland by voivodeship office, November 2026.* CC BY 4.0. https://expatessentials.pl/

Corrections and new office replies: hello@expatessentials.pl
