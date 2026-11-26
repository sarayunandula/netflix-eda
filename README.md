# Netflix Content Analysis (EDA)

## PROJECT GOAL 
To find out how the Netflix catalogue has grown and what it contains .

## DATASET
Netflix Movies and TV Shows dataset taken from Kaggle 
(file ends Nov 2019) : 5837 titles and 12 columns 

## STEPS 
1. Data Inspection : checked the shape , data types and missing values.
2. Cleaning :
   1. Filled missing director , cast and country with "Unknown".
   2. Filled missing rating with most common value.
   3. converted date_added to a date.
   4. kept the 642 missing dates (11%) without inventing new data.
   5. checked for duplicates , found none.
3. Feature Engineering :
   1. split duration into minutes for movies and seasons for shows.
   2. created year_added and month_added.
   3. split multi-genre and multi-country cells into one value per row.
4. Analysis and Visualization :
   Chart-1 : No. of Titles Added to Netflix per Year
   Chart-2 : Distribution of Movie Length
   Chart-3 : No. of Titles per Genre (Top 10 genres)
   Chart-4 : No. of Titles for each Country (Top 10 countries)

## KEY FINDINGS
1. The No. of Titles being added increased year by year for both Movies and Shows.
2. 62.5% of movies run 80-120 minutes (average about 98). Titles under 20 minutes are short films and behind-the-scenes features, and the 312-minute Black Mirror: Bandersnatch is an interactive film, so I kept them.
3. International Movies (1,797 titles) and Dramas (1,488) are the top 2 genres. A title can have several genres, so these counts overlap.
4. The US accounts for 36.1% of country mentions, over 3 times India's 11.2% in second place (a title can list several countries)
5. Growth is slowing: the yearly increase fell from nearly 3x in 2017 to +38% in 2018 and +13% in 2019.
6. Movies make up 67.5% of the catalogue and TV shows 32.5%. About two thirds of TV shows have only one season.
7. 97.6% of titles with a known date were added in 2016 or later, with additions rising from 74 in 2015 to 1,843 in 2019 (2019 is incomplete).


## TOOLS USED
Python , Pandas , NumPy , Matplotlib , Seaborn , Google Colab 

## LIMITATIONS
1. Dataset ends in Nov 2019. So 2019 data is incomplete , 11% of dates are missing.
2. Country figures count every country listed for a title, so shares are of mentions, not of titles.
