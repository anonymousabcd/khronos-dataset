# Khronos-dataset

Data is provided to the review process for paper Khronos: A Real-Time Indexing Framework for Time Series Databases on Large-Scale Performance Monitoring Systems.

The data contains the following four datasets:

(1) ASI: Time series data corpus collected from a container scheduling system.  
(2) HI: Time series data corpus collected from a resource scheduling system.  
(3) IG: Time series data corpus collected from an online graph engine.  
(4) TPP: Time series data corpus collected from a search and recommendation platform.  

The demo directory contains three demo segments of each dataset, while the entire directory contains all segments for three consecutive days. As the paper focuses on the index construction process of time series meta, we are providing the meta data of each series in one segment.

The segment is an [ORC](https://github.com/apache/orc) file with ZSTD compression that can be parsed by an [official tool](https://github.com/apache/orc/blob/main/tools/src/FileContents.cc). Each segment has three columns. The first column is the series key (including one metric and a list of tag key and tag value pairs), while the second and third columns are the start and end timestamps of the corresponding time series, respectively. Note that the data has been processed through anonymization techniques to preserve privacy.
