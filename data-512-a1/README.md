# Human Centered Data Science - A1: Data Curation

The goal of this project is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2020.

## API Documentation

Wikimedia Foundation REST API [Terms of Use](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)

The following APIs are used for collecting data:

1. The (Legacy) Page Count API, at monthly granularity: [Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts#Pagecounts)  
2. The Page View API, at monthly granularity:  [Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews#Monthly_counts)

## CSV Data Description

| Column | Description |
|--------|-------------|
| `year`   | The year of the data point |
| `month`  | The month of the data point |
| `pageview_all_views` | The total number of views (mobile + desktop) from the PageView API |
| `pageview_mobile_views` | The number of views of mobile (app + web) visits from the PageView API |
| `pageview_desktop_views` | The number of views of desktop site (web) visits from the PageView API |
| `pagecount_mobile_views` | The number of views of mobile visits from the Legacy PageCount API |
| `pagecount_desktop_views` | The number of views of desktop site visits from the Legacy PageCount API |
| `pagecount_all_views` | The total number of views (mobile + desktop) from the Legacy PageCount API |

## Miscellaneous

1. Data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.

## License

This code is available under the [MIT License](LICENSE)
