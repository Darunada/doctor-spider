# Doctor Spider #
*not creepy*

Description
--------------------------------------
This spider crawls a list of doctors from SelectHealth's **Find a Doctor** 
search page and generates a CSV for easy viewing.

Installation
--------------------------------------
This scraper is built in python. Is this your first time?

- You have python installed
- You have considered creating a [virtual environment](https://docs.scrapy.org/en/latest/intro/install.html#using-a-virtual-environment-recommended) 
- You have installed requirements using `pip install -r requirements.txt`

Usage
--------------------------------------
1. Navigate to [https://selecthealth.org/find-a-doctor](https://selecthealth.org/find-a-doctor)
2. Fill in the search parameters you desire and execute a search.
3. Scroll to the bottom of the page to load all search results (hold down arrow, etc). You will see "No more results"
4. Right click in whitespace, "Save As" Complete webpage.
5. Open the saved html file in your browser
6. Replace your `file://` url into `start_urls` array in this script.
7. Execute script with `scrapy runspider doctor_spider.py -o file-to-output.json`
8. Patience...
9. Convert the json into a flattened csv format with this super rad tool [https://www.convertcsv.com/json-to-csv.htm](https://www.convertcsv.com/json-to-csv.htm)
9. Open CSV and enjoy browsing doctors at a glance in a spreadsheet.

N.B. I did not make it execute the search automatically, 
so generating the list of search results locally is required. Sorry about that, 
I couldn't figure out the infinite scroll functionality in the time I had.

 Contributing
--------------------------------------
Pull requests are welcome!
