# Bias on Wikipedia

## Project Goal

The goal of this project is to analyze what the nature of political articles on Wikipedia - both their existence, and their quality - can tell us about bias in Wikipedia's content.

## Data

### Dataset 1: Politicians by Country from the English-language Wikipedia

The wikipedia dataset can be found on [Figshare](https://figshare.com/articles/Untitled_Item/5513449)

### Dataset 2: The Population Data

The population data is on [the Population Research Bureau website](http://www.prb.org/DataFinder/Topic/Rankings.aspx?ind=14)

### Related API 

[ORES](https://www.mediawiki.org/wiki/ORES): a web service and API that provides machine learning as a service for Wikimedia projects maintained by the Scoring Platform team

### The Wikimedia Foundation Terms of Use

https://wikimediafoundation.org/wiki/Terms_of_Use/en)

### Figshare Terms and Conditions

https://figshare.com/terms

### PRB Privacy Policy

http://www.prb.org/DataFinder/Topic/~/link.aspx?_id=11A2A1677D184053936CE705FAEDEC1D&_z=z

## Final Dataset Desciption

The final data file generated for data analysis contains five variables(columns):

| Column          |
| --------------- |
| country         | 
| article_name    | 
| revision_id     | 
| article_quality |
| population      |

- article_quality: ORES returns a prediction value that contains the name of one category, which represents the article quality

## Data Analysis

### Calculating the proportion of articles per population for each country

For example:
if a country has a population of 10,000 people, and you found 10 articles about politicians from that country, then the percentage of articles-per-population would be .1%.

### Calculating the proportion of high-quality articles for each country

By "high quality" articles, in this case we mean the number of articles about politicians in a given country that ORES predicted would be in either the "FA" (featured article) or "GA" (good article) classes.

For example:
if a country has 10 articles about politicians, and 2 of them are FA or GA class articles, then the percentage of high-quality articles would be 20%.

## Tables and Visualizations

#### 10 highest-ranked countries in terms of number of politician articles as a proportion of country population

|             country	           | articles_per_population | Population  |
| ------------------------------ |:-----------------------:| -----------:|
| Nauru                          | 0.004880                | 10860       |
| Tuvalu                         | 0.004661                | 11800       |
| San Marino                     | 0.002485                | 33000       |
| Monaco                         | 0.001050                | 38088       |
| Liechtenstein                  | 0.000772                | 37570       |
| Marshall Islands               | 0.000673                | 55000       |
| Iceland                        | 0.000623                | 330828      |
| Tonga                          | 0.000610                | 103300      |
| Andorra                        | 0.000436                | 78000       |
| Federated States of Micronesia | 0.000369                | 103000      |


- 2. 10 lowest-ranked countries in terms of number of politician articles as a proportion of country population
- 3. 10 highest-ranked countries in terms of number of GA and FA-quality articles as a proportion of all articles about politicians from that country
- 4. 10 lowest-ranked countries in terms of number of GA and FA-quality articles as a proportion of all articles about politicians from that country




## Licence

The MIT License is a permissive free software license originating at the Massachusetts Institute of Technology (MIT). As a permissive license, it puts only very limited restriction on reuse and has therefore an excellent license compatibility. For detailed description of the contents of license please refer to the file [License](https://github.com/jingyany/data-512-a1/blob/master/LICENSE).
