# Analysis of Digital Twin Channel Impulse Response Predictions

This project conducts a comparative analysis between channel impulse response measurements from an experimental testbed and digital twin channel impulse response measurements rendered in a Sionna ray-tracing scene for the same network.

## Overview
This repository includes:
* The main jupyter notebook for comparative analysis: **[CIRcomparison_results.ipynb](https://github.com/cjeng8771/CIRcomparison/blob/main/CIRcomparison_results.ipynb)**
* Example experimental CIR data collected using Shout on the POWDER platform at UofU: **[Dense-Deployment_Shout_meas_02-18-2025_11-38-19](https://github.com/cjeng8771/CIRcomparison/tree/main/Dense-Deployment_Shout_meas_02-18-2025_11-38-19)**
* Example digital twin CIR data for the dense deployment nodes on the POWDER platform at the UofU: **[RTcir_dd_diff.json](https://github.com/cjeng8771/CIRcomparison/blob/main/RTcir_dd_diff.json)**
* Generated results from running the comparative analysis notebook: **[results.txt](https://github.com/cjeng8771/CIRcomparison/blob/main/results.txt)**

The comparative analysis notebook includes:
* Packet generation and modulation for transmission.
* Post-processing cross-correlation of received packet with sent packet.
* Kernel distance calculations for each link.
* Axis matching between experimental CIR and RT CIR data.
* Peak-finding algorithm to isolate peaks in measured CIR data.
* Peak-matching algorithm to analyze similarities and differences between arriving peaks in RT and measured CIR data.
* Total received power calculations for both RT and measured CIR data.
* RMS delay spread calculations for both RT and measured CIR data.
* Noise floor calculations for measured CIR data to remove excess noise around peaks.

## Set Up & Run Comparative Analysis
1. Download [CIRcomparison_results.ipynb](https://github.com/cjeng8771/CIRcomparison/blob/main/CIRcomparison_results.ipynb).
2. Ensure all data files are in the same local directory as [CIRcomparison_results.ipynb](https://github.com/cjeng8771/CIRcomparison/blob/main/CIRcomparison_results.ipynb). Navigate to this directory.
3. Run the command `pip install pylfsr` if you do not have `pylfsr` installed already.
4. Open [CIRcomparison_results.ipynb](https://github.com/cjeng8771/CIRcomparison/blob/main/CIRcomparison_results.ipynb).
5. In cell 5, make any appropriate modifications to the variable declarations for `folder` and `jsonfile` to read in your experimental CIR data. Additional formatting changes may need to be made throughout the cell if the new data format differs from the example Shout data format.
6. In cell 7, modify the variable `rt_json_filename`, if needed, to express the filepath to your digital twin CIR data.
7. Run all the cells in [CIRcomparison_results.ipynb](https://github.com/cjeng8771/CIRcomparison/blob/main/CIRcomparison_results.ipynb). A summary of the results will be written to [results.txt](https://github.com/cjeng8771/CIRcomparison/blob/main/results.txt) and the detailed results, including plots, will be displayed in the output of cells 8 and 9. The results in cell 8 are displayed sequentially by TX-RX pairs.

> [!NOTE]
> Cells 5 and 7 are reading in the experimental testbed CIR measurement data and digital twin CIR data, respectively. Using the current variable declarations, the notebook will run the comparative analysis using the example data included in this project repository. If you wish to recreate our results using the provided data, make sure the folder [Dense-Deployment_Shout_meas_02-18-2025_11-38-19](https://github.com/cjeng8771/CIRcomparison/tree/main/Dense-Deployment_Shout_meas_02-18-2025_11-38-19) and file [RTcir_dd_diff.json](https://github.com/cjeng8771/CIRcomparison/blob/main/RTcir_dd_diff.json) are downloaded from the repository and in the same location as the Jupyter notebook.

## About this Work
The comparative analysis and results in this repository are part of the paper _Analysis of Digital Twin Channel Impulse Response Predictions_, which will be presented at the [2026 IEEE International Conference on RFID (RFID): National Radio Dynamic Zones: Looking Back – Looking Forward](https://2026.ieee-rfid.org/nrdz-2026/) workshop.

### Citation
Cassie Jeng and Neal Patwari, [Analysis of digital twin channel impulse response predictions](https://patwarilab.com/pub/jeng2026analysis.pdf), National Radio Dynamic Zones Workshop at the 2026 IEEE RFID Conference, 16 June 2026.
