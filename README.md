# 📜 Text as Data Module

<!-- EDIT with your badge link -->
[![Notebook check](https://github.com/espm-157/text-template/actions/workflows/main.yml/badge.svg)](https://github.com/espm-157/text-template/actions/workflows/main.yml)

## Team Members

🦸
🦹

## 🎓 Learning Objectives

📜 Treating text as data: from documents to paragraphs to tables  
🔤 Regular expressions, and why a pattern that runs can still be wrong  
🏷️ Classifiers that return probabilities, and checking them against your own labels  
🧭 Embeddings and search by meaning, in DuckDB  
💬 Retrieval-augmented generation, with every claim traced to a source  
🧱 Structured extraction with schemas  
🔍 Verifying output from models you did not build  
🦉 Become familiar with how climate change enters U.S. endangered species law  

## 📖 Content Overview

[💻 Assignment template](esa.ipynb)  
[💯 Assignment rubric](rubric.md)  

When the U.S. government lists a species under the Endangered Species Act, it publishes its
reasoning in the Federal Register. [Delach et al. (2019)](https://doi.org/10.1038/s41558-019-0620-8)
read the official documents for all 459 endangered animals by hand and found climate change
named as a threat for 64% of them, but management actions planned for only 18%.

In this module you read thirty years of final listing rules with code. You climb a ladder of
tools (regular expressions, a decision model, embeddings, retrieval-augmented generation, and
structured extraction), each answering a sharper version of one question: *when the
government protects a species, does it say climate change is why?* Then you reconcile your
answer with Delach et al.'s published per-species data.

Every tool past the first is a model, and every model is sometimes wrong. The question from
the first module still applies:

> How do I know these numbers are right?

## Data sources

- Federal Register API (no key needed) — <https://www.federalregister.gov/developers/documentation/api/v1>
- Delach et al. 2019 data — <https://doi.org/10.17605/OSF.IO/R9UCA>

## Models

- `deepseek-v4-flash` (language model) and `qwen3-embedding` (embeddings), served by the
  [National Research Platform](https://nrp.ai/documentation/userdocs/ai/llm-managed/)
- [Laya](https://huggingface.co/convaiinnovations/laya), an open-weights decision model,
  served on an NRP GPU for this course

The notebook reads your `NRP_TOKEN` and `LAYA_API_KEY` from the environment. Never put
these in the notebook or commit them.

## Setup

Environment setup, GitHub authentication, and language model configuration are covered on
the [course website](https://espm-157.carlboettiger.info/).

GitHub Actions runs a lightweight check on every push (the notebook is valid, every code cell
parses, and no credentials are committed). It does not run the notebook or call any model.

## Links

[🌐 Course Website](https://espm-157.carlboettiger.info/)
