# ChartTableViVQA: Vietnamese Visual Question Answering for Chart and Table Images with Instruction

## Project Overview
**ChartTableViVQA** is a fully self-collected dataset designed for **Visual Question Answering (VQA)** tasks involving **charts** and **tables** in Vietnamese.  
It addresses the lack of high-quality, domain-specific resources for multimodal AI in the Vietnamese context.  
The dataset enables the evaluation and development of models that interpret both **visual** and **textual** information, benchmarked with **Qwen2.5-VL-7B-Instruct**.

---

## Dataset

### Source and Collection
The dataset was collected from reputable Vietnamese educational websites (*Vuihoc.vn*, *Vietjack.com*, *Yourhomework.net*), which base their materials on **Vietnam’s official statistical yearbooks**.  
All images, annotations, and reasoning instructions were manually curated and validated to ensure **accuracy**, **clarity**, and **relevance**.

### Content
- 395 chart images (bar charts, line charts, pie charts)
- 474 table images (numerical, comparative, analytical tables)
- 13,069 question–answer pairs, each with step-by-step reasoning instructions

### Question Categories
- **Lookup** – Direct retrieval of values from visual data
- **Comparison** – Identify greater/lesser values and calculate differences
- **Aggregation** – Perform sums, averages, and differences
- **Trend Analysis** – Detect increases, decreases, or consistent patterns

### Data Format
Structured in **JSON** with:
- Metadata for each image
- Raw data extracted from charts/tables
- Question–answer pairs
- Reasoning instructions for each QA pair

### Quality Assurance
1. Manual verification of all numerical values and labels
2. Multiple rounds of cross-checking by different annotators
3. Removal of redundant, ambiguous, or low-quality entries

---

## Installation

**Prerequisites**
- Python 3.x

**Install dependencies**
```bash
pip install pandas numpy scikit-learn torch transformers
```

---

## Results

| Metric    | ChartVQA | TableVQA | Average |
| --------- | -------- | -------- | ------- |
| BERTScore | 76.70%   | 82.20%   | 79.45%  |
| BLEU-1    | 15.50%   | 29.10%   | 22.30%  |
| ROUGE-1   | 39.80%   | 55.00%   | 47.90%  |
| METEOR    | 18.70%   | 34.90%   | 26.80%  |

---

## Main Responsibilities

* Collected and curated **Vietnamese-only** charts and tables from official statistical sources
* Generated and validated **13,069 QA pairs** in four categories
* Designed a structured JSON schema for dataset storage
* Benchmarked **Qwen2.5-VL-7B-Instruct** and analyzed results by question type
* Conducted error analysis to identify reasoning weaknesses

---

## Project Duration

**Ongoing** – The dataset has been fully collected and initial benchmarking completed.  
Upcoming work includes expanding the dataset and conducting further experiments with diverse multimodal models.

---

## Conclusion

**ChartTableViVQA** is the **first large-scale, self-collected Vietnamese dataset** for chart and table VQA, enriched with detailed reasoning annotations.  
Benchmarking results confirm its value as a reliable resource for advancing multimodal AI in the Vietnamese context.  
Future developments will focus on enlarging the dataset, increasing visual variety, and adding paraphrased answers to enhance model robustness and generalization.

---
