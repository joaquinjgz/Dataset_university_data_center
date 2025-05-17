# Three-Phase Power System Harmonic Dataset from a University Data Center

## Overview

This dataset contains detailed electrical measurements from a three-phase power system installed in a **data center at the University of Córdoba (Spain)**. It includes active, reactive, and apparent power for each phase, along with harmonic magnitudes and phase angles for voltage and current signals up to the **11th harmonic order**.

All data was collected and processed in compliance with international standards **IEC 61000-4-30** and **IEC 61000-4-7**. Additionally, harmonic phase angles were computed using the **prevailing phasor methodology**, as described in peer-reviewed IEEE literature.

## Dataset Origin

- **Location**: University of Córdoba, Spain  
- **System Type**: Low-voltage three-phase system  
- **Environment**: Operational data center with typical nonlinear loads (e.g., servers, UPS, HVAC systems)  
- **Sampling Interval**: 10 minutes  
- **Total Duration**: 77 days  
- **Total Records**: 11,088 samples  
- **Measurement Standards and Methods**:
  - **IEC 61000-4-30:2015/A1:2022** – Power Quality measurement methods
  - **IEC 61000-4-7:2002 + AMD1:2008** – Harmonic and interharmonic measurements
  - **Prevailing Phasor Method** – For consistent harmonic phase angle interpretation

## Device and Data Acquisition

The dataset was obtained using the three-phase version of the device described in:

J. Garrido-Zafra, A. R. Gil-de-Castro, R. Savariego-Fernandez, M. Linan-Reyes, F. Garcia-Torres and A. Moreno-Munoz, "IoT Cloud-Based Power Quality Extended Functionality for Grid-Interactive Appliance Controllers," IEEE Transactions on Industry Applications, vol. 58, no. 3, pp. 3909-3921, May-June 2022. https://doi.org/10.1109/TIA.2022.3160410

This device enables cloud-based power quality monitoring with extended functionalities tailored for grid-interactive appliance controllers.

## Technical Methodology

Harmonic phase angles were calculated using the **prevailing phasor method**, which aligns each harmonic’s angle reference with the dominant fundamental component. This ensures temporal coherence and meaningful comparison across time intervals.

This method is based on:

- Blanco, A. M., Stiegler, R., Meyer, J., & Schwenke, M. (2016). *Implementation of harmonic phase angle measurement for power quality instruments*. IEEE AMPS 2016. https://doi.org/10.1109/AMPS.2016.7602811  
- Meyer, J., Blanco, A. M., Domagk, M., & Schegner, P. (2016). *Assessment of prevailing harmonic current emission in public low-voltage networks*. IEEE Transactions on Power Delivery, 32(2), 962–970. https://doi.org/10.1109/TPWRD.2016.2558187

## Contents

Each record includes:

### Power Measurements (per phase: A, B, C)
- **Active Power (pa, pb, pc, ptotal)** [W]
- **Reactive Power (qa, qb, qc, qtotal)** [VAR]
- **Apparent Power (sa, sb, sc, stotal)** [VA]
- **Frequency (frequency)** [Hz]
- **RMS Voltages** [V]
- **RMS Currents** [A]
- **Timestamp** [ms]

### Harmonic Analysis (Voltage and Current)
- **Voltage harmonic Magnitudes**: vmag1a, vmag1b, vmag1c, vmag1n, ...,  vmag11n [V]
- **Current harmonic Magnitudes**: imag1a, imag1b, imag1c, imag1n, ...,  imag11n [A]
- **Voltage harmonic Phase angles**: vph1a, vph1b, vph1c, vph1n, ...,  vph11n [º]
- **Current harmonic Phase angles**: iph1a, iph1b, iph1c, iph1n, ...,  iph11n [º]
- **Voltage prevailing ratios**: vpr1a, vpr1b, vpr1c, vpr1n, ...,  vpr11n
- **Current prevailing ratios**: ipr1a, ipr1b, ipr1c, ipr1n, ...,  ipr11n

### Format

- **File format**: CSV  
- **Total records**: 11,088 entries  
- **Time interval**: Every 10 minutes  
- **Duration**: 77 days  
- **Units**: SI units (W, VAR, VA, A, V, Hz, degrees)
- **a, b, c and n**: Phases and neutral of the three-phase system.

## Applications

- Power quality analysis in real-world systems
- Harmonic distortion research and mitigation studies
- Data-driven modeling and prediction of electrical behavior
- Training and evaluation of machine learning models for:
  - Load classification
  - Anomaly detection
  - Harmonic forecasting

## Citation

If you use this dataset, please cite it as:

J. Garrido-Zafra, R. D. Rodríguez-Cantalejo, A. Gil-de-Castro, and A. Moreno-Muñoz, "Three-Phase Power System Harmonic Dataset from a University Data Center," 2025. [Online]. Available: https://github.com/tu_usuario/tu_repositorio

