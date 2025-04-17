First file to be used was 'urbandict_sitemap_gz.xml' that provided the sitemap that was used in 'Urban Dictionary One Word Slang Scrape.ipynb' to create 'urban_dictionary_one_word_slangs.txt' which was added to AntConc as the reference corpus. 

For the Urban Dictionary data, it was obtained from the following URL: https://www.kaggle.com/datasets/jef1056/discord-data/data
There are many versions but for ease, 'Discord Data v3 Antispam' was used as it was the latest and had some degree of preprocessing. Discord will not be uploaded.
This data was utilized in 'Test Discord Removal.ipynb' as a test before being used in 'Discord Data Cleanup.ipynb' to create the cleaned data that was provided to AntConc as the target corpus

In AntConc, once the refence and target corpora were added, the keywords tab was used. As mentioned, if frequency was more than 200 and range was over 50, the word was chosen to be selected. This data was exported and can be found in the file 'keywordlist.csv' with 'keywordlist_info.csv' and 'corpus_info.csv' provided by AntConc as well, although somewhat useless. 

'all_wordnet_cleaned.csv' and 'all_wordnet_categories.csv' were created using the WordNet data that was available for free here: https://provalisresearch.com/products/content-analysis-software/wordstat-dictionary/wordnet-based-categorization-dictionary/

This data was utilized with the aforementioned 'keywordlist.csv' to create 'classified_keywords.csv' that had all the keywords classified. The code can be found in 'Classified Dictionary Word List.ipynb'

After generating ' 'classified_keywords.csv' only the Noun.Communication and null categories were kept as slang using 'Further Refined Keyword List of Slang.ipynb' which resulted in the file 'filtered_keywords_cleaned.csv' which was the most refined version of the slang words present in the Discord Data with the Urban Dictionary having been used as the reference corpus. 
