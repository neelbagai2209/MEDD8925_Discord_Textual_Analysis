First file to be used was 'urbandict_sitemap_gz.xml' that provided the sitemap that was used in 'Urban Dictionary One Word Slang Scrape.ipynb' to create 'urban_dictionary_one_word_slangs.txt' which was added to AntConc as the reference corpus. 

For the Urban Dictionary data, it was obtained from the following URL: https://www.kaggle.com/datasets/jef1056/discord-data/data
There are many versions but for ease, 'Discord Data v3 Antispam' was used as it was the latest and had some degree of preprocessing. Discord will not be uploaded.
This data was utilized in 'Test Discord Removal.ipynb' as a test before being used in 'Discord Data Cleanup.ipynb' to create the cleaned data that was provided to AntConc as the target corpus

In AntConc, once the refence and target corpora were added, the keywords tab was used. As mentioned, if frequency was more than 200 and range was over 50, the word was chosen to be selected. This data was exported and can be found in the file 'keywordlist.csv' with 'keywordlist_info.csv' and 'corpus_info.csv' provided by AntConc as well, although somewhat useless. 

'all_wordnet_cleaned.csv' and 'all_wordnet_categories.csv' were created using the WordNet data that was available for free here: https://provalisresearch.com/products/content-analysis-software/wordstat-dictionary/wordnet-based-categorization-dictionary/

This data was utilized with the aforementioned 'keywordlist.csv' to create 'classified_keywords.csv' that had all the keywords classified. The code can be found in 'Classified Dictionary Word List.ipynb'

After generating 'classified_keywords.csv,' irrelevant columns such as range_ref, lower_word, and source_file were dropped in 'Refined Classified Dictionary List.ipynb' as they served zero value to me in further analysis and this resulted in the file 'refined_classified_keywords.csv'

The next step involved further refinement of  'refined_classified_keywords.csv' in 'Further Refined Keyword List of Slang.ipynb,' which saw removal of all subcategories unless they were communication nouns (Noun.Communication) or had no category given their unique slang nature. This resulted in the 'filtered_keywords_cleaned.csv' file which was used for the next step, the graph-based PageRank was done.

As for the PageRank, for which the code can be found in 'Graph Based Keyword Extraction Discord Data.ipynb,' a co-occurance graph was made along with a 'refined_keywords_pagerank_scores.csv' file

Using a copy of the 'refined_keywords_pagerank_scores.csv' file, the final deliverable, the 'Slang Terms with Meaning.csv' file was made. It contains 193 slang entries (with the highest PageRank score) and includes meaning added by myself or through help of the Urban Dictionary in cases where I was unsure.


