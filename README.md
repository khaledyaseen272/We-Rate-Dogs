# (Twitter Account 'We Rate Dogs' Data)
## by (Khaled Yaseen)


## Data sources:
### In the project I needed to gather 3 files in 3 different formats , every file will make a sigle dataframe:

1- twitter-archive-enhanced.csv (CSV file) 
2- image_predictions.tsv (downloaded programmatically ) 
3- twitter api for additional data ( json file )

## After loading data from CSV file of Ford Go-bike system Dataset, i started assessing data visually and programatically to be cleaned and I found some limitations i need to handle it before starting analysis , for instance :
### A- Missing data (completeness issue) :

- missing values of in reply to status id,in reply to user id,retweeted_status_id,retweeted_status_user_id, retweeted_status_timestamp in archived dataframe.

### B- Tidiness issues: 

- requiered one dataframe.
- dogs stage type are columns values shouldn't be columns names.
- p2 & p3 columns not needed , the first prediction is higher probabilty.
- names of p1 & p1_dog & p1_conf is not Better representation.

### C- Quality issues:
#### Validity:
- only original tweets required not retweets or replies or tweets without images.
- tweet id is string not floats.
- time stamp is datetimes not strings.
- dog stages are category not string.
- img_num is category.

#### Accuracy:

- unavailable dognames (none, a, an , the).

#### Consistency:

- i will uniform the rating method so the rating_numerator from 5 to 15 and rating_denominator must be 10.
- columns arrange in not the best way.

## After cleaning data I stored it as csv file then I read the csv as my new df which will be analyzed and visualized . In analysis and visualization process I decided to focus on 9 insights and visualize them , here the findinings:

1- Golden_Retriever has most tweets from weratedogs account .

2- Angora has most retweets from weratedogs followers.

3- Angora has most favourite counts from weratedogs followers.

4- the most important breed in tweet counts from weratedog account doesn't have the same interest and almost ignored from the followers in retweet and favourite counts , vice versa the most important breed in retweet and favourite counts doesn't have the same interest from weratedog account in tweet counts (important insight here is that the the most count breed in favourits and retweets ‘Angora’ is not dog in prediction of machine learning !!!).

5- the most breeds in retweet and favourite counts are for other animals not dogs or dogs in weird photoes so the the prediction of it in machine learning is not dog , and these weird tweets have more interaction from follwers than others of normal dogs.

6- ideal time to tweet and get interactions is 6 A.M.

7- the relation between retweet count and rating ratio is positive correlation.

8- in the beggining of weratedogs the rating numerator was < 10 then the rating method changed.

9- retweets Number number increases over time and years.