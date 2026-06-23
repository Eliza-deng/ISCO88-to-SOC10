# ISCO88-to-SOC10
Crosswalk about ISCO88 to SOC10

A fully cleaned, manually validated crosswalk between ISCO-08 4-digit occupations and U.S. SOC 2018 6-digit occupations, created for research on labor markets, automation, and occupational classification harmonization.

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
This project applies a consistent set of rules to remove or downgrade incorrect mappings.

1. Supervisor mappings removed
All mappings from ISCO operational occupations to SOC supervisory occupations were deleted.

Examples:
ISCO 828x → SOC 511011
ISCO 83xx → SOC 531031

Reason: Supervisory roles represent different job content and skill levels.

2. Industry mismatch mappings removed
Mappings where the ISCO occupation and SOC occupation belong to different industries were deleted.

Examples:
Glass makers → Floral designers
Textile workers → Leather repairers
Vehicle cleaners → Septic tank servicers

3. Task mismatch mappings removed
Mappings where tasks differ fundamentally (e.g., food prep vs cleaning) were removed.

Examples:
Office cleaners → Dishwashers
Street vendors → Food servers (nonrestaurant)

4. Weak but plausible mappings downgraded
Mappings with partial overlap were kept but flagged as low confidence.

Examples:
Grounds maintenance ↔ farm labor
Parking attendants ↔ doorkeepers
Cooling/freezing operators ↔ food processing

## Dataset Description(isco88_to_soc10_with_labels)
| Column | Description |
| --- | --- |
| ``ISCO_88_code`` | ISCO-88 4-digit occupation code |
| ``ISCO_88_Title_EN`` | ISCO occupation title |
| ``soc_10`` | SOC 2018 6-digit occupation code |
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
> https://www.ilo.org/resource/correspondence-table-isco08-isco88
