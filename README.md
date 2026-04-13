# WMT2026 Shared Task: Efficient Low-Resource Multilingual Translation
## Chinese-Southeast Asian Multilingual MT Task


## OVERVIEW AND TASK DESCRIPTION
WMT is a leading conference dedicated to the advancement of machine translation research and technology. The Shared Task is a core component of WMT, providing a standardized platform for researchers to evaluate and compare the performance of different machine translation systems on a common benchmark dataset.

Against the backdrop of the Belt and Road Initiative, the demand for cross-language communication between Chinese and Southeast Asian languages has grown explosively. However, low-resource languages in this region are constrained by limited parallel corpora, weak model generalization, and high barriers to edge deployment. Meanwhile, mainstream high-performance translation models are oversized, making it difficult to meet millisecond-level response requirements for real-time applications and edge devices (e.g., AI phones, IoT terminals).

To address these pain points and promote research on lightweight, efficient, low-resource multilingual machine translation, we launch this dedicated shared task at WMT2026. This task focuses on bidirectional translation between Chinese and seven Southeast Asian languages, with core constraints of small model size, fast inference speed, and strong low-resource language performance. It fills the gap of efficiency-oriented multilingual translation evaluation in WMT, and drives the practical deployment and real-world application of edge-adaptable translation systems.

### Task 1: Translation into Southeast Asian Languages (Chinese → Southeast Asian Languages)
- Sub-Task 1A: Chinese → Thai
- Sub-Task 1B: Chinese → Vietnamese
- Sub-Task 1C: Chinese → Lao
- Sub-Task 1D: Chinese → Burmese
- Sub-Task 1E: Chinese → Khmer
- Sub-Task 1F: Chinese → Indonesian
- Sub-Task 1G: Chinese → Malay

### Task 2: Translation from Southeast Asian Languages (Southeast Asian Languages → Chinese)
- Sub-Task 2A: Thai → Chinese
- Sub-Task 2B: Vietnamese → Chinese
- Sub-Task 2C: Lao → Chinese
- Sub-Task 2D: Burmese → Chinese
- Sub-Task 2E: Khmer → Chinese
- Sub-Task 2F: Indonesian → Chinese
- Sub-Task 2G: Malay → Chinese

Participants will be provided with two types of core resources: (1) high-quality manually aligned parallel corpora covering all target language directions; (2) domain-matched monolingual data for each target language. Participants are required to use their built systems to translate a held-out blind test set of unseen sentences in the source language. The final ranking of systems will be based on comprehensive evaluation of translation quality, model efficiency, and low-resource robustness via a standardized automatic evaluation protocol.

---

## GOAL
The primary objectives of this shared task are to:
- Encourage advanced research in lightweight, efficient machine translation for low-resource Southeast Asian languages
- Provide a unified, standardized benchmark platform for researchers to evaluate and compare translation systems that balance translation quality, model size, and inference speed
- Advance the state of the art in edge-deployable multilingual translation for real-time and mobile application scenarios
- Establish reproducible benchmarks for low-resource cross-lingual transfer and data-efficient machine translation training

Participants are encouraged to explore and innovate in the following technical directions:
- Low-resource data augmentation: Leveraging monolingual corpora to alleviate the scarcity of parallel data for low-resource languages
- Lightweight model design: Novel model architectures, parameter-efficient fine-tuning strategies, and knowledge distillation methods tailored for low-resource translation
- Inference acceleration: Optimization techniques to achieve low-latency, high-throughput inference on resource-constrained edge devices
- Cross-lingual transfer learning: Adapting knowledge from high-resource language pairs to improve low-resource translation performance
- Multilingual modeling: Exploring unified multilingual translation frameworks with strong generalization across diverse Southeast Asian languages

---

## IMPORTANT DATES
| Date                 | Event                                                                               |
| -------------------- | ----------------------------------------------------------------------------------- |
| March 2026           | Proposal drafting and official application to WMT2026 organizing committee          |
| April 2026           | Task website released, task officially announced, and team registration open        |
| TBD                  | Team registration close                                                             |
| TBD                  | Training and validation datasets release (only for registered participants)         |
| TBD                  | Test sets release and official evaluation cycle begins (system run submission open) |
| TBD                  | End of the evaluation cycle (system run submission close)                           |
| TBD                  | Result declaration to individual participating teams                                |
| In-line with WMT2026 | System paper submission                                                             |
| November 2026        | WMT2026 Conference held in conjunction with EMNLP 2026                              |

---

## DATA
All datasets released in this task are collected from copyright-compliant resources including OPUS, Tatoeba, UN Corpus, and self-built manually proofread corpora. The datasets will be open to the research community after registration. WMT participants can use the dataset for non-commercial research purposes in accordance with the CC-BY fair use principle.

We spent 8 months addressing data sourcing and quality control, and invested around 30,000 euros for manual alignment and native speaker verification to build this high-quality benchmark dataset. The detailed data statistics are listed as follows:

| Data Type                 | Total Number of Sentences | Details                                                                                                                                                                                                                                                                |
| ------------------------- | ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bilingual Training Data   | 140,000                   | Multi-domain parallel corpus covering general domains, news, healthcare, finance, and other practical fields. For each of the 7 target languages, we provide 20,000 manually aligned bilingual sentence pairs.                                                         |
| Monolingual Training Data | 700,000                   | High-quality multi-domain monolingual data matching the domain of parallel corpus. For each of the 7 target languages, we release 100,000 domain-balanced monolingual sentences, which can be used for data augmentation via back-translation and forward-translation. |
| Validation Data           | 14,000                    | Unified validation set for all 7 language pairs, with 2,000 sentences per language. All sentences are unseen and independent from training data, covering the same multi-domain scenarios, with one high-quality human reference translation per source sentence.      |
| Test Data                 | 14,000                    | Held-out blind test set, with 2,000 sentences per language. Consistent with the validation set in domain coverage and data specification, with high-quality human reference translations. System ranking will be based on performance on this test set.                |

In addition to the above datasets, parallel and monolingual data from the WMT2026 General MT Task can also be used for data augmentation in this task.

---

## TEST DATA
The held-out blind test set will be released to registered participants at the start of the evaluation cycle. It contains 2,000 unseen sentences for each of the 7 Southeast Asian languages, covering general, news, healthcare, finance and other practical application domains. Each source sentence is paired with exactly one high-quality human reference translation completed and verified by native speakers.

The test set is strictly independent from the training and validation datasets, to ensure the fairness and reliability of the evaluation results. Participants are required to submit the translation outputs of their systems for the test set within the specified evaluation cycle.

---

## System Submission Guidelines
- All submissions must be sent to the official task email: WmtEvaluation@163.com
- Each participating team can submit at most 1 translation output per language pair direction
- Submitted files must follow the standard format specified in the detailed task instructions (to be released along with the test set)
- Participants must submit a system description document along with the translation outputs, detailing the model architecture, training strategy, data usage, and optimization techniques adopted
- All submitted systems must comply with the task constraints on model size and inference efficiency, which will be specified in the detailed task instructions

---

## PAPER Submission Process
The paper submission process will be fully in-line with the official WMT2026 conference requirements and timeline.

---

## EVALUATION
We adopt a hybrid automatic evaluation framework that comprehensively assesses both translation quality and model inference efficiency, to fairly compare systems targeting edge deployment and real-time application scenarios.

### Translation Quality Evaluation
We use multiple mainstream automatic evaluation metrics to measure the overall accuracy and fluency of the translation outputs, including:
- sacreBLEU
- chrF
- COMET

### Efficiency & Robustness Evaluation
In addition to translation quality metrics, we incorporate dedicated automatic metrics to assess the inference performance and low-resource robustness of the systems, which are critical for edge-deployable lightweight translation systems:
- Model parameter size
- End-to-end inference latency
- Token throughput

Systems will be ranked based on a weighted comprehensive score of the above metrics. We also reserve the right to conduct targeted human evaluation by native speakers for further verification of translation quality for top-ranked systems.

---

## CONTACT
For any questions about the shared task, please contact the organizing team via official email: WmtEvaluation@163.com

---

## PAPER SUBMISSION
Your system paper submission should be prepared according to the WMT2026 official instructions, and uploaded to the START submission system before the specified deadline (TBD, in line with the WMT2026 main conference schedule).

---

## ORGANIZERS
- Ziyan Chen (Newtranx)
- Jingsong Liu (Newtranx)
- Shaolin Zhu (Tianjin University)