# Welcome to MaRCoS-mri

<!--[![GitHub stars](https://img.shields.io/github/stars/YourOrganizationName/YourRepository.svg)](https://github.com/YourOrganizationName/YourRepository/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/YourOrganizationName/YourRepository.svg)](https://github.com/YourOrganizationName/YourRepository/issues)
[![GitHub license](https://img.shields.io/github/license/YourOrganizationName/YourRepository.svg)](https://github.com/YourOrganizationName/YourRepository/blob/main/LICENSE)
-->

## About MaRCoS

MaRCoS (MAgnetic Resonance COntrol System) is an open-source initiative developed by an international community of low-field MRI researchers. It serves as an electronic control system for magnetic resonance imaging (MRI) devices, handling pulse sequences, signal detection, and processing.

### Key Features

- **Inexpensive:** MaRCoS provides a cost-effective solution for MRI device control.
- **Cycle-Accurate Sequences:** Capable of handling cycle-accurate sequences without hard length limitations.
- **Rapid Event Bursts:** Supports rapid bursts of events for versatile MRI applications.
- **Arbitrary Waveforms:** Can handle arbitrary waveforms for flexible imaging techniques.
- **Adaptable:** Readily adapted to meet the requirements of academic and private institutions.

## Architecture

MaRCoS consists of three main components:

1. **Hardware:** At the core of MaRCoS is the Red Pitaya SDRLab 122–16, a commercial board featuring two analog inputs for digitizing received data and two analog outputs for generating RF transmit waveforms. With a bandwidth of 50 MHz, the SDRLab is well-suited for proton MRI at field strengths of up to 1.17 Tesla. MaRCoS interfaces with either a GPA-FHDO (https://github.com/menkueclab) or an OCRA1 (https://zeugmatographix.org/ocra/2020/11/27/ocra1-spi-controlled-4-channel-18bit-dac-and-rf-attenutator/) four-channel gradient board, providing flexibility for various experimental setups. The architecture of MaRCoS sets it apart by allowing unlimited, cycle-accurate sequences, accommodating rapid bursts of events, and facilitating the creation of arbitrary waveforms, including RF and gradients. This hardware configuration supports independent control of frequency, phase, and amplitude for different TX and RX channels in each repetition. MaRCoS stands out as the first inexpensive system capable of these features, empowering researchers with specialized experiments and offering unique capabilities.
2. **Firmware:** MaRCoS firmware, tailored for magnetic resonance imaging (MRI) devices, operates on FPGA hardware to execute instructions from the MaRCoS server. It manages real-time data streaming, synchronization, and controls various aspects, including transmit, gradient, digital I/O, and ADC data acquisition. The FIFO-based control system simplifies instruction specification, enabling the client software on the PC to handle complex sequence timing and design without low-level changes. This firmware plays a crucial role in achieving MaRCoS' goals, making it a versatile solution for diverse pulse sequences in low-field MRI applications.
3. **Software:** The MaRCoS Graphical Environment (MaRGE) is a graphical user interface pursuing three primary goals: firstly, to enhance user interaction with the MaRCoS system, fostering to operators with varying technical expertise levels; secondly, to optimize MaRCoS functionality for both laboratory and medical environments, tailoring its capabilities to diverse research and clinical needs; and thirdly, to provide a comprehensive set of tools for image post-processing. This software prioritizes user-centric design, ensuring a positive and efficient experience for all users.

## Publications
Guallart‐Naval, T., O’Reilly, T., Algarín, J. M., Pellicer‐Guridi, R., Vives‐Gilabert, Y., Craven‐Brightman, L., Negnevitsky, V., Menküc, B., Galve, F., Stockmann, J. P., Webb, A., & Alonso, J. (2022). Benchmarking the performance of a low‐cost magnetic resonance control system at multiple sites in the open MaRCoS community. NMR in Biomedicine, 36(1), 1–13. https://doi.org/10.1002/nbm.4825

Negnevitsky, V., Vives-gilabert, Y., Algarín, J. M., Craven-, L., Pellicer-guridi, R., Reilly, T. O., Stockmann, J. P., Webb, A., Alonso, J., & Menküc, B. (2023). MaRCoS, an open-source electronic control system for low-field MRI. Journal of Magnetic Resonance, 350, 107424. https://doi.org/10.1016/j.jmr.2023.107424


## Acknowledgments

We express our gratitude to the international community of low-field MRI researchers for their contributions to the development of MaRCoS. We extend our sincere gratitude to Vlad Negnevitsky (https://github.com/vnegnev) for his exceptional contributions and unwavering dedication in propelling MaRCoS forward.

Thank you for being a part of the MaRCoS community!

