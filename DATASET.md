---
license: cc-by-4.0
language:
- en
- pl
pretty_name: Karta pobytu waiting times in Poland by voivodeship office (November 2026)
size_categories:
- n<1K
tags:
- poland
- immigration
- residence-permit
- karta-pobytu
- public-sector
- open-government-data
configs:
- config_name: by_office
  data_files: karta_pobytu_wait_times_by_office.csv
- config_name: long
  data_files: karta_pobytu_wait_times_long.csv
---

# Karta pobytu waiting times in Poland by voivodeship office (November 2026)

Average processing times for residence permits (temporary residence, permanent residence, EU long-term resident), as reported **by the voivodeship offices themselves** in written replies to public-information requests sent by Expat Essentials Poland on 7 October 2026.

- **Publisher:** Expat Essentials Poland, https://expatessentials.pl/
- **Licence:** CC BY 4.0
- **Coverage:** 16 offices asked; 10 replied with figures (Bydgoszcz, Gorzów Wielkopolski, Kraków, Łódź, Olsztyn, Opole, Poznań, Rzeszów, Szczecin, Warsaw). Six offices (Białystok, Gdańsk, Katowice, Kielce, Lublin, Wrocław) have no figures in this edition.
- **Reference periods:** decisions issued in 2025; decisions issued 1 Jan–30 Sep 2026.
- **Source letters dated:** 8–22 October 2026.

## Files
| File | Rows | Description |
|---|---|---|
| `karta_pobytu_wait_times_by_office.csv` | 16 | One row per voivodeship; headline averages (temporary, permanent, EU long-term), change 2025→2026, pending temporary-residence cases, letter reference and request status. |
| `karta_pobytu_wait_times_long.csv` | 153 | One row per figure stated in a letter (average days, applications filed, persons covered, cases pending), by permit type and period, with the original Polish labels and notes. |
| `karta_pobytu_wait_times.json` | — | Both tables plus metadata and caveats. |

## Key columns (long file)
`voivodeship, office_city, office, letter_ref, letter_date, metric, permit_type, period, value, unit, approximate, original_metric_pl, original_permit_pl, original_period_pl, notes_pl`

- `metric`: `avg_days_to_decision`, `applications_filed`, `persons_covered_by_applications` (Łódź counts persons incl. family members), `cases_pending`.
- `permit_type`: `temporary_residence_all`, `temporary_residence_work`, `temporary_residence_studies`, `temporary_residence_family`, `temporary_residence_family_of_polish_citizen`, `permanent_residence`, `eu_long_term_resident`, `all_permit_types`.
- `period`: `decisions_2025`, `decisions_2026-01-01_to_2026-09-30`, `2025`, `2026-01-01_to_2026-09-30`, `as_of_YYYY-MM-DD`.

## Limitations
- Values are **averages of finished cases as stated by each office**, not medians and not forecasts.
- Offices compute averages differently (e.g. Rzeszów includes refusals, discontinued cases and cases left without consideration; Szczecin states its reports do not define the start date of the count).
- Poznań reported approximate values (`approximate = true`).
- Pending-case counts have different dates and scopes; do not sum them.
- 2026 covers nine months only. Ten of sixteen offices is not a national picture.
- No estimates, media figures or crowd-sourced reports are included. Empty cells mean the office did not provide the figure.

## Citation
> Expat Essentials Poland (2026). *Karta pobytu waiting times in Poland by voivodeship office, November 2026.* Data from voivodeship offices' replies to public-information requests. CC BY 4.0. https://expatessentials.pl/

## Updates
Next edition planned for early December 2026 if more offices reply. Corrections: hello@expatessentials.pl
