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

- 1. 10 highest-ranked countries in terms of number of politician articles as a proportion of country population

|             country	           | articles_per_population | 
| ------------------------------ |:-----------------------:| 
| Nauru                          | 0.004880                | 
| Tuvalu                         | 0.004661                |
| San Marino                     | 0.002485                |
| Monaco                         | 0.001050                |
| Liechtenstein                  | 0.000772                | 
| Marshall Islands               | 0.000673                | 
| Iceland                        | 0.000623                | 
| Tonga                          | 0.000610                | 
| Andorra                        | 0.000436                | 
| Federated States of Micronesia | 0.000369                | 

The population of top 10 highest-ranked countries in terms of number of politician articles as a proportion of country population is negatively correlated to the population of the country. The population of these 10 countries is less than or equal to 10,000. This is one of the reasons that they ranked higher than countris have large amount of population. Also, the official language of these countries are mainly English. Some countries' languages are French or Italian, which is a brach of Indo-European languages. It seems easier to be translated into English. 

- 2. 10 lowest-ranked countries in terms of number of politician articles as a proportion of country population

|       country       | articles_per_population | 
| ------------------- |:-----------------------:| 
| India	              | 7.533687e-07            | 
| China               | 8.294944e-07            | 
| Indonesia           | 8.406911e-07            | 
| Uzbekistan          | 9.267902e-07            | 
| Ethiopia            | 1.069813e-06            | 
| Korea, North        | 1.561062e-06            | 
| Zambia              | 1.680249e-06            | 
| Thailand            | 1.719869e-06            | 
| Congo, Dem. Rep. of | 1.936182e-06            | 
| Bangladesh          | 2.019812e-06            | 

First, the population of 10 lowest-ranked countries in terms of number of politician articles as a proportion of country population is negatively correlated to the population of the country. The population of India and China is more than 10 hundred million. It is reasonable that the percentages are super low for these two countris. Other eight contries also have relatively large amount of populations, which lead to a low persantage. Second, all countries in this ranking are developing countrie. The political openness of most countres in this list are very low compared to developed countries. Last, The official languages of these countrie mostly are asian languages, which are very different from english. Most politician articles are not being translated to English version. So the dataset may not contains the accurate number of political articles for these countries.

- 3. 10 highest-ranked countries in terms of number of GA and FA-quality articles as a proportion of all articles about politicians from that country

|           country        | high_quality_articles | 
| ------------------------ |:---------------------:| 
| Korea, North	           | 0.230769              | 
| Romania                  | 0.129310              | 
| Saudi Arabia             | 0.126050              | 
| Central African Republic | 0.117647              | 
| Qatar                    | 0.098039              | 
| Guinea-Bissau	           | 0.095238              | 
| Vietnam                  | 0.094241              | 
| Bhutan                   | 0.090909              | 
| Ireland                  | 0.081365              | 
| United States	           | 0.078324              |



- 4. 10 lowest-ranked countries in terms of number of GA and FA-quality articles as a proportion of all articles about politicians from that country

|           country        | high_quality_articles | 
| ------------------------ |:---------------------:| 
| Finland	                 | 0.001748              | 
| Tanzania                 | 0.002451              | 
| Peru                     | 0.002825              | 
| Czech Republic           | 0.003937              | 
| Lithuania                | 0.004032              | 
| Moldova	                 | 0.004695              | 
| Fiji                     | 0.005025              | 
| Uganda                   | 0.005319              | 
| Luxembourg               | 0.005556              | 
| Nigeria	                 | 0.005848              |




## Licence

The MIT License is a permissive free software license originating at the Massachusetts Institute of Technology (MIT). As a permissive license, it puts only very limited restriction on reuse and has therefore an excellent license compatibility. For detailed description of the contents of license please refer to the file [License](https://github.com/jingyany/data-512-a1/blob/master/LICENSE).
