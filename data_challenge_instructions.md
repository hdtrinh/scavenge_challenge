# SCAVENGE DATA CHALLENGE

## Dataset description

The dataset is obtained using a sniffer that collect the data over the LTE PDCCH. This PHY channel is responsible for the communication of the scheduling information. The data is sent by the eNodeB to the user terminal. Each user is temporally identified by a RNTI (Radio Network Temporary Identifier) which is renewed after a short time of inactivity (about 10 seconds).
Data can be missing or it can contain mistakes due to measurements failures. 

•	Each folder corresponds to a different eNodeB

•	The measurements are 1 week long for each eNodeB

•	Each file contains approximately 4 hours of measurements

•	Each line corresponds to 1 millisecond (the duration of one LTE radio frame is 10 ms. One frame is divided into 10 subframes of 1 ms each)

•	Each file has the following 6 columns:


['dates','subframe_n','subframe_ind','rnti','direction','mcs']


•	dates:  timestamp of the measurements (format %Y%m%d%H%M%S)

•	subframe_n: LTE subframe number

•	subframe_ind: LTE frame in [0,9]

•	rnti: Radio Network Temporary Identifier in [0,65535]. Note that RNTI in [0,10] should be discarded and 65535 is reserved for broadcasting/paging

•	direction: 1 for downlink – 0 for uplink

•	mcs: MCS index




