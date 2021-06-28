# Searching Data
---

## Static data vs. Time Series Data

Static is typically data which may grow or change slowly, like a catalog or an inventory of items.

On the other hand, you can store time series data as well. Time series is moire specific to things like logging or metric data. Data that generally grows rapidly. Typically this type of data isn't changed. 

---

## Static Dataset

Static datasets in this will be blog posts, data like this does change periodically, but not often. This information has a lot of information such as author's name, title and body of the post.

---

## Time series Dataset

The example below is a time series dataset that are web access log files from elastic blogs.

```json
{
  "@timestamp" : "2017-05-11T01:26:16.590Z",
  "user_agent" : "Amazon CloudFront",
  "originalUrl" : "/kr/blog/0-17-1-released",
  "response_size" : 40534,
  "host" : "server1",
  "geoip" : {
    "country_code2" : "US",
    "country_name" : "United States",
    "continent_code" : "NA",
    "country_code3" : "US",
    "location" : {
      "lon" : -77.4728,
      "lat" : 39.0481
    },
    "region_name" : "Virginia",
    "city_name" : "Ashburn"
  },
  "status_code" : 200,
  "level" : "info",
  "method" : "GET",
  "runtime_ms" : 224,
  "http_version" : "1.1",
  "language" : {
    "url" : "/blog/0-17-1-released",
    "code" : "ko-kr"
  }
}
```

---

## Ingesting the Log Data

To ingest the log files we can use Filebeat. This will convert the log files into the JSON format that Elasticsearch requires and send the bulk requests to push them in 50 logs at a time.