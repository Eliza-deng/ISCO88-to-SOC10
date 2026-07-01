# ISCO88-to-SOC10
Crosswalk about ISCO88 to SOC10

A fully cleaned, manually validated crosswalk between ISCO-88 4-digit occupations and U.S. SOC 2010 6-digit occupations, created for research on labor markets, automation, and occupational classification harmonization.

This repository contains:
- A cleaned crosswalk dataset
- Documentation of mapping rules
- Notes on error correction and validation
- Methodological principles for constructing international occupation mappings

## Project Overview
This project provides a high-quality ISCO–SOC crosswalk suitable for:
- Labor economics research
- Automation exposure measurement
- Cross-country occupational comparisons
- Harmonizing survey datasets (e.g., CFPS, CPS, ACS, EU-LFS)
- Machine learning models requiring unified occupation codes

## Cleaning & Validation Principles
TThe crosswalk applies a small set of consistent rules to ensure conceptual validity:

Supervisor mappings removed  
ISCO operational roles cannot map to SOC first‑line supervisors.

Industry mismatches removed  
Mappings across unrelated industries (e.g., textile ↔ leather repair) are deleted.

Task‑content mismatches removed  
Occupations must share core tasks and work processes.

Weak but plausible mappings retained  
Partial overlaps are kept but flagged as weak.

Full details are documented in Crosswalk Methodology.


## Dataset Description(isco88_to_soc10_with_labels)
| Column | Description |
| --- | --- |
| ``ISCO_88_code`` | ISCO-88 4-digit occupation code |
| ``ISCO_88_Title_EN`` | ISCO occupation title |
| ``soc_10`` | SOC 2010 6-digit occupation code |
| ``soc_title`` | SOC occupation title |
| ``match_type`` | ``"strong"``, ``"weak"``, or ``"removed"`` |
| ``notes`` | Explanation for weak/removed mappings |

## Citation
If you use this crosswalk in academic work, please cite:
> Kaiyi Deng (2026). ISCO–SOC Crosswalk (Cleaned & Validated). GitHub Repository.

## License
This project is released under the MIT License.
You are free to use, modify, and distribute the dataset with attribution.

## Reference
> Guido Weksler & Facundo Lastra (2022). occupationcross: Package for making crosswalks among different occupational codes. R package version https://doi.org/10.5281/zenodo.7025097
> ILO ISCO correspondence tables：https://www.ilo.org/resource/correspondence-table-isco08-isco88
> BLS SOC crosswalks：https://ibs.org.pl/en/resources/occupation-classifications-crosswalks-from-onet-soc-to-isco/
> IBS O*NET–ISCO resources：https://www.bls.gov/soc/2018/crosswalks.htm
