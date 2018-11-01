# A2: Bias in data

Name: Ryan Bald

Date: 11/01/2018

## Goal

The goal of this assignment is to identify potential biases with the volume and quality of English Wikipedia articles about politicians, across many different countries.

## External Data Sources

**data/page_data.csv**

A CSV file storing information about ~50,000 English Wikipedia politician articles. The CSV file, relevant code, and other dataset information can be viewed/downloaded at https://figshare.com/articles/Untitled_Item/5513449.

|column |description                                          |
|-------|-----------------------------------------------------|
|page   |name of Wikipedia article                            |
|country|country of politician the Wikipedia article is about |
|rev_id |revision ID of the last edit to the Wikipedia article|

**data/WPDS_2018_data.csv**

A CSV file storing ~200 countries/continents and their populations in millions of people. The CSV file can be downloaded at https://www.dropbox.com/s/5u7sy1xt7g0oi2c/WPDS_2018_data.csv?dl=0.

|column                        |description                                             |
|------------------------------|--------------------------------------------------------|
|Geography                     |country or contintent                                   |
|Population mid-2018 (millions)|population of country or continent in millions of people|

**Object Revision Evaluation Service (ORES) API**

API used to predict article quality based on the [WikiProject article quality grading scheme](https://en.wikipedia.org/wiki/Wikipedia:Content_assessment#Grades). The documentation can be found at https://ores.wikimedia.org/v3/#!/scoring/get_v3_scores_context.

## Dependencies

This assignment was completed using Python 3.6 and running in a Jupyter Notebook environment.

* Python 3.6 documentation: https://docs.python.org/3.6/

* Jupyter Notebook documentation: https://jupyter-notebook.readthedocs.io/en/latest/

The following Python packages were also used:

* pandas 0.22.0 ([documentation](https://pandas.pydata.org/pandas-docs/version/0.22/index.html))
* requests 2.18.4 ([documentation](http://docs.python-requests.org/en/master/))

## Outfiles

**article_qualities.csv**

A CSV file that merges the Wikipedia articles CSV file, the country populations CSV file, and the article quality predictions extracted from the ORES API calls.

|column         |description                                         |
|---------------|----------------------------------------------------|
|country        |country of politician the Wikipedia article is about|
|article_name   |name of Wikipedia article                           |
|revision_id    |revision ID of last edit to Wikipedia article       |
|article_quality|predicted grade/quality of Wikipedia article        |
|population     |population of country in millions of people         |

## Licenses

This assignment's code is released under an [MIT License](https://opensource.org/licenses/MIT).

`data/page_data.csv` is licensed under a [CC BY 4.0 License](https://creativecommons.org/licenses/by/4.0/).
