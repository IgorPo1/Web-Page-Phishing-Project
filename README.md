
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
Which field(s) has/have the strongest correlation with the “phishing” field?  Which field(s) has/have the weakest correlation with the “phishing” field?
Would you say that the URL length is a strong indicator of whether or not the URL is phishing?  Why or why not?  What metrics do you have to support your answer?
Would you say the number of redirections is a strong indicator of whether or not the URL is phishing?  Why or why not?  What metrics do you have to support your answer?
Based on your analysis, what advice would you give to others for deciphering whether or not a URL is phishing?

1) Use the \copy command to import data to a table on a PostgreSQL (create table and then use \copy web_phishing(name of created table) (url_length, n_dots, n_hypens, n_underline, n_slash, n_questionmark, n_equal, n_at, n_and, n_exclamation, n_space, n_tilde, n_comma, n_plus, n_asterisk, n_hastag, n_dollar, n_percent, n_redirection, phishing(columns name, because CSV file has column heading information)) from 'path/for/csv/file' WITH DELIMITER ',' CSV HEADER;)
2) 
3)
