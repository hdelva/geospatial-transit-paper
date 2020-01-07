## Related work

### Linked Data Fragments

Share the load

### Linked Connections

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