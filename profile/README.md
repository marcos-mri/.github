# Welcome to MaRCoS-mri

<!--[![GitHub stars](https://img.shields.io/github/stars/YourOrganizationName/YourRepository.svg)](https://github.com/YourOrganizationName/YourRepository/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/YourOrganizationName/YourRepository.svg)](https://github.com/YourOrganizationName/YourRepository/issues)
[![GitHub license](https://img.shields.io/github/license/YourOrganizationName/YourRepository.svg)](https://github.com/YourOrganizationName/YourRepository/blob/main/LICENSE)
-->

## About MaRCoS

MaRCoS (MAgnetic Resonance COntrol System) is an open-source initiative developed by an international community of low-field MRI researchers. It serves as an electronic control system for magnetic resonance imaging (MRI) devices, handling pulse sequences, signal detection, and processing.

Please see the [MaRCoS Wiki](https://github.com/vnegnev/marcos_extras/wiki) for more detailed technical information, examples and tutorials/setup guides.

### Key Features

- **Inexpensive:** MaRCoS provides a cost-effective solution for MRI device control.
- **Cycle-Accurate Sequences:** Capable of handling cycle-accurate sequences without hard length limitations.
- **Rapid Event Bursts:** Supports rapid bursts of events for versatile MRI applications.
- **Arbitrary Waveforms:** Can handle arbitrary waveforms for flexible imaging techniques.
- **Adaptable:** Readily adapted to meet the requirements of academic and private institutions.

## Architecture

MaRCoS consists of three main components:

1. **Hardware:** MaRCoS runs on a [Red Pitaya SDRLab 122–16](https://redpitaya.com/sdrlab-122-16), a commercial board featuring two analog inputs for digitizing received data and two analog outputs for generating RF transmit waveforms. It interfaces with either a [GPA-FHDO](https://github.com/menkueclab) or an [OCRA1](https://zeugmatographix.org/ocra/2020/11/27/ocra1-spi-controlled-4-channel-18bit-dac-and-rf-attenutator/) four-channel gradient board.
2. **Firmware:** [MaRCoS firmware](https://github.com/vnegnev), that operates on FPGA hardware, manages real-time data streaming, synchronization, and controls various aspects, including transmit, gradient, digital I/O, and ADC data acquisition.
3. **Software:** MaRCoS can be controled at high level from a client PC through Python scripts, [Pulseq](https://pulseq.github.io/matlab.html)/[PyPulseq](https://github.com/imr-framework/pypulseq), or by the dedicated MaRCoS Graphical Environment ([MaRGE](https://github.com/mriLab-i3M/MaRGE)). MaRGE is able to interface with [RFAutoMaTE](https://github.com/josalggui/RFAutoMaTE) (Radio-Frequency Automatic Matching and Tuning Equiment).

## Publications
Guallart‐Naval, T., O’Reilly, T., Algarín, J. M., Pellicer‐Guridi, R., Vives‐Gilabert, Y., Craven‐Brightman, L., Negnevitsky, V., Menküc, B., Galve, F., Stockmann, J. P., Webb, A., & Alonso, J. (2022). Benchmarking the performance of a low‐cost magnetic resonance control system at multiple sites in the open MaRCoS community. NMR in Biomedicine, 36(1), 1–13. https://doi.org/10.1002/nbm.4825 
[![](https://img.shields.io/badge/citations-blue)](https://scholar.google.com/scholar?cites=3003368430876529690&as_sdt=2005&sciodt=0,5&hl=es&oi=gsb)

Negnevitsky, V., Vives-gilabert, Y., Algarín, J. M., Craven-Brightman, L., Pellicer-guridi, R., O'Reilly, T., Stockmann, J. P., Webb, A., Alonso, J., & Menküc, B. (2023). MaRCoS, an open-source electronic control system for low-field MRI. Journal of Magnetic Resonance, 350, 107424. https://doi.org/10.1016/j.jmr.2023.107424
[![](https://img.shields.io/badge/citations-blue)](https://scholar.google.com/scholar?cites=8536552105319785905&as_sdt=2005&sciodt=0,5&hl=es&oi=gsb)

Algarín, J. M., Guallart-Naval, T., Borreguero, J., Galve, F., & Alonso, J. (2024). MaRGE: A graphical environment for MaRCoS. Journal of Magnetic Resonance, 361, 107662. https://doi.org/10.1016/j.jmr.2024.107662 [![](https://img.shields.io/badge/citations-blue)](https://scholar.google.com/scholar?cites=9185046212591311905&as_sdt=2005&sciodt=0,5&hl=es)

Wang, H., Lou, F., Huang, Y., Gao, Y., & Zhang, X. (2024). Function Extension and Implementation of MaRCoS in Low-, Mid-, and High-Field MRI Systems: A Technical Report. https://doi.org/10.36227/techrxiv.172226905.56017383/v1

## Acknowledgments

We express our gratitude to the international community of low-field MRI researchers for their contributions to the development of MaRCoS, including: Tom O'Reilly and Andrew Webb from the Department of Radiology, Leiden University Medical Center, Leiden, The Netherlands; Benjamin Menküc from University of Applied Sciences and Arts Dortmund, Germany; Lincoln Craven-Brightman and Jason P. Stockmann from Massachusetts General Hospital (MGH), A. A. Martinos Center for Biomedical Imaging, Charlestown, MA, USA. Also a special aknoledgment to Thomas Witzel from MGH for developing [OCRA](https://www.opensourceimaging.org/project/ocra-open-source-console-for-real-time-acquisition), the predecessor of MaRCoS.  

Thank you for being a part of the MaRCoS community!

