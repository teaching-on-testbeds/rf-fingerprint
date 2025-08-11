# Localization using radio fingerprinting on AERPAW

In this experiment, we will build a practical wireless localization system using USRP software-defined radios. 

Four USRPs act as fixed transmitters, each broadcasting a distinct narrowband pilot tone at a known frequency, while a fifth USRP serves as a mobile receiver. At a set of known positions, the receiver measures the received signal reference power (RSRP) from each transmitter at the same time. These measurements are stored as short vectors — one value per transmitter — that capture the unique pattern of signal strengths at each location. This collection of location-labeled vectors forms a "radio map" of the environment. 

Later, when the receiver is at an unknown location, it collects a new RSRP vector and compares it to the radio map, finding the most similar stored pattern and using its associated coordinates as the position estimate.
