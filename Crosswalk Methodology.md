# **Crosswalk Methodology**

## **1. Introduction**

This document presents the full methodological framework used to construct, clean, and validate the **ISCO‑88 → SOC‑2010** occupational crosswalk.  
The objective is to produce a conceptually consistent, task‑aligned, and research‑grade mapping suitable for labor economics, automation exposure measurement, and international harmonization.

## **2. Sources and Reference Frameworks**

The crosswalk integrates multiple authoritative sources:

- ILO ISCO‑88 and ISCO‑08 documentation  
- U.S. SOC‑2010 classification  
- O*NET occupational definitions and task lists  
- IBS O*NET–ISCO crosswalk resources  
- BLS SOC correspondence tables  

These sources provide the conceptual foundation for evaluating industry alignment, task equivalence, and hierarchical consistency.

## **3. Systematic Error Types Identified**
### **3.1 Industry Mismatch Errors**
Mappings across fundamentally different industries are removed.

**Examples:**  
- ISCO 2212 Pharmacologists, pathologists → SOC clinical physicians  
- ISCO textile workers → SOC leather repairers  

Industry alignment is evaluated using ISCO/SOC major groups and O*NET work context.

### **3.2 Supervisor–Operator Level Mismatches**
ISCO operational roles cannot map to SOC first‑line supervisors.

**Examples:**  
- ISCO 828x assemblers → SOC 511011 Supervisors of Production Workers  
- ISCO 83xx drivers → SOC 531031 Supervisors of Transportation Workers  

Supervisory tasks (scheduling, oversight, coordination) differ fundamentally from ISCO 8xxx/9xxx operational roles.

### **3.3 Task‑Content Mismatches**
Mappings are removed when core tasks do not overlap.

**Examples:**  
- ISCO cleaners → SOC dishwashers  
- ISCO vehicle cleaners → SOC septic tank servicers  
- ISCO beverage machine operators → SOC industrial extruding machine operators  

Task equivalence is evaluated using O*NET task lists and ISCO descriptions.

### **3.4 Material / Process Mismatches**
Mappings are removed when ISCO and SOC occupations work with different materials or production processes, unless explicitly covered by SOC.

**Examples:**  
- ISCO plastic‑products machine operators → SOC metal machining occupations  


### **3.5 Weak but Plausible Mappings**
Mappings with partial overlap in tools, work environment, or physical tasks are retained but labeled as `weak`.

**Examples:**  
- grounds maintenance ↔ farm labor  
- parking attendants ↔ doorkeepers  
- cooling/freezing operators ↔ food processing  

Weak matches allow researchers to decide whether to include them depending on analytical needs.

## **4. Validation Principles**

### **4.1 Industry Consistency**
ISCO and SOC occupations must belong to the same broad industry:

- chemical ↔ chemical  
- textile ↔ textile  
- food processing ↔ food processing  
- construction ↔ construction  
- transportation ↔ transportation  

### **4.2 Task Equivalence**
Core tasks must align in:

- machinery operated  
- materials handled  
- workflow structure  
- physical or cognitive demands  

Task equivalence is evaluated using O*NET task lists and ISCO descriptions.

### **4.3 Skill and Knowledge Alignment**
Occupations must share similar:

- technical skills  
- knowledge domains  
- work context  

### **4.4 Hierarchical Consistency**
All mappings to SOC supervisory codes (511011, 531031, 531021) are removed.

### **4.5 Semantic Review**
Each ISCO–SOC pair is manually reviewed for:

- occupational definitions  
- task lists  
- industry classification  
- work context  
- required training/skills  

## **5. Match Classification**
Each ISCO–SOC pair is assigned one of three categories:

| Match Type | Meaning |
|-----------|---------|
| **strong** | High task/industry equivalence; retained |
| **weak** | Partial overlap; retained with caution |
| **removed** | Conceptually invalid; deleted |

## **6. Limitations**
- Some ISCO occupations have no true SOC equivalent.  
- Weak matches should be used cautiously.  
- Crosswalks cannot fully capture country‑specific job content differences.  
- Task definitions differ across statistical systems, introducing unavoidable noise.



