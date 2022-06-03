# ChangingRoom_challenge
## Requiements:
Details:
Write an application to crawl an online fashion brand website, e.g. https://www.fordays.com, https://www.reformation.com or https://www.zara.com using a crawler framework such as Selenium, bs4, etc. You can use a crawl framework of your choice in Python. (YOU ONLY NEED TO SCRAPE A FEW PRODUCTS, not entire website, however, please explain your strategy to scrape the whole website, extract all the URLs and update the database automatically overtime (new products, update old products not available anymore)



In the challenging, I only scraped 20 items in the women's category because of the anti-scraping system. If I want to scrap more, I need go though each big categories(women's men's), and also add some judgment of if there exists next page when scraping items. If there is next page, after crawling this page,  we go to next page to crawl data.

If I want to update the database automatically, here is my strategy:
1. crawl the data daily at specific time
2. check if in each row the product in the new df appears before, we update the infos, (Use SQl commands : UPDATE products SET.....)
   if not appeared before, we add this new item (make a temp df, then use the insert_into_tabel fuction)
