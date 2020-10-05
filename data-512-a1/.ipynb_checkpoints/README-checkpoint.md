# data-512

The goal of this project is to display the mobile, desktop and combined wikipedia traffic in one simple visualization. The visualization can be seen
via the A1_plot.jpeg file.

## License of the source data and link to terms of use
CC BY-SA
GFDL
https://foundation.wikimedia.org/wiki/Terms_of_Use/en

## Links to all relevant API documentation
https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts

## Explanation of columns in en-wikipedia_traffic_200712-202008.csv

Year: The year the API call is referring to
Month: The month the API call is referring to
pagecount_all_views: The total views from desktop and mobile pagecount API calls
pagecount_desktop_views: The amount of desktop views from the pagecount API call
pagecount_mobile_views: The amount of mobile views from the pagecount API call
pageview_all_views: The total views from desktop and mobile pageview API calls
pageview_desktop_views: The amount of desktop views from the pageview API call
pageview_mobile_views: The amount of mobile views from the pageview API call

### Extra information
Data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
CSV file contains zeros for missing data but they are replaced with nan at plot time.
Pageview API returns JSON with the key for the number of views for a specific year and month as "views"
while the Pagecount API returns JSON with the key for the number of views as "count".
This software also used code from https://public.paws.wmcloud.org/User:Jtmorgan/data512_a1_example.ipynb 
which contains sample code for API calls. This sample code is licensed CC0.