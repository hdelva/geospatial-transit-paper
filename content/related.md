## Related work

### Mobility Data

The General Transit Feed Specification (GTFS) is, at the time of writing, the de facto standard for publishing public transit schedules. A single feed is a combination of 6 to 13 CSV files, compressed into a single ZIP archive. Its core data elements are stops, routes, trips, and stop times. Stops are places where vehicles pick up or drop off riders, routes are two or more stops that form a public transit line, trips correspond to a physical vehicle that follows a route during a specific time period, and stop times indicate when a trip passes by a stop. This data is not only useful for route planning applications, other applications include [embedding timetables in mobile applications, data visualization; accessibility analysis, and planning analysis](cite:citesAsEvidence antrim2013many).

Data dumps and query APIs are the two extremes on the [Linked Data Fragments axis](cite:cites verborgh2014querying). This axis serves as a conceptual framework to discuss trade-odds between different methods of publishing Linked Data on the Web. Data dumps put the data processing burden on the client's side, but a client that can cope with this burden is free to process it however they want. Query APIs on the other hand put the processing burden on the server side but always restrict, in some way, the way the data can be used. The [Linked Connections specification](cite:cites colpaert2015intermodal) defines a way to publish transit data that falls somewhere in between these two extremes.

Public transit schedules as LDF

### Partitioning Public Transit Networks

- - “For accelerating route planning in road networks, methods based on partitioning [14,15,19,23,24,30,31] turned out to be the most practical ones”

  - - Exploiting topology, largely static data

  - Mostly done for the purpose of speeding up route planning

  - Scalable Transfer Patterns

  - - http://ad-publications.informatik.uni-freiburg.de/ALENEX_scalable_tp_BHS_2016.pdf
    - Uses conventional graph clustering algorithms to create sets of stops
    - k-Means clustering:
      Some  methods  for  classification and  analysis  of  multivariate  observations.
    - Merge-based clustering:
      Creating graph partitions for fast optimum route planning.
    - METIS:
      A fast and high quality multilevel scheme for partitioning irregular graphs.
    - PUNCH
      Graph partitioning with natural cuts.

  - CSAccel 

  - - https://arxiv.org/pdf/1703.05997.pdf

    - Uses KaFFPa:

    - - Think Locally, Act Globally: Highly Balanced Graph Partitioning

    - Found it superior to METIS

  - HypRAPTOR

  - - http://drops.dagstuhl.de/opus/volltexte/2017/7896/pdf/OASIcs-ATMOS-2017-8.pdf
    - Uses metis as well
    - But uses it to create sets of trips

  - Focus so far has been on being robust to changes in the timetable, such as working around train delays.

  - New stops, or trips, will not be used until the preprocessed is repeated.

### Voronoi Partinioning

yes