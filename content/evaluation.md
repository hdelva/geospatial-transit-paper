## Evaluation

Server and client are two machines on the same local network, with a default 20 ms added per request

No caching to isolate the impact of the clustering methods, cacheability of files is simulated separately

<figure>
    <img src="./img/elapsed_boxen.svg" width="100%">
    <figcaption>elapsed</figcaption>
</figure>

<figure>
    <img src="./img/downloaded_boxen.svg" width="100%">
    <figcaption>downloaded</figcaption>
</figure>

### Cacheability

no considerable change in total data size, so a cache that is big enough to cache the original data can also cache the partitioned data

One thing that does change is how fast the cache will fill up - you need at least one request per fragment to fill up a web cache. 

The different partitioning schemes will also diverge when the cache is too small to contain all the data. Filling a cache with fine-grained data will take longer, but the cached data is more likely to be relevant. For example, a purely temporal fragmentation strategy will contain data for the entire operator's service area, even if one region is significantly less often requested. 

To evaluate how fast a cache is filled we replay a small amount of requests on an empty cache, and do this many times. To evaluate how often relevant data is evicted from the cache we do the same, but on an already warmed up cache.

<figure>
    <img src="./img/cold_cache.svg" width="100%">
    <figcaption>cold</figcaption>
</figure>





<figure>
    <img src="./img/warm_cache.svg" width="100%">
    <figcaption>warm</figcaption>
</figure>