# SPC4004: Analysing Natural Language Data

A corpus linguistics study analysing the semantic shift of the word **"machine"** in UK Parliamentary discourse between 1900 and 2005, using the Hansard Corpus. Completed as part of the module **Exploring AI: Understanding and Applications (SPC4004)** at Queen Mary University of London.

---

## Research Question

> How has the semantic context of the word "machine" changed in UK Parliamentary discourse between 1900 and 2005, and can an LLM accurately classify these contextual shifts?

---

## Methodology

One sentence containing the word "machine" was systematically sampled every 5 years between 1900 and 2005 from the Hansard Corpus, producing a dataset of 22 sentences. From 1960 onwards, purposive sampling was applied to capture the emerging use of "machine" in computing contexts.

Each sentence was manually classified using a binary system:
- **1** — "machine" is used in a computing context
- **0** — "machine" is used in any other context (military, industrial, figurative, etc.)

All metadata including dates, corpus source, and file names were removed prior to LLM classification to ensure a blind test based solely on linguistic content.

---

## AI Tools Used

| Tool | Role |
|------|------|
| Claude Sonnet 4.6 | Assisted in developing the classification prompt and methodology |
| Gemini 2.0 Flash Thinking Experimental | Performed binary classification of the dataset |

---

## Key Findings

- **1900–1955**: "machine" was predominantly used in military and industrial contexts, following a cyclical pattern of pre-war usage, wartime application, post-war reflection, and economic reconstruction.
- **1960**: "machine" began appearing in computing contexts for the first time.
- **1965**: "machine" and "computer" became briefly interchangeable, possibly reflecting uncertainty around emerging technology.
- **1970**: The two terms had separated again, with "machine" returning to industrial contexts.
- **Gemini achieved 81.82% accuracy (18/22)**, with all errors being false positives — suggesting the LLM over-associated "machine" with computing when computers were mentioned nearby, potentially reflecting a training bias toward modern datasets.

---

## Repository Contents

| File | Description |
|------|-------------|
| `Parliment quotes.xlsx` | Full dataset with manual labels, Gemini predictions, match column, AI reasoning, and Hansard reference links |
| `classified_sentences.csv` | Randomised unlabelled dataset used for blind LLM classification |

---

## Dataset Source

[Hansard Corpus](https://hansard.parliament.uk) — UK Parliamentary debates, 1900–2005
