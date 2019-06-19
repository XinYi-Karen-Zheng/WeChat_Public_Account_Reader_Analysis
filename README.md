# WeChat Public Account Reader Analysis
Can be used to analyze reader data provided by the WeChat public account platform, and further explore characteristics of the target reader population.

### Background<br />
Many people choose to open a WeChat public account (similar to a blog) to share useful information. However, without a deep understanding of the target reader population as well as its characteristics, accounts are hard to grow at a fast pace. Thus, as a WeChat public account owner, I started this project to learn more about my readers.

### Using Own Reader Data<br />
The WeChat public account platform tracks and provides reader data, and that's the most direct data reflecting reader characteristics.
The data comes in two forms, a general one and a 7-day detailed one.

The general form provides infomation on number of followers the account had when it sent the post, and the total number of people who read the post to date.

The more detailed form tracks data within seven days from the day the post is sent. For each day, it records
* number of people who read the post
* number of current followers who read the post
* number of people who opened the post from WeChat moments
* number of people who forwarded/recommended this post to other people
* number of people who favorited the post

For my account, I divided my articles into five different categories:
* school
* competition
* summer experience
* summer introduction
* testing

The program in own_reader_data.Rmd uses general statistical analysis + linear regression to determine which category attracts my readers the most. This result gives me inspirations in topic selection. 
Results and explanation are on my data project (link: https://karenzxy.wixsite.com/dpdp2)

### Scraping related public accounts
Writing about hot topics among target reader population can also help reach more potential followers. The program in scraped_data_abstract_analysis.Rmd determines what "hot topics" are.

Using scraped data of other (and bigger) WeChat public accounts targeting at the same reader population, the program performs simple text mining(Chinese text mining) and makes a word cloud based on frequency. The bigger a word on the word cloud, the more popular the topic is among target readers.

Results and explanation are on my data project (link: https://karenzxy.wixsite.com/dpdp2)

### Scraping UGC
When WeChat public accounts share information with readers, readers themselves may produce contents as well. 

In my case, while I share STEM related learning resources with international students, international students often write articles about their studying-experiences. Using scraped data of these articles, the program in scraped_data.Rmd performs topic analysis(English topic analysis) to extract topics that are most concerned by international students(my target readers). This result also gives me inspirations in topic selection.

Results and explanation are on my data project (link: https://karenzxy.wixsite.com/dpdp2)


# Data Format
own_reader_data.Rmd = 
For the current code, the input csv file needs follow the format of the file in sample_input. These data can be downloaded and combined from the WeChat public account platform. Article topics need to be physically labeled.
*Need to record the current number of followers in order to calculate relative numbers.

scraped_data_abstract_analysis.Rmd =
For the current code, the input csv file needs to have a column named "abstract", which contains the scraped contents.

scraped_data.Rmd = 
For the current code, the input csv file needs to have a column named "text", which contains the scraped article contents.
