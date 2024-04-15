# BlendX : Complex Multi-Intent Detection with Blended Patterns


<div align=center>
  <img alt="Static Badge" src="https://img.shields.io/badge/BlendX-1.0-blue">
  <img alt="GitHub License" src="https://img.shields.io/github/license/HYU-NLP/BlendX">
  <img alt="Github Created At" src="https://img.shields.io/github/created-at/HYU-NLP/BlendX">
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/HYU-NLP/BlendX">
  <br>
</div>

### Abstract

Task-oriented dialogue (TOD) systems are commonly designed with the presumption that each utterance represents a single intent. However, this assumption may not accurately reflect real-world situations, where users frequently express multiple intents within a single utterance. While there is an emerging interest in multi-intent detection (MID), existing in-domain datasets such as MixATIS and MixSNIPS have limitations in their formulation. To address these issues, we present BlendX, a suite of refined datasets featuring more diverse patterns than their predecessors, elevating both its complexity and diversity. For dataset construction, we utilize both rule-based heuristics as well as a generative tool -- OpenAI's ChatGPT -- which is augmented with a similarity-driven strategy for utterance selection. To ensure the quality of the proposed datasets, we also introduce three novel metrics that assess the statistical properties of an utterance related to word count, conjunction use, and pronoun usage. Extensive experiments on BlendX reveal that state-of-the-art MID models struggle with the challenges posed by the new datasets, highlighting the need to reexamine the current state of the MID field. The dataset is available at https://github.com/HYU-NLP/BlendX.

![Representative Figure](Figure_1.png)

> An overview of the BlendX construction framework. Initially, we preprocess four source datasets: ATIS, Banking77, CLINC150, and SNIPS. We then select single-intent utterances from these datasets. These utterances are combined using both Manual and Generative approaches. It is important to note that utterances are kept separate and not mixed across datasets. Following the merging process, all resultant datasets are compiled to form BlendX. We particularly highlight non-trivial combinations, such as omissions, which are indicated within the blue rounded box on the rightmost side of the framework. Finally, BlendX is evaluated using three methods: custom metrics, baseline evaluation, and visualization.

### Dataset Description

The BlendX dataset comprises a suite of refined datasets with a focus on multi-intent detection in task-oriented dialogues. It introduces more diverse patterns of utterance formulation, challenging the existing MID models with its elevated complexity and diversity.


## Repository Structure
This repository contains the following datasets:

- `/v1.0` - Contains the implementation of baseline SOTA models for multi-intent detection.
    - `/BlendX` - Our original dataset, BlendX, specifically crafted to challenge and refine multi-intent detection algorithms through complex concatenation scenarios.
    - `/MixX` - Our extended version of the MixX dataset, implementing a concatenation strategy from this [paper](https://aclanthology.org/2020.findings-emnlp.163/) and [datasets](https://github.com/LooperXX/AGIF) with our additional datasets `Banking77`([paper](https://aclanthology.org/2020.nlp4convai-1.5/), [dataset](https://github.com/PolyAI-LDN/task-specific-datasets/tree/master/banking_data)) and `CLINC150`([paper](https://aclanthology.org/D19-1131/), [dataset](https://github.com/clinc/oos-eval)) included.

## Coming Soon!

- 2024.04.15 The **BlendX Dataset** is now available in this repository. We are also planning to release an updated version soon, which will include additional enhancements and features designed to further support research in TOD systems.
- 2024.03.28 The BlendX Dataset will soon be made available in this repository, offering a comprehensive and detailed dataset designed for enhancing research in task-oriented dialogue (TOD) systems.
