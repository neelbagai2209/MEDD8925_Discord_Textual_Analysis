# MEDD8925 Discord Textual Analysis

Welcome to my repository! This project contains files and scripts used for the analysis of Discord textual data to extract and classify slang terms. The final deliverable is **`Slang Terms with Meaning.csv`**, a file containing 193 slang entries with definitions and rankings.

Feel free to explore or build upon this work. Below is the detailed methodology and file descriptions.

---

## Methodology

### 1. Urban Dictionary Reference Corpus
- **File used**: `urbandict_sitemap_gz.xml`
- Script: **`Urban Dictionary One Word Slang Scrape.ipynb`**
- Output: **`urban_dictionary_one_word_slangs.txt`**

The sitemap from Urban Dictionary was processed to create a reference corpus (`urban_dictionary_one_word_slangs.txt`), which was then added to **AntConc** as the reference corpus.

### 2. Discord Data
- **Source**: [Discord Data | Kaggle](https://www.kaggle.com/datasets/jef1056/discord-data/data)
- Dataset version: **`Discord Data v3 Antispam`**

The Discord data was cleaned using:
- **`Test Discord Removal.ipynb`**
- **`Discord Data Cleanup.ipynb`**

This resulted in a target corpus for **AntConc**.

### 3. Keyword Extraction Using AntConc
In **AntConc**, the reference and target corpora were analyzed:
- **Criteria**: Frequency > 200 and Range > 50
- **Outputs**:
  - `keywordlist.csv`
  - `keywordlist_info.csv`
  - `corpus_info.csv`

### 4. WordNet-Based Classification
Using the [WordNet-based categorization dictionary](https://provalisresearch.com/products/content-analysis-software/wordstat-dictionary/wordnet-based-categorization-dictionary/), keywords were classified:
- **Files created**:
  - `all_wordnet_cleaned.csv`
  - `all_wordnet_categories.csv`

This was further processed in:
- Script: **`Classified Dictionary Word List.ipynb`**
- Output: `classified_keywords.csv`

### 5. Refining Classified Keywords
The classified keywords were refined in:
- Script: **`Refined Classified Dictionary List.ipynb`**
- Output: `refined_classified_keywords.csv`

Further refinements were made in:
- Script: **`Further Refined Keyword List of Slang.ipynb`**
- Output: `filtered_keywords_cleaned.csv`

### 6. PageRank Scoring
PageRank was applied to score the keywords:
- Script: **`Graph Based Keyword Extraction Discord Data.ipynb`**
- Output: `refined_keywords_pagerank_scores.csv`

### 7. Final Deliverable
Using **`refined_keywords_pagerank_scores.csv`**, the final file was created:
- **`Slang Terms with Meaning.csv`**: Contains 193 slang terms with meanings and rankings.

---

## File Descriptions

Below is a list of all files included in this repository:

### Scripts
- **`Urban Dictionary One Word Slang Scrape.ipynb`**: Processes Urban Dictionary data.
- **`Test Discord Removal.ipynb`**: Initial testing of Discord data cleaning.
- **`Discord Data Cleanup.ipynb`**: Cleans Discord data for analysis.
- **`Classified Dictionary Word List.ipynb`**: Classifies keywords using WordNet.
- **`Refined Classified Dictionary List.ipynb`**: Refines classified keywords.
- **`Further Refined Keyword List of Slang.ipynb`**: Final refinement of keywords.
- **`Graph Based Keyword Extraction Discord Data.ipynb`**: Applies PageRank to keywords.

### Data Files
- **`urbandict_sitemap_gz.xml`**: Urban Dictionary sitemap.
- **`urban_dictionary_one_word_slangs.txt`**: Reference corpus from Urban Dictionary.
- **`keywordlist.csv`**: Extracted keywords from AntConc.
- **`keywordlist_info.csv`**: Additional keyword metadata.
- **`corpus_info.csv`**: Corpus metadata from AntConc.
- **`all_wordnet_cleaned.csv`**: Cleaned WordNet data.
- **`all_wordnet_categories.csv`**: WordNet categories.
- **`classified_keywords.csv`**: Keywords classified using WordNet.
- **`refined_classified_keywords.csv`**: Refined classified keywords.
- **`filtered_keywords_cleaned.csv`**: Further cleaned keywords.
- **`refined_keywords_pagerank_scores.csv`**: Keywords scored using PageRank.
- **`Slang Terms with Meaning.csv`**: Final deliverable with slang terms and definitions.

### Additional Files
- **`English_stoplist.txt`**: List of English stop words.
- **`final_slang_words.txt`**: Final list of slang words.
- **`slang_wordlist_frequencies.csv`**: Frequencies of slang words.

---

## Usage Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/neelbagai2209/MEDD8925_Discord_Textual_Analysis.git
   cd MEDD8925_Discord_Textual_Analysis
