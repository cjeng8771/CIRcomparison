# CIRcomparison
Code for comparative analysis between channel impulse response measurements from experimental testbed and digital twin channel impulse response measurements for the same network rendered in a Sionna ray-tracing scene.

Code notebook includes:
* Packet generation and modulation for transmission.
* Post-processing cross-correlation of received packet with sent packet.
* Kernel distance calculations for each link.
* Axis matching between experimental CIR and RT CIR data.
* Peak-finding algorithm to isolate peaks in measured CIR data.
* Peak-matching algorithm to analyze similarities and differences between arriving peaks in RT and measured CIR data.
* Total received power calculations for both RT and measured CIR data.
* RMS delay spread calculations for both RT and measured CIR data.
* Noise floor calculations for measured CIR data to remove excess noise around peaks.