# Project Goal

The goal of this project is to construct, analyze and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2020. 
All data, documentation, and code is published in this GitHub repository.

# License and Terms of Use

The MIT license for this project can be found [here](https://github.com/hariniramp/data-512/blob/main/data-512-a1/LICENSE)

The privacy policy of the Wikimedia Foundation REST API can be found [here](https://foundation.wikimedia.org/wiki/Privacy_policy)

The terms of use of the Wikimedia Foundation REST API can be found [here](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions).

# API Documentation

In order to measure Wikipedia traffic from January 1 2008 through August 30 2020, I collected data from two different API endpoints, 
the Legacy Pagecounts API and the Pageviews API. The documentation, endpoint and a brief description of both these APIs is below.

1. The Legacy Pagecounts API [documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end) provides access to desktop and mobile traffic data from December 2007 through July 2016.

2. The Pageviews API [documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end) 
provides access to desktop, mobile web, and mobile app Traffic data from July 2015 through last month.

# Data Files, Code & Analysis

The 5 JSON data files correspond to the 5 different API query types and are as follows:

1. pagecounts_desktop-site_200801-202008.json

2. pagecounts_mobile-site_200801-202008.json

3. pageviews_desktop-site_200801-202008.json

4. pageviews_mobile-app-site_200801-202008.json

5. pageviews_mobile-web-site_200801-202008.json

The final curated data file can be found [here](https://github.com/hariniramp/data-512/blob/main/data-512-a1/en-wikipedia_traffic_200712-202008.csv)

The analysis or final visualization can be found [here](https://github.com/hariniramp/data-512/blob/main/data-512-a1/Page%20Views%20on%20English%20Wikipedia.png)

All analysis is performed in a [Jupyter notebook](https://github.com/hariniramp/data-512/blob/main/data-512-a1/A1-Data%20Curation.ipynb).

# Data Dictionary
The fields in the final curated data file are described as follows:

1. _pagecount_desktop_views_: Number of views using desktop access obtained from the Legacy Pagecount API 

2. _pagecount_mobile_views_: Number of views using mobile access obtained from the Legacy Pagecount API 

3. _pagecount_all_views_: Number of views using desktop and mobile access obtained from the Legacy Pagecount API 

4. _pageview_mobile_views_: Number of views using mobile app and mobile web access obtained from the Pageview API 

5. _pageview_desktop_views_: Number of views using desktop access obtained from the Pageview API 

6. _pageview_all_views_: Number of views using mobile and desktop access obtained from the Pageview API 

7. _year_: Calendar year of traffic data

8. _month_: Calendar month of traffic data

# Special Considerations
It must be noted that there are some caveats to consider when analyzing data from the Wikimedia Foundation API. For example,

1. The Pageview API is an improvement upon the Legacy Pagecounts API. It allows us to filter out views that have happened through web crawlers or automated bots.

2. October 2014 is the first full month for which mobile traffic data is available.

3. It is possible that some months return 0s or errors from the API. The documentation mentioned above can be checked for these exceptions. 

# Reproducibility
This repository contains a Jupyter notebook that is entirely reproducible. One can download it and run it from start to finish to reproduce it. Each code chunk is preceded
by a description of what the code chunk does for added clarity. For any further questions, mail the author at hramprasad98@gmail.com



