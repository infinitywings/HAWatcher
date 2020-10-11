# HAWatcher Technical Report

This repository hosts a auxiliary technical report for our paper *HAWatcher: Semantics-Aware Anomaly Detection for Appified Smart Homes*. In this technical report, we present the complete capability adjacent table for the physical correlation channel as mentioned in Section 5.3.2 and the table of testing results on testbed 2,3, and 4. 

## [Physical channel capability adjacent table](physical_adjacent_tabel.xlsx)

The table is built for SmartThings (v3) platform. We acquire 73 capabilities and their descriptions from [SmartThings official developer website](https://smartthings.developer.samsung.com/docs/api-ref/capabilities.html). We define 7 physical channels: `humidity`, `temperature`, `sound`, `vibration`, `power`, `illuminance`, `air quality`. We measure the relevance between a physical channel and a capability by calculating the similarity score between the channel name and the capability's description with [pretrained word2vec model](https://code.google.com/archive/p/word2vec/). For each channel, we pick out the top 10 correlations that have the highest scores and mark them as mutually correlated at that channel. The generated 73*73 tabel can be accessed at `physical_adjacent_Table.xlsx`. In the table, If two capabilities are correlated at a physical channel, the cell with these two capabiilties as the row and column headers are filled with the name of the physical channel. Two capabilities could be correlated on more than one physical channels.

## [Testing results of testbed 2~4](Rusults_of_Testbed_2to4.pdf)
This table shows the detailed testing cases and testing results on our testbed 2, 3, and 4. We put it here because of the page limit of the paper. The table is available at `Rusults_of_Testbed_2to4.pdf`.

