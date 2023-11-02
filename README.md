# FlexHash - Network Traffic Fingerprinting with Hybrid Locality Sensitive Hashing
Data associated with the paper as well as citation information will be released upon publication.

## Table of Contents

- [Overview](#overview)
- [Access](#access)
- [Citation](#citation)
- [Dataset Details](#dataset-details)
- [Dataset Structure](#dataset-structure)

## Overview
This repository is intended to provide documentation on the FlexHash dataset as well as the code written during the development of our research ideas. A link to the dataset is provided below.

The **FlexHash** dataset is a collection of .pcapng files which makeup the device activity for 24 devices: 8 web cameras, 8 smart plugs, and 8 smart light bulbs. Each .pcapng file contains a single packet and has been cleaned of ip/mac addresses and the checksums have been recomputed. This was done to anonymize the data and remove information which may simplify the task of classification.

## Access
Individuals interested in using the FlexHash dataset can visit the following link to download the data: 

The data is provided under the MIT license and we request that anybody utilizing the data cite our work as detailed in the citation section of this README.

## Citation

If you use the DoppelVer dataset in your work, please cite it as:

...

N. Thom, J. Thom, B. Charyyev, E. M. Hand, S. Sengupta “FlexHash: Hybrid Locality Sensitive Hashing for IoT Device Identification” IEEE Consumer Communications & Networking Conference, 2024.

BibTeX: 
```bibtex
@inproceedings{thom2024flexhash,
  author = {N. Thom and J. Thom and B. Charyyev and E. M. Hand and S. Sengupta},
  title = {FlexHash: Hybrid Locality Sensitive Hashing for IoT Device Identification},
  booktitle = {IEEE Consumer Communications \& Networking Conference},
  year = {2024},
}
```

## Dataset Details

- **Dataset Name**: FlexHash dataset
- **Version**: 1.0
- **Release Date**: 11/1/23
- **Number of Devices**: 24
- **Number of Device Types**: 3
- **Number of Pakcets**: 505,032
- **File Format**: pcapng

## Dataset Structure

The dataset is organized as follows:
``` bash
FlexHash_Dataset/
├── README.md
├── LICENSE
├── decompress_script.sh
├── cams.tar.gz
├── lights.tar.gz
├── plugs.tar.gz
├── all_devices.tar.gz
├── cams/
│ ├── cam-1/
│ │ ├── /per_packet_no_activity_cleaned
│ │ │ ├── cam_1-packet_<PACKET_ID>_<DATE>.pcapng
│ │ │ ├── cam_1-packet_<PACKET_ID>_<DATE>.pcapng
│ ├── cam-2
│ ├── etc.
├── lights/
│ ├── light-1/
│ │ ├── /per_packet_no_activity
│ │ │ ├── light-1-packet_<PACKET_ID>_<DATE>.pcapng
│ │ │ ├── light-1-packet_<PACKET_ID>_<DATE>.pcapng
│ │ ├── /per_packet_no_activity_cleaned
│ │ │ ├── light-1-packet_<PACKET_ID>_<DATE>.pcapng
│ │ │ ├── light-1-packet_<PACKET_ID>_<DATE>.pcapng
│ ├── light-2
│ ├── etc.
├── plugs/
│ ├── plug-1/
│ │ ├── /per_packet_no_activity
│ │ │ ├── plug-1-packet_<PACKET_ID>_<DATE>.pcapng
│ │ │ ├── plug-1-packet_<PACKET_ID>_<DATE>.pcapng
│ │ ├── /per_packet_no_activity_cleaned
│ │ │ ├── plug-1-packet_<PACKET_ID>_<DATE>.pcapng
│ │ │ ├── plug-1-packet_<PACKET_ID>_<DATE>.pcapng
│ ├── plug-2
│ ├── etc.
```
- `LICENSE`: The license for use of the dataset (MIT).
- `decompress_script.sh`: A bash scipt that takes as input a path to compressed files and decompresses them with multiple cores.
- `cams.tar.gz/`: A compressed file containing cleaned, no interaction packets from the YI 1080p Home Camera.
- `lights.tar.gz/`: A compressed file containing both cleaned and uncleaned, no interaction packets from the General Electric CYNC Full-Color Smart Bulb.
- `plugs.tar.gz/`: A compressed file containing both cleaned and uncleaned, no interaction packets from the Ghome Smart Plug.
- `all_devices.tar.gz/`: A compressed file containing all data.

Please note that the naming convention in the cams file is different than that found in the plugs and lights due to a typo during processing. The pcapng files for cams are of the format "<DEVICE>_<DEVICE_NUMBER>-packet..." while pcapng files for lights and plugs are of the format "<DEVICE>_<DEVICE_NUMBER>_packet...". We will address this in a future patch.

Additionally, the cams data does not come with uncleaned packets. We will attempt to add these packets in a future fix as well.

---

We hope you find the DoppelVer dataset valuable for your research or application. If you have any questions or need further assistance, please don't hesitate to contact us at nathanthom@nevada.unr.edu or jthom@unr.edu.
