# AI Peer Review Prompt

**Version:** 5.1 (250326.51)  
**Author:** Kravtsov G.G.  
**AI Model:** DeepSeek  
**Languages:** Russian / English

## Description

Universal prompt for preliminary peer review of scientific manuscripts. Implements a 100-point weighted metric (novelty 30%, methodology 25%, practical value 20%, visualization 15%, ethics 10%) with differentiation of novelty types (I/P-Novelty) and mandatory contextual calibration on an array of articles.

## Usage

1. Create a new dialogue in DeepSeek
2. Copy the prompt text from the file `Universal_AI_Review_Prompt_v_51_EN.txt`
3. Provide it to the AI along with the manuscript(s) to be reviewed
4. The AI will generate a structured review according to the algorithm

**Approximate execution time:** 1.5–2 minutes for 4 average-sized articles.

## Data Availability

All materials required to reproduce the results are publicly available:

### Prompts
- `Universal_AI_Review_Prompt_v_51_RU.txt` — calibrated version (Russian)
- `Universal_AI_Review_Prompt_v_51_EN.txt` — calibrated version (English)
- `Simple_AI_Review_Prompt_RU.txt` — simple non-calibrated prompt (for reference)

### Validation Data
- `validation/Supplementary_Validation_Data.xlsx` — method validation (10 runs of simple and calibrated prompts)
- `examples/DEMO_AMIS_peer_review_4_papers_2026_RU.doc` — example of AI-generated peer review (https://doi.org/10.5281/zenodo.19275632)

### Example
- `DEMO_AMIS_peer_review_4_papers_2026_RU.doc` — example of AI-generated peer review (https://doi.org/10.5281/zenodo.19275632)

### Subprompts
- `subprompts/` — modular prompts for analyzing individual sections (title, abstract, introduction, etc.)

### Related Publication

Kravtsov G.G. Open-source AI reviewer: universal tool for hybrid expertise and self-analysis of scientific texts (https://doi.org/10.5281/zenodo.17020322)

## License

CC BY 4.0
