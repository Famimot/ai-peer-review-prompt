# Prompt for AI Review

**Version:** 51 - 61 (250326.51 - 260417.61)  
**Author:** Kravtsov G.G.  
**AI Model:** DeepSeek  
**Languages:** Russian / English

## Description

A universal prompt for preliminary peer review of scientific manuscripts. Implements a 100-point weighted metric (Novelty 30%, Methodology 25%, Practical Value 20%, Visualization 15%, Ethics 10%) with differentiation of novelty types (I/P-Novelty) and mandatory contextual calibration on the article array.

## Usage

1. Create a new dialogue in DeepSeek
2. Copy the prompt text from the file `Universal_AI_Review_Prompt_v_51_EN.txt`
3. Submit it to the AI along with the manuscript(s) for review
4. The AI will generate a structured review according to the algorithm

**Estimated execution time:** 1.5–2 minutes for 4 average-sized articles.

## Data Availability

All materials for reproducing the results are publicly available:

### Prompts
- `Universal_AI_Review_Prompt_v_51_RU.txt` — calibrated version (Russian)
- `Universal_AI_Review_Prompt_v_51_EN.txt` — calibrated version (English)
- `Simple_AI_Review_Prompt_RU.txt` — simple uncalibrated prompt (for reference)

### Validation Data
- `validation/Supplementary_Validation_Data.xlsx` — method validation (10 runs of simple and calibrated prompts)
- Analyzed article: https://doi.org/10.5281/zenodo.19275632

### Example
- `DEMO_AMIS_peer_review_4_papers_2026_RU.doc` — example AI review (https://doi.org/10.5281/zenodo.19275632)

### History of Changes (Changelog)

## 260327 
### Subprompts
- `subprompts/` — modular prompts for analyzing individual sections (title, abstract, introduction, etc.)

## 260417
**Added: modified prompt, source materials for scientific journal ranking:**
- New prompt version: `Universal_AI_Review_Prompt_v_61_RU.txt` and `Universal_AI_Review_Prompt_v_61_EN.txt`.
- Folder for initial run: `journal_ranking_data/raw_runs/`.
- Initial run files for 5 journal articles: `J1`, `J2`, `J3`, `J4`, `J5`.
- Folder for aggregated results (10 runs): `journal_ranking_data/aggregated/`.
  - `Top 5 articles.xlsx` — strongest articles (top 5 by total score)
  - `5_median_articles.xlsx` — median articles (5 articles with average scores)
  - `5 weakest articles.xlsx` — weakest articles (bottom 5 by total score)
  - `Final journal ranking.xlsx` — final journal ranking (summary result)
- "History of Changes" section in README.

**Changes to the prompt (v.61):**
- Refined review structure: mandatory preliminary stage added (thematic spectrum, category composition, general level of the array).
- Added prospects for integration with AI services to the "Practical Value" criterion.
- Requirement for sorting articles in the final output from highest to lowest score ("quality anchor").
- Additional materials now considered as an increasing factor for novelty and methodology.
- Adjusted criteria scale: Novelty 35%, Methodology 30%, Practical Value 20%, Visualization 15% (ethics integrated into methodology).
- Clarified criteria for the highest score for P-Novelty (logical integrity, identifying limitations of traditional approaches, potential for a new research program).

## 260428
**Added: modified prompt, source materials for comparing articles from journals with high and low entry barriers:**
- New version of the prompt: `Universal_AI_Review_Prompt_v_71_RU.txt` and `Universal_AI_Review_Prompt_v_71_EN.txt`.
- Source files and run results folder: `journal_comparison_high_low_entry_barriers_data`

## 260430
**Added source materials for the article CALIBRATED AI REVIEWER: AN ALGORITHM FOR MATCHING A MANUSCRIPT WITH A JOURNAL'S LEVEL**
- source files and run results in folder `AI_Reviewer_Manuscript_vs_Journal`

## Related publications

Kravtsov G.G. Open-source AI reviewer: a universal tool for hybrid expertise and self-analysis of scientific texts (https://doi.org/10.5281/zenodo.17020322)  
Kravtsov G.G. Two-level open-source architecture for independent ranking of scientific journals (https://doi.org/10.5281/zenodo.19640342)  
Kravtsov G.G. TWO-LEVEL OPEN-SOURCE ARCHITECTURE FOR INDEPENDENT AI RANKING OF SCIENTIFIC JOURNALS (https://doi.org/10.31235/osf.io/vpbk6_v1)  
Kravtsov G.G. Calibration AI reviewer: algorithm for comparing scientific journals with high and low entry barriers (https://doi.org/10.5281/zenodo.19784244)  

## License

CC BY 4.0
