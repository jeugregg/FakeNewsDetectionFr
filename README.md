# FakeNewsDetectionFr

Detect French Fake News

- Scraping TRUE news from French Newspapers  using "gbolmier/newspaper-crawler" : 
  - Futura Sciences
  - Liberation
  - Telerama
  - Le Monde
  - Le Figaro

For Le Monde, it is necessary to modify the spider : 
newspaper_crawler/spiders/lemonde_spider.py
- issue #1 : fixing lemonde body scraping 

-  Scraping TRUE news using "scrapy" for : 
  - 20 minutes 

- Scraping FAKE news from French Parody Newspapers using "scrapy" : 
  - Le Gorafi
  - NordPresse.be
  - BuzzBeed.com

- Train camemBERT model 
- Evaluate 
- Compare to baseline

Files :
 
01_Scraping_French_newspaper_crawler.ipynb : 
This notebook can be used to scrap french news from RSS feed of these newspapers :

  - Figaro
  -  Futura Sciences
  -  Liberation
  -  Le Monde

Doesn't work for :

   - Nouvel Obs

This notebook can be executed several times to add new news to database : newspaper_db.

02_Scraping_French_News.ipynb : 
This notebook use scrapy classes to retrieve latest news content from :
  - Le Gorafi (societe, politique)
  - Nord Presse.be (France)
  - BuzzBeed
  - 20 Minutes

2 possible sources :
  - pages links and next page (best)
  - RSS feed (possible to update data)

To select only RSS :
  - execute only RSS parts and finish by Export parts.

03_Train_evaluate_camemBERT.ipynb : 
French Fake News Detection model with camemBERT model
This notebook contains :
- Exploration of news
- Preparation input data
- Training camemBERT Sequence Classification (using "simpletransformers")
- Evaluation
- Works on Google Colab
  - Choose GPU Execution type
  
04_Train_evaluate_baseline.ipynb : 
French Fake News Detection baseline model
This notebook contains :
- Preparation input data TF-IDF
- Training baseline Sequence Classification (using "LogisticRegression")
- Evaluation
- Works on Google Colab


