# Can LLMs Predict Gene-Disease Links?

Scripps Research internship project: ask GPT models which diseases a gene is associated with, then measure how often the answers are real versus hallucinated, using curated DisGeNET associations as ground truth.

| Notebook | What it does |
|---|---|
| `batch_request.ipynb` | Sends gene → disease prompts through the OpenAI Batch API and saves the responses |
| `new_hallucinations_filtering.ipynb` | Normalizes predicted disease names (fuzzy matching with Levenshtein distance), separates hallucinated diseases from real ones, and scores predictions with precision, recall, F1, Jaccard, BLEU and ROUGE |

**Stack:** OpenAI API · pandas · python-Levenshtein · tiktoken · seaborn

The API key is read from a local `config` file (`config['api_keys']['openai']`), which is not committed. The datasets are not included.
