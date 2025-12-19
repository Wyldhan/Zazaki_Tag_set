# Zazaki POS-Tagged Gold Standard Dataset

This repository contains a manually annotated gold standard dataset for Zazaki (Kirmanjki/Dimli) Kurdish, specifically curated for Natural Language Processing (NLP) researchers. This dataset serves as a robust benchmark for tasks such as Part-of-Speech (POS) tagging and morphological analysis.

## Composition and Methodology
The dataset was constructed using 100 sentences randomly sampled from the first 75 issues of the Vate journal, a primary source for standardized Zazaki. In the selection process, strict structural constraints were applied to ensure data consistency: each sentence was curated to contain a minimum of 4 and a maximum of 10 tokens.

## Application
This specific gold standard was utilized as the evaluation ground truth in a study focused on the assessment of Hunspell-based morphological tools. By providing a verified reference point, it enables the precise measurement of error rates and linguistic coverage for Zazaki computational models.

## 📊 Dataset Specifications

* **Total Tokens:** 1,188
* **Language:** Zazaki
* **Format:** `.tsv` (Tab-Separated Values)
* **Annotation Type:** Manual POS Tagging
* **Quality:** Expert-verified (Gold Standard)

## ✍️ Annotation & Methodology

The dataset has been meticulously labeled by two language experts to ensure high linguistic accuracy and consistency:

* **Pınar Yıldız**
* **Hacı İbrahim Aytekin**

The annotation process involved cross-verification between the experts to minimize inter-annotator disagreement, making this set ideal for evaluating the performance of automated tagging systems.

---

## 📁 File Structure

The data is stored in a structured **TSV** format, which is easily parsable by standard NLP toolkits like `spaCy`, `NLTK`, or `HuggingFace Datasets`.

| Column | Description |
| :--- | :--- |
| `Word` | The surface form (token) from the text. |
| `Label` | The Part-of-Speech tag assigned by the experts. |

### Sample Data
```text
kes	kes	PRON
vecîyayene	nêveciya	VERB
vatene	nêva	VERB
```


## 🚀 Getting Started
You can easily load the dataset using Python and pandas:

Python
```
import pandas as pd

# Load the gold standard test set
df = pd.read_csv("zazaki_test.tsv", sep="\t")

# Preview the data
print(df.head())

```

## 🎯 Use Cases
* **Evaluation:** Use this as a test set to evaluate zero-shot or cross-lingual POS taggers.

* **Fine-tuning:** Small-scale fine-tuning for low-resource model adaptation.

* **Linguistic Research:** Quantitative analysis of Zazaki word classes.

## 📜 Citation
*If you use this dataset in your research, please cite the contributors:*

```
@dataset{zazaki_pos_2024,
  taggers = {Yıldız, Pınar and Aytekin, Hacı İbrahim},
  title = {Zazaki POS-Tagged Gold Standard Dataset},
  year = {2025},
  author = {Yıldızhan, Veysel},
  Thesis = {ZAZAKİ İÇİN HUNSPELL: VATE DERGİSİ DERLEMİ TEMELLİ MORFOLOJİK ANALİZÖR VE YAZIM DENETLEYİCİSİ}
}
```
