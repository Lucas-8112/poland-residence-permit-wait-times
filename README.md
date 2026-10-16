---
license: cc-by-4.0
language:
- en
- pl
pretty_name: Poland Residence Permit Wait Times (Official Voivodeship Office Data)
size_categories:
- n<1K
task_categories:
- tabular-classification
tags:
- poland
- immigration
- residence-permit
- karta-pobytu
- government-data
- foia
configs:
- config_name: default
  data_files: poland-residence-permit-wait-times.csv
---

# Poland Residence Permit Wait Times: Official Voivodeship Office Data

Official figures on how long Polish voivodeship offices (urzędy wojewódzkie) take to decide residence-permit cases. The figures cover temporary residence, permanent residence and EU long-term resident permits. Expat Essentials Poland collected them through public-information requests.

- Live tracker: https://app.expatessentials.pl/wait-times
- Publisher: Expat Essentials Poland, https://expatessentials.pl

## Source and method
On 2026-10-07, Expat Essentials Poland sent requests under the Polish Act on Access to Public Information (ustawa o dostępie do informacji publicznej, 6 Sept 2001) to all 16 voivodeship offices. For each permit type, the requests asked for the average time from application to decision in 2025 and in 1 Jan to 30 Sep 2026, the number of applications, and the number of pending cases. Every number in this dataset was copied verbatim from the offices' signed reply letters. Each row cites the letter reference and date.

Offices included so far:
| Office | Letter | Date |
|---|---|---|
| Łódzki Urząd Wojewódzki (Łódź) | SOC-IV.1331.14.2026 | 2026-10-16 |
| Podkarpacki Urząd Wojewódzki (Rzeszów) | O-II.1331.27.2026 | 2026-10-08 |

The other offices had not supplied figures as of 2026-10-16. Some are still within the statutory deadline, and others classified the request as "processed information".

## Columns
`office`, `voivodeship`, `case_type` (temporary_residence / permanent_residence / eu_long_term_resident), `period` (`2025` or `2026-01-01/2026-09-30`), `avg_days`, `applications`, `pending_cases`, `pending_scope`, `letter_ref`, `letter_date`, `source_note`.

## Caveats
- **These are averages (means), not medians.** Neither office supplied a median. A few very long cases can raise the average well above a typical applicant's wait.
- Offices calculate the figures differently. Rzeszów averages over all closing decisions: positive, negative, discontinued and left unexamined. Łódź counts applications as persons covered, including family members.
- Rzeszów reports pending cases only as a single total for all three permit types (7,854 as of 2026-10-08). Łódź reports pending cases per type as of 2026-09-30.
- Neither office splits temporary residence by purpose (work, family, study).

## Updates
We add new office replies as they arrive. More are expected after 2026-10-21. After that, we plan to request updated figures periodically, roughly every quarter.

## Citation
Expat Essentials Poland, https://app.expatessentials.pl/wait-times. Licensed under CC BY 4.0. See `CITATION.cff`.
