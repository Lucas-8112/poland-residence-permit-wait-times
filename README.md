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

Offices included so far (data last updated: 22 Oct 2026):
| Office | Letter | Date |
|---|---|---|
| Kujawsko-Pomorski Urząd Wojewódzki (Bydgoszcz) | BW.II.1331.268.2026 | 2026-10-21 |
| Łódzki Urząd Wojewódzki (Łódź) | SOC-IV.1331.14.2026 | 2026-10-16 |
| Lubuski Urząd Wojewódzki (Gorzów Wielkopolski) | SO-IV.1331.23.2026.ESzo | 2026-10-22 |
| Małopolski Urząd Wojewódzki (Kraków) | SC-I.1331.28.2026 | 2026-10-19 |
| Mazowiecki Urząd Wojewódzki (Warsaw) | WSC-IV.1331.30.2026 | 2026-10-16 |
| Opolski Urząd Wojewódzki (Opole) | SO.II.1331.24.2026 | 2026-10-21 |
| Podkarpacki Urząd Wojewódzki (Rzeszów) | O-II.1331.27.2026 | 2026-10-08 |
| Warmińsko-Mazurski Urząd Wojewódzki (Olsztyn) | none (reply by e-mail) | 2026-10-21 |
| Wielkopolski Urząd Wojewódzki (Poznań) | SC-XI.1331.28.2026 | 2026-10-20 |
| Zachodniopomorski Urząd Wojewódzki (Szczecin) | WSC-1.1331.24.2026 | 2026-10-21 |

As of 2026-10-22, 6 offices had not supplied figures: dolnośląskie, lubelskie, podlaskie, pomorskie, śląskie and świętokrzyskie. Some are still within the statutory deadline or have extended it, and others classified the request as "processed information".

## Columns
`office`, `voivodeship`, `case_type` (temporary_residence / permanent_residence / eu_long_term_resident), `period` (`2025` or `2026-01-01/2026-09-30`), `avg_days`, `applications`, `pending_cases`, `pending_scope`, `letter_ref`, `letter_date`, `source_note`.

## Caveats
- **These are the offices' own figures, copied from their letters. They are averages (means), not medians.** No office supplied a median. A few very long cases can raise the average well above a typical applicant's wait.
- Offices calculate the figures differently. Rzeszów averages over all closing decisions: positive, negative, discontinued and left unexamined. Szczecin says its reports do not state which start date the average uses. Wielkopolskie gave approximate values ("około"), and its 2026 period has no stated end date.
- `applications`:
  - Łódź counts persons covered, including family members.
  - Mazowieckie: the header of the applications table in the letter is partially illegible in our copy. The letter text says it lists the number of applications submitted, so we read the figures that way.
  - Opole and Wielkopolskie did not give counts and referred to migracje.gov.pl. Those cells are empty.
- `pending_cases` uses each office's own date and scope (see `pending_scope`):
  - Rzeszów, Opole (approximate) and Bydgoszcz report only one total for all three permit types.
  - Lubuskie counts only cases filed in 2025 and 2026, as of the reply date.
  - Mazowieckie did not report pending cases.
- Some offices also split temporary residence by purpose (work, studies, family). Those splits are not in this CSV yet, but the live tracker shows them.

## Updates
We add new office replies as they arrive. More are expected after 2026-10-21. After that, we plan to request updated figures periodically, roughly every quarter.

## Citation
Expat Essentials Poland, https://app.expatessentials.pl/wait-times. Licensed under CC BY 4.0. See `CITATION.cff`.
