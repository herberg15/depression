# User-Level Depression Detection with Long-Context Transformers and Behavioral Metadata

This repository contains the source code and experimental pipeline for the study:

**“User-Level Depression Detection with Long-Context Transformers and Behavioral Metadata”**

The study proposes a hybrid deep learning framework for detecting depression at the user level from social media data by combining long-context Transformer architectures with behavioral metadata features.

---

## Overview

Most Transformer-based depression detection approaches are limited to short text segments due to the 512-token input constraint, which restricts their ability to model longitudinal user behavior. In addition, aggressive text preprocessing may remove expressive cues relevant to mental health assessment.

To address these limitations, this work:
- Models entire user timelines using **long-context Transformers** (up to 4096 tokens),
- Introduces a **Selective Cleaning (SC)** strategy to preserve contextual and emotional signals,
- Integrates **behavioral metadata** with contextual text representations,
- Performs systematic comparisons against standard Transformer baselines.

---

## Methodology

### Text Preprocessing
Two preprocessing strategies are evaluated:
- **Aggressive Cleaning (AC):** Traditional noise-removal pipeline.
- **Selective Cleaning (SC):** Context-preserving minimal preprocessing aligned with Transformer architectures.

### Models
The following models are implemented and evaluated:
- BERT-base
- Roberta-Base
- DistilBert
- MentalBERT
- Longformer
- BigBird

Longformer and BigBird are used to process sequences of up to **4096 tokens**, enabling user-level longitudinal modeling.

### Behavioral Metadata
A total of **37 behavioral features** are extracted, including:
- Temporal activity patterns (e.g., night posting behavior),
- Engagement metrics,
- User-level activity statistics.

Metadata features are fused with Transformer-based representations in a hybrid architecture.

---


