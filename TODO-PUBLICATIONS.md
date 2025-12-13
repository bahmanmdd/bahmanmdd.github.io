# TODO: Add Full Publication List to Website

## Current Status
- **Currently Showing**: Only 7 journal articles in publications section
- **Archived**: 21 additional publications moved to `content/publications-archive/`

## Full Publication List (30 total)

### Journal Articles (7) - CURRENTLY VISIBLE
1. j2025-av-scenarios - EJTIR 2025
2. j2024-hybrid-dl - ESWA 2024  
3. j2021-multistage - COR 2021
4. j2021-dedicated-networks - JAT 2021
5. j2020-bilevel-evo - CACIE 2020
6. j2020-anchorage - ESWA 2020
7. j2018-subnetworks - CSTP 2018/2019

### PhD Thesis (1) - CURRENTLY VISIBLE
-  phd-thesis-2021

### Conference Papers (7) - ARCHIVED
- c2018-trb - TRB 2018
- c2019-cota - COTA 2019 (Scenario-based infrastructure)
- c2021-its-hamburg - ITS 2021 (Tele-operated driving)
- c2023-ewgt-cav - EWGT 2023 (CAV readiness framework)
- c2023-istdm - ISTDM 2025 (LLM for artifacts) - **NOTE: Check authors!**
- c2023-icasp14 - ICASP14 2023 (Bridge maintenance - Donmez lead)
- c2025-istdm-llm - (duplicate? check this)

### Book Chapter (1) - ARCHIVED
- b2022-tra-chapter - TRA 2026 book chapter

### Technical Reports (7) - ARCHIVED
- r2018-image-assessment
- r2021-5gblueprint  
- r2023-pbl-automation
- r2023-cedr-d1, d2, d3, operations (4 CEDR reports)

### Preprints (2) - ARCHIVED
- p2023-hybrid-dl-arxiv - arXiv preprint (same as published ESWA 2024)
- p2023-teleoperated - arXiv teleoperated driving

### Popular Science (3) - ARCHIVED
- m2023-zra-wegennetwerk - Verkeerskunde
- m2022-teleoperatie-trucks - Logistiek Magazine  
- m2022-impact-teleoperatie - Kenniscentrum DC Logistiek

---

## What We Tried That DIDN'T WORK

### ❌ Attempt 1: Multiple Filtered Collection Blocks on Publications Page
**Tried**: Creating separate collection blocks filtered by publication_type
```yaml
sections:
  - block: collection
    content:
      title: Journal Articles
      filters:
        publication_type: 'article-journal'
  - block: collection
    content:
      title: Conference Papers
      filters:
        publication_type: 'paper-conference'
```
**Problem**: Hugo Blox only showed first 2-3 sections, rest disappeared

### ❌ Attempt 2: Removing "Recent Publications" Section
**Tried**: Removing Recent Publications from homepage to avoid duplication
**Problem**: "See All" button disappeared from Featured Publications

### ❌ Attempt 3: Custom Link Parameters
**Tried**: Adding explicit `link.text` and `link.url` to Featured Publications
**Problem**: Didn't create the "See All" button - template requires Recent Publications section

### ❌ Attempt 4: Changing Featured Count
**Tried**: Setting `count: 4` or `count: 6` to control featured publications
**Problem**: Template always shows exactly 5 featured publications (hardcoded)

---

## Research Needed

Before adding archived publications back, research:

1. **Hugo Blox Tabs/Accordion Blocks**: Can we use tabs to organize by publication type?
2. **Custom Archive Page**: Can we create a separate "All Publications" page with filtering?
3. **BibTeX Import**: Can we use Hugo Blox's native BibTeX import for better organization?
4. **Custom Layout Override**: Can we override the publications layout template?
5. **Separate Pages**: Create individual pages like /publications/conferences/, /publications/reports/?

---

## Critical Issues Fixed

- ✅ ISTDM paper authorship error identified (needs verification of correct authors)
- ✅ All publications have TU Delft Repository PDFs (8 items)
- ✅ All 30 publications documented with correct metadata

---

## Next Steps

1. Keep current simple setup (7 journals + thesis only)
2. Research proper Hugo Blox methods for comprehensive publication lists
3. Test locally before any changes
4. Document what works before implementing
