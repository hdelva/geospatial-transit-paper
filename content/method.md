## Method

separation of concerns

data publishers are not necessarily data owners

* data publisher may be hired by the data owner to publically disclose the data
* data publisher might republish data as a third party to meet specific requirements
  * some applications do not require fragmentations at all
  * some applications might benefit from specific fragmentations (for example, by trip instead of by stop)

regardless of the data publisher's role -- their service has to be maintainable to keep it cost-efficient

* the world is not static, it keeps evolving 
* data published based on the real world has to evolve as well
* if the transit operator adds a stop, the published connections should accommodate this with as little friction as possible

existing work has focused on distributing stops, or trips, into discrete sets

* problem with this approach is that the clustering has to be updated to include new stops, or risk going out of sync with the source data
* we propose to partition the physical space with Voronoi
* the resulting partitions are published separately as their own resource, described as WKT literals
* connections server can ingest any partition description, fragment the source data accordingly, and generate a hydra:PartialCollectionView per partition, the tree ontology is used to describe which partial view corresponds to which geospatial partition

---

clustering

Is it even desirable to use highly balanced clusters? Does that reflect how the data is used? 

* kmeans with voronoi
  * simple chunks of equal size
* prio
  * simple chunks of varying size
* merged
  * irregular shapes of varying size
* metis
  * irregular shapes of equal size