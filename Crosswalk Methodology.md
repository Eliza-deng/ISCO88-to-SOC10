# Methodology for Cleaning and Validating the ISCO‑88 → SOC‑2010 Crosswalk

This document describes the methodological principles, validation rules, and systematic error corrections applied to the ISCO‑88 to SOC‑2010 crosswalk.
The goal is to produce a research‑grade, conceptually consistent, task‑aligned occupational mapping suitable for empirical labor economics, automation exposure measurement, and cross‑country harmonization.

## Overview
The original ISCO‑88 → SOC‑2010 crosswalk contains numerous structural inconsistencies, including:

- Industry mismatches
- Task-content mismatches
- Supervisor vs. operator level mismatches
- Incorrect mappings caused by overly broad automated matching
- Ambiguous mappings lacking occupational equivalence

This project applies a systematic, rule‑based cleaning procedure combined with line‑by‑line manual semantic review.

## Systematic Error Types Identified
1. Industry Mismatch Errors
These occur when the ISCO occupation and SOC occupation belong to different industries, even if the job titles appear superficially similar.

  Examples
  ISCO 2212 Pharmacologists, pathologists and related professionals  
  → incorrectly mapped to clinical physicians (SOC 29‑1xxx)
  
  Reason:  
  ISCO 2212 refers to life science researchers, not clinical practitioners.
  This is a systematic error in the original crosswalk.

2. Supervisor–Operator Level Mismatches
  A major class of errors arises when ISCO operational occupations (machine operators, assemblers, drivers, cleaners) are    mapped to SOC first‑line supervisors.

  Examples
  ISCO 828x Assemblers → SOC 511011 First‑Line Supervisors of Production Workers
  ISCO 83xx Drivers → SOC 531031 First‑Line Supervisors of Transportation Workers
  ISCO 9333 Freight handlers → SOC 531021 Supervisors of Laborers

  Reason:  
  Supervisory roles involve managerial, scheduling, and oversight tasks absent from ISCO 8xxx and 9xxx occupations.

  Rule:  
  → All supervisor mappings were removed.

3. Task-Content Mismatches
  These errors occur when the ISCO occupation and SOC occupation perform fundamentally different tasks.

  Examples
  Cleaners (ISCO 9132) → Dishwashers (SOC 359021)
  Textile workers (ISCO 826x) → Leather repairers
  Vehicle cleaners (ISCO 9142) → Septic tank servicers (SOC 474071)
  Beverage machine operators (ISCO 8278) → Industrial extruding machine operators (SOC 519041)

  Rule:  
  → Mappings were removed when core tasks did not overlap.

4. Material/Process Mismatches
  These errors arise when the ISCO occupation works with one material (e.g., plastic) but the SOC occupation works with      another (e.g., metal).

  Examples
  ISCO 8232 Plastic‑products machine operators
  → incorrectly mapped to metal machining SOC codes (5140xx)

  Rule:  
  → Plastic ↔ metal mappings were removed unless the SOC explicitly covers both.

5. Weak but Plausible Mappings
  Some mappings are not perfect but share partial overlap in: Work environment, Tools, Physical tasks, General production    processes

  Examples
  Grounds maintenance ↔ farm labor
  Parking attendants ↔ doorkeepers
  Cooling/freezing operators ↔ food processing operators

  Rule:  
  → These mappings were retained but downgraded as "weak".

## Validation Principles
The cleaning process follows a consistent set of rules:

1. Industry Consistency
  ISCO and SOC occupations must belong to the same broad industry
  If industries differ fundamentally, the mapping is removed.

2. Task Equivalence
  Core tasks must align:
  Operating similar machinery
  Performing similar manual labor
  Handling similar materials
  Following similar workflows

  If tasks differ in nature or purpose, the mapping is removed.

3. Skill and Knowledge Alignment
  Occupations must share: Similar technical skills, Similar knowledge domains, and similar work context

  Example:
  Chemical plant operators ↔ chemical equipment operators (strong match)

4. Hierarchical Consistency
  ISCO operational roles cannot map to SOC supervisory roles.

  Rule:  
  → All mappings to SOC 511011, 531031, 531021 were removed.

5. Semantic Review
  Each ISCO–SOC pair was manually reviewed for:
  Occupational definitions
  Task lists
  Industry classification
  Work context
  Required training/skills

## Match Classification
Each ISCO–SOC pair is assigned one of three categories:

| Match Type | Meaning |
| --- | --- |
| **strong** | High task/industry equivalence; retained |
| **weak** | Partial overlap; retained with caution |
| **removed** | Conceptually invalid; deleted |

## Limitations
Some ISCO occupations have no true SOC equivalent
Weak matches should be used cautiously
Crosswalks cannot fully capture country‑specific job content differences
