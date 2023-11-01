# FlexHash - Network Traffic Fingerprinting with Hybrid Locality Sensitive Hashing
Data associated with the paper as well as citation information will be released upon publication.

## Table of Contents

- [Overview](#overview)
- [Access](#access)
- [Dataset Details](#dataset-details)
- [Data Description](#data-description)
- [Dataset Structure](#dataset-structure)
- [Citation](#citation)
- [License](#license)
- [Code](#code)

## Overview
This repository is intended to provide documentation on the FlexHash dataset as well as the code written during the development of our research ideas. A link to the dataset is provided below.

The **FlexHash** dataset is a collection of .pcapng files which makeup the device activity for 24 devices: 8 web cameras, 8 smart plugs, and 8 smart light bulbs. Each .pcapng file contains a single packet and has been cleaned of ip/mac addresses and the checksums have been recomputed. This was done to anonymize the data and remove information which may simplify the task of classification.

## Access
Individuals interested in using the FlexHash dataset can visit the following link to download the data: 
The data is provided under the MIT license and we request that anybody utilizing the data cite our work as detailed in the citation section of this README.

## Dataset Details

- **Dataset Name**: FlexHash dataset
- **Version**: 1.0
- **Release Date**: 11/1/23
- **Number of Devices**: 24
- **Number of Device Types**: 3
- **Number of Pakcets**: 27,430
- **File Format**: pcapng

## Data Description

The DoppelVer dataset includes the following features and attributes:

- Doppelganger pairs: annotation of which identities are doppelgangers to one another.
- Verification Pairs: protocols for evaluating face verification, including paths to two images and a label denoting if the images depict the same of different identities. 

## Dataset Structure

The dataset is organized as follows:
``` bash
FlexHash_Dataset/
├── README.md
├── decompress_script.sh
├── cams.zip
├── lights.zip
├── plugs.zip
├── Images/
│ ├── Original_Images/
│ │ ├── Abigail Spencer/
│ │ │ ├── 00.jpg
│ │ │ ├── 01.jpg
│ │ │ ├── etc.
│ │ ├── etc./
│ │ │ ├── 00.jpg
│ │ │ ├── 01.jpg
│ │ │ ├── etc.
│ ├── CCA_Images/
│ │ ├── Abigail Spencer/
│ │ │ ├── 00_0.jpg
│ │ │ ├── 01_0.jpg
│ │ │ ├── etc.
│ │ ├── etc./
│ │ │ ├── 00_0.jpg
│ │ │ ├── 00_1.jpg
│ │ │ ├── etc.
```
- `cams.zip/`: A compressed file containing all original images and pre-processed images.
- `lights.zip/`: A compressed file containing all original images and pre-processed images.
- `plugs.zip/`: A compressed file containing all original images and pre-processed images.
- `cams/`: The resultant directory after decompressing the Images.zip file.
- `lights/`: The resultant directory after decompressing the Images.zip file.
- `plugs/`: The resultant directory after decompressing the Images.zip file.

## Citation

If you use the DoppelVer dataset in your work, please cite it as:

...

N. Thom, J. Thom, B. Charyyev, E. M. Hand, S. Sengupta “FlexHash: Hybrid Locality Sensitive Hashing for IoT Device Identification” IEEE Consumer Communications & Networking Conference, 2024.

BibTeX: [^thom2024flexhash].

...

[^thom2024flexhash]: Thom, N., Thom, J., Charyyev, B., Hand, E. M., & Sengupta, S. (2024). "FlexHash: Hybrid Locality Sensitive Hashing for IoT Device Identification." In IEEE Consumer Communications & Networking Conference.

---

We hope you find the DoppelVer dataset valuable for your research or application. If you have any questions or need further assistance, please don't hesitate to contact us at nathanthom@nevada.unr.edu or jthom@unr.edu.
