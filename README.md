# Experimental-Modal-Analysis-of-a-Cantilever-Beam

MATLAB implementation of experimental modal analysis using impact-hammer excitation and acceleration measurements from ten equally spaced accelerometers mounted along a cantilever beam.

## Methodology

- Estimated ten frequency response functions (FRFs) using auto-spectral density (ASD) and cross-spectral density (CSD) functions.
- Identified the first five natural frequencies using peak detection (findpeaks) and estimated the corresponding damping ratios using the peak amplitude method.
- Extracted the first four mode shapes from the imaginary part of the selected FRF.
- Performed modal analysis using MATLAB's modalfrf, modalsd, and modalfit functions, including stabilization diagram construction and model order selection.
- Compared the modal parameters and reconstructed FRF obtained through MATLAB's built-in functions with those from the independently implemented procedure to assess the consistency of the results.

## Repository Contents

- Experimental_Data.dat – Experimental force and acceleration measurements.
- Modal_Analysis.m – Main MATLAB script for FRF estimation, modal parameter identification, and result visualization.
- intersections.m – External utility function by Douglas M. Schwarz, used for damping ratio estimation (include only if its license permits redistribution).

## How to Run

- Place the experimental data file and the required MATLAB function files in the same directory.
- If intersections.m is not included, download it from MATLAB Central File Exchange and add it to the MATLAB path.
- Open and run Modal_Analysis.m in MATLAB.

The script performs the FRF estimation, modal parameter identification, and comparison of the two analysis approaches.

## External Reference

Douglas M. Schwarz, Fast and Robust Curve Intersections, MATLAB Central File Exchange, Version 2.0 (2017).
