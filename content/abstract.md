## Abstract
<!-- Context - bigger picture     -->
The more unique your mobility needs are, the less likely you are to find an existing data service that suits your needs. Therein lies the beauty of publishing the raw data; data owners don't have to anticipate everyone's needs if third parties can fill in the gaps.
<!-- Need - gap we try to solve   -->
Public transit operators often publish their data as a large data dump under the assumption that data consumers want to process the entire dataset anyway. Unfortunately, developers with limited computational resources can have trouble ingesting all this data. Linked Connections is an alternative publishing scheme that fragments the data by the connections' departure times. This enables data consumers to be more selective in the data they choose to process. This is already a good improvement over monolithic data dumps, but each fragment still contains data from the entire operator's service area.
<!-- Task - what we did           -->
We build upon the idea of Linked Connections by fragmenting geospatially as well as by departure time. Ideally, our publishing scheme must work in the case  where the data publisher is not the data owner. This means that the fragmentation method should be robust to changes in the original data, such as the deletion or the addition of stops. Contrary to the conventional approach of generating discrete sets of stops, we propose generating geospatial partitions instead. These partitions are published alongside the transit data itself, allowing data consumers to infer which fragments contain which data. 
<!-- Object       -->
In this paper we explore conventional clustering methods such as k-Means and METIS, alongside two simple methods of our own that are custom-tailored to public transit data. We compare the effectiveness of each for the use case of client-side route planning.
<!-- Findings     -->
Our results show that the number of generated partitions greatly affects the performance of route planning. Even with only 4 partitions queries get answered 2.2 times faster while also requiring 2.6 times less data, and 16 partitions already yield 4.4 times faster queries and 7.2 times less required data. Interestingly enough the choice of fragmentation strategy has less impact; a simple clustering method such as k-Means results in 5% faster queries than a complex method such as METIS.
<!-- Conclusion   -->
These results show that data publishers don't have to train the perfect clustering model -- even a simple approach is effective. 
<!-- Perspectives -->
Consequently, this increases the likelihood that such a publishing scheme may be adopted. 