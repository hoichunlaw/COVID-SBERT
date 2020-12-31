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

## Example of COVID-SBERT vs SBERT
```
s1 = "How did coronavirus transmit?"
s2 = "How did COVID-19 transmit?"

# COVID Model
e1 = covid_model.encode(s1).reshape(1, -1)
e2 = covid_model.encode(s2).reshape(1, -1)

cosine_similarity(e1, e2)
```
array([[0.838884]], dtype=float32)

```
s1 = "How did coronavirus transmit?"
s2 = "How did COVID-19 transmit?"

# bert-base-nli-mean-tokens
e1 = model.encode(s1).reshape(1, -1)
e2 = model.encode(s2).reshape(1, -1)

cosine_similarity(e1, e2)
```
array([[0.5953794]], dtype=float32)
