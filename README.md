# Domain-Specific LLM Fine-Tuning

A domain-specific language model fine-tuning project exploring parameter-efficient fine-tuning (PEFT) using LoRA for helpdesk ticket classification and prioritization.

## Overview

This project demonstrates a workflow for adapting a pretrained language model to a specialized helpdesk domain.

It includes synthetic helpdesk ticket data, baseline evaluation, LoRA/PEFT training code, an evaluation workflow, and an API interface.

The project is designed to explore how domain-specific fine-tuning can improve classification tasks while reducing the number of trainable model parameters.

## Key Features

- Synthetic helpdesk ticket dataset.
- Domain-specific classification workflow.
- Ticket category prediction.
- Ticket priority prediction.
- LoRA-based fine-tuning implementation.
- PEFT training workflow.
- Baseline evaluation.
- Model evaluation scripts.
- API implementation.
- Docker configuration.
- Automated tests.

## Architecture

```text
       Helpdesk Ticket Dataset
                  |
                  v
          Data Preparation
                  |
                  v
          Pretrained LLM
                  |
                  v
          LoRA / PEFT Setup
                  |
                  v
          Fine-Tuning Workflow
                  |
                  v
           Model Evaluation
                  |
                  v
           Prediction API
                  |
                  v
        Category / Priority
```

## Technology Stack

- Python
- Hugging Face Transformers
- PEFT
- LoRA
- PyTorch
- FastAPI
- Pytest
- Docker

## Dataset

The project uses **80 synthetic helpdesk ticket examples**.

The examples are synthetic and licensed under CC0 according to the project dataset documentation.

The dataset supports experimentation with ticket categorization and priority prediction.

## Project Structure

```text
llm-domain-finetuning/
│
├── data/
├── src/
├── training/
├── evaluation/
├── api/
├── tests/
├── requirements.txt
├── Dockerfile
├── README.md
└── .gitignore
```

*The actual repository files should be used as the source of truth.*

## Installation

```bash
git clone https://github.com/Chanikyaa/llm-domain-finetuning.git
cd llm-domain-finetuning

python -m venv .venv
```

Activate the environment:

**Windows**
```bash
.venv\Scripts\activate
```

**Linux/macOS**
```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Fine-Tuning Workflow

The repository includes training code for LoRA-based parameter-efficient fine-tuning.

Actual fine-tuning requires the relevant Transformers and PEFT dependencies and access to the selected pretrained model.

Use the training script and configuration included in the project for the exact execution command.

## Baseline Evaluation

The baseline evaluation used 20 held-out synthetic examples.

| Metric | Baseline Result |
|---|---:|
| Category accuracy | 80% |
| Category macro-F1 | 0.80 |
| Priority accuracy | 35% |
| Exact combined-label accuracy | 30% |

These are baseline results only. They do not represent the performance of a fine-tuned model.

## Testing

Run the automated tests:

```bash
pytest
```

## Current Validation

- Automated tests: **10 passed**.
- Training implementation and evaluation code are included.
- Baseline evaluation completed on the held-out examples.

## Important Limitations

- Actual LoRA fine-tuning has **not been executed**.
- Transformers and PEFT were unavailable in the validation environment.
- No fine-tuned model performance or improvement has been established.
- Model downloads may require internet access unless the model is already cached.
- Docker and hosted CI have not been verified.

## Engineering Concepts Demonstrated

- Domain adaptation
- Large Language Model fine-tuning
- Parameter-efficient fine-tuning
- LoRA
- Synthetic dataset preparation
- Classification evaluation
- Model serving
- API development

## Future Improvements

- Execute LoRA fine-tuning with a pretrained model.
- Compare pretrained and fine-tuned performance.
- Evaluate on a larger real-world dataset.
- Add confusion matrices and per-class metrics.
- Optimize inference latency.
- Deploy the fine-tuned model through an API.

## Author

**Palli Chanikya Paidi Balaji**

B.Tech – VIT Chennai (2025)  
M.Tech CSE – AI & Data Science, Mahindra University (2026–2028)

GitHub: [@Chanikyaa](https://github.com/Chanikyaa)

---

*Part of an AI/ML Engineering Portfolio.*
