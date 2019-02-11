# SCAVENGE Data Challenge
This repository is for the SCAVENGE Data Challenge (http://www.scavenge.eu/dissemination/data-challenge/). SCAVENGE is a ETN funded by the European Commission in the framework of H2020  under the Marie Skłodowska-Curie grant agreement No 675891.

We provide a dataset containing traces from the 4G control channel of 3 different cells. Data includes one week of observations of the mobile users both uplink (UL) and downlink (DL). Specifically, the dataset consists of 4 columns containing: Timestamp, Temporal User Identifier, Transmission direction (UL/DL) and Modulation and Coding Scheme (MCS) Index (from 1 to 29).

The student should use state-of-the-art machine learning algorithms to process this data to:

•	Perform temporal comparisons and classify the users based on observed MCS pattern;

•	Implement a temporal predictor for the MCS of the different user classes and provide a detailed analysis of its accuracy;

•	Analyze the channel quality experienced by users and try to infer their mobility patterns.

References:

[1] 3GPP TS 36.213 version 8.3.0 Release 8: Evolved Universal Terrestrial Radio Access (E-UTRA); Physical layer procedures

[2] Mohammad T. Kawser, Nafiz Imtiaz Bin Hamid, Md. Nayeemul Hasan, M. Shah Alam, and M. Musfiqur Rahman, Downlink SNR to CQI Mapping for Different Multiple Antenna Techniques in LTE, International Journal of Information and Electronics Engineering, Vol. 2, No. 5, September 2012


# Dataset description
The dataset is obtained using a sniffer that collect the data over the LTE PDCCH. This PHY channel is responsible for the communication of the scheduling information. The data is sent by the eNodeB to the user terminal. Each user is temporally identified by a RNTI (Radio Network Temporary Identifier) which is renewed after a short time of inactivity (about 10 seconds).

Data can be missing or it can contain mistakes due to measurements failures. 

•	Each folder corresponds to a different eNodeB

•	The measurements are 1 week long for each eNodeB

•	Each file contains approximately 4 hours of measurements

•	Each line corresponds to 1 millisecond (the duration of one LTE radio frame is 10 ms. One frame is divided into 10 subframes of 1 ms each)

Each file has the following 6 columns:

• ['dates','subframe_n','subframe_ind','rnti','direction','mcs']

•	dates:  timestamp of the measurements (format %Y%m%d%H%M%S)

•	subframe_n: LTE subframe number

•	subframe_ind: LTE frame in [0,9]

•	rnti: Radio Network Temporary Identifier in [0,65535]. Note that RNTI in [0,10] should be discarded and 65535 is reserved for broadcasting/paging

•	direction: 1 for downlink – 0 for uplink

•	mcs: MCS index



