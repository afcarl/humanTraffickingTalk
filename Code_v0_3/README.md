Important note:

These commands must be done in sequence.  They cannot be done simultaneously!

In order to run the tool for a single community in craigslist run the following 
sequence of commands in the Base_Code folder:

single_config.py
--sets up the base url to be scraped

python automate.py
--downloads the links to be scraped

python recursive_scrape.py
--does the scraping of all links


python results_filter_women.py
--filters women searching for men with pictures and without pictures

python results_filter_men.py
--filters men searching for women with pictures and without pictures

next within results/results_women you must create two folders:

prostitutes and non_prostitutes

Then you must manually sort the first 130 records into prostitutes 
and non_prostitutes.

next within results/results_men you must create two folders:

john and non_john

Then you must manually sort the first 130 records into john and non_john.  
This manual sorting only needs to be done once.

python classify_men.py
--classifies the remaining data into john, non_john and hard_to_classify

python classify_women.py
--classifies the remaining data into prostitutes, non_prostitutes and 
hard_to_classify.

python posts_over_time.py
--This figures out the frequency of posts over time and places the results into
a CSV file.
