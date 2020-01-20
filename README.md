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
