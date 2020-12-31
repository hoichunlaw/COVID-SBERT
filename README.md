# COVID-SBERT: Sentence BERT trained on COVID Text

## Abstract
Follow the framework described by this paper (https://arxiv.org/abs/1908.10084), trained COVID-BERT (https://github.com/hoichunlaw/COVID-BERT) on NLI data, to have a final model capable of generating meaningful sentence embeddings.

## Model URL
https://saved-language-models.s3.amazonaws.com/covid-sbert-base-uncased.zip

## Usage
```
from sentence_transformers import SentenceTransformer
covid_model = SentenceTransformer(your_model_path)
```