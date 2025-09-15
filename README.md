

---

# MediaMorphBD: Government Stance Classification Dataset

## Overview

**MediaMorphBD** is a bilingual resource consisting of **two separate datasets**:

* **Bangla dataset** (`updated_bangla_dataset.csv`)
* **English dataset** (`updated_english_dataset.csv`)

Each dataset contains Bangladeshi news articles annotated with **stance**, **sentiment**, and **media bias**.
The corpus spans from **2013 to 2025**, split into *before* and *after* the **July 2024 Uprising**.

The dataset enables research on:

* **Stance Detection** (Pro-government, Anti-government, Neutral)
* **Sentiment Analysis** (Positive, Negative, Neutral)
* **Media Bias Classification** (Biased, Neutral, Objective)

---

## Repository Structure

```
MEDIAMORPHBD-GOVERNMENT-STANCE-CLASSIFICATION-DATASET/
│
├── Datasets/
│   ├── dataset_info.json
│   ├── updated_bangla_dataset.csv
│   ├── updated_english_dataset.csv
│
├── LICENSE.md
└── .gitattributes
```

---

## Dataset Details

### English Dataset

* **Articles**: 6,269
* **Sources**: 8 newspapers + 1 international source (*Al Jazeera*)
* **Tokens**: \~2.19M
* **Categories**: Politics, National, Government Affairs

### Bangla Dataset

* **Articles**: 3,349
* **Sources**: 4 newspapers (*Prothom Alo, Bangladesh Pratidin, Samakal, BDNews24*)
* **Tokens**: \~4.33M
* **Categories**: Politics, National, Government Affairs

---

## Columns

Both datasets share the same 15 features:

* `Title` – Article headline
* `Author` – Author name (if available)
* `Date` – Publication date
* `Source` – Newspaper source
* `ArticleText` – Full article text
* `Period` – Before/After July 2024 uprising
* `CountryLeader` – Political leader referenced
* `Cleaned_Text` – Preprocessed text (NLTK cleaned)
* `Loaded_Language_Score` – Emotional/charged language score
* `Hedging_Score` – Uncertainty or cautious expressions score
* `Bias_Label` – Biased / Neutral / Objective
* `Bias_Confidence` – Confidence score (0–100)
* `Predicted_Stance` – Pro-government / Anti-government / Neutral
* `Sentiment_Polarity` – Continuous sentiment score
* `Sentiment_Label` – Positive / Negative / Neutral

---

## Quick Stats

| Language    | Period           | Pro-Gov (%) | Anti-Gov (%) | Neutral (%) | Positive (%) | Negative (%) | Neutral Sentiment (%) |
| ----------- | ---------------- | ----------- | ------------ | ----------- | ------------ | ------------ | --------------------- |
| **English** | Before July 2024 | 21.3        | 54.3         | 24.4        | 21.3         | 57.4         | 21.3                  |
| **English** | After July 2024  | 27.0        | 15.1         | 57.9        | 27.0         | 46.0         | 27.0                  |
| **Bangla**  | Before July 2024 | 21.2        | 33.4         | 45.4        | 21.2         | 53.8         | 25.0                  |
| **Bangla**  | After July 2024  | 9.7         | 65.6         | 24.7        | 9.7          | 66.2         | 24.1                  |

*(Percentages adapted from findings in the MediaMorphBD paper.)*

---

## Citation

If you use this dataset, please cite:

```
@article{MediaMorphBD2025,
  title={MediaMorphBD: A Dataset of Government Sentiment and Stance in Bangladeshi News Before and After the July 2024 Uprising},
  author={Meherun Mehnaj Miti, Joytun Nessa Tonny, Abrar Hasnat Bhuiyan Maheen, Selina Akter Mim, Ms. Khushnur Binte Jahangir, Md. Tarek Hasan},
  year={2025},
  journal={Preprint}
}
```

---

## License

Released under the **CC BY-NC-SA 4.0 License**.
Use is permitted for **non-commercial research**, with attribution.

---

## Acknowledgments

* Data collected via **Selenium & BeautifulSoup**
* Preprocessing with **NLTK**
* Annotation using **LLM-as-a-Judge (GPT-4o-mini)**

---

