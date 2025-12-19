# 📚 Zazaki Gold Standard Dataset
This repository provides a manually annotated gold standard dataset for Zazaki (Kirmanjki/Dimli) Kurdish, meticulously curated for Natural Language Processing (NLP) researchers. It serves as an essential benchmark for tasks such as Part-of-Speech (POS) tagging and morphological analysis.

## 🛠 Dataset Specifications
The dataset is composed of 100 sentences randomly sampled from the first 75 issues of the Vate journal. The following constraints were strictly implemented during the selection process:

* **🔢 Token Range:** Minimum 4 – Maximum 10 tokens per sentence.

* **📖 Source Material:** Vate Journal (Issues 1–75).

* **🎯 Selection Method:** Randomized sampling for linguistic diversity.

The following table illustrates the frequency of Part-of-Speech tags within the gold standard 

| *Category* | *Tag* | *Count* |
| :--- | :--- | :--- |
| `Noun` |**NOUN** | 374 |
| `Verb` | **VERB** | 213 |
| `Pronoun` | **PRON** |170 |
| `Adposition` | **ADP** | 137 |
| `Conjunction` | **CONJ** | 92 |
| `Adjective` | **ADJ** | 85 |
| `Adverb` | **ADV** | 85 |
| `Numeral` | **NUM** | 18 |
| `Particle` | **PART** | 12 |
| `Interjection` | **INTJ** | 2 |

## 🧪 Evaluation & Use Case
This dataset was specifically developed and utilized for the performance evaluation of a Hunspell-based morphological framework. It provides a high-fidelity ground truth for measuring:

* *✅ Morphological coverage*

* *✅ Tagging accuracy*

* *✅ Dictionary validation*

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
| `Surface` | The surface form (token) from the text. |
| `Lemma` | The canonical or dictionary form of the word. |
| `Tag` | The Part-of-Speech (POS) label assigned by experts. |

### Sample Data

```text
kes	kes	PRON
vecîyayene	nêveciya	VERB
vatene	nêva	VERB
```


## 🚀 Getting Started
You can easily load the dataset using Python and pandas:

```Python
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

```text
@dataset{zazaki_pos_2024,
  taggers     = {Yıldız, Pınar and Aytekin, Hacı İbrahim},
  author      = {Yıldızhan, V.},
  title       = {SEBA ZAZAKÎ HUNSPELL: BI BINGEHÊ KORPUSÊ KOVARA VATEYÎ ANALİZKERO MORFOLOJÎK Û KONTROLKERÊ RASTNUŞTIŞÎ},
  school      = {Dicle University},
  year        = {2025},
  type        = {Doctoral thesis},
  note        = {Unpublished thesis},
  address     = {Diyarbakır, Turkey}
}
```
