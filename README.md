
#Web Page Phishing Project

Description: In this project, you will analyze web page URL phishing data to determine which fields in a URL suggest that the URL may be phishing.

Difficulty: Easy

Data download: https://www.kaggle.com/datasets/danielfernandon/web-page-phishing-dataset?resource=download 

SQL Practice: 
Pretend there is an additional field in this dataset that assigns each row a unique number, or key.  This additional field is called unique_id and it is the first field in the dataset.  Pretend this data was stored in two different tables in a SQL server.  The first table is named web_page_fishing and it contains the following fields:
unique_id
url_length
n_redirection
phishing
The second table is named phishing_dataset and it contains the following fields:
unique_id
n_dots
n_hyphens
n_underline
n_slash
n_questionmark
n_equal
n_at
n_and
n_exclamation
n_space
n_tilde
n_comma
n_plus
n_asterisk
n_hashtag
n_dollar
n_percent
What SQL code would you write to query all of the data contained in the provided dataset?

Business Questions:
1) Which field(s) has/have the strongest correlation with the “phishing” field?  Which field(s) has/have the weakest correlation with the “phishing” field?
2) Would you say that the URL length is a strong indicator of whether or not the URL is phishing?  Why or why not?  What metrics do you have to support your answer?
3) Would you say the number of redirections is a strong indicator of whether or not the URL is phishing?  Why or why not?  What metrics do you have to support your answer?
4) Based on your analysis, what advice would you give to others for deciphering whether or not a URL is phishing?

Connect the data:
Use the \copy command to import data to a table on a PostgreSQL from CSV file (create table and then use \copy web_phishing(name of created table) (url_length, n_dots, n_hypens, n_underline, n_slash, n_questionmark, n_equal, n_at, n_and, n_exclamation, n_space, n_tilde, n_comma, n_plus, n_asterisk, n_hastag, n_dollar, n_percent, n_redirection, phishing(columns name, because CSV file has column heading information and you have to specify headers)) from 'path/for/csv/file' WITH DELIMITER ',' CSV HEADER;)


Business Answers:
1) The field with the strongest correlation with the phishing field is n_slash (0.611). The field with the weakest correlation with the phishing field is n_plus (0.007).
2) URL length can be considered a moderately strong indicator of whether a URL is phishing. The analysis reveals the following:
Mean URL Length: Phishing URLs have a significantly higher mean length (66.49) compared to non-phishing URLs (23.59).
Distribution: The histograms illustrate that phishing URLs generally have longer lengths, with a wider distribution and more outliers.
Percentage Longer: A substantial 87.99% of phishing URLs are longer than the average non-phishing URL.
While a longer URL doesn't definitively mean it's phishing, it does raise a red flag. Combining this information with other factors (like the number of slashes or the presence of certain characters) can help make a more informed decision about a URL's legitimacy.
3) 
