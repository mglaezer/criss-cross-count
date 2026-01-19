# Backgammon - Criss Cross Count "The Trainer" for MacOS

**Web version:** https://mglaezer.github.io/criss-cross-count/

## Table of Contents
- [Synopsis](#synopsis)
- [CCC Summary](#ccc-summary)
- [Definitions](#definitions)
- [General Formula](#general-formula)
  - [Criss-Cross Count](#criss-cross-count)
  - [Distribution Correction](#distribution-correction)
  - [Fine Adjustment](#fine-adjustment)
- [References](#references)
- [Features](#features)
- [Screenshots](#screenshots)
- [Gatekeeper Notice](#gatekeeper-notice)
- [Installation & Compiling from Source](#installation--compiling-from-source)
- [Usage](#usage)
- [Known Issues](#known-issues)
- [Privacy](#privacy)
- [Disclaimer](#disclaimer)

## Synopsis
This macOS application serves as a trainer for **Max Glaezer's Criss Cross Count**.  
It includes the **complete list of reference positions** and can also **generate random positions** for practice.


## CCC Summary

The Criss-Cross pipcount system is based on dividing the backgammon board into eight so-called *slices*, each consisting of three points.  
Each slice is assigned a numerical value, structured symmetrically, allowing for plus/minus adjustments. Opposing slices always sum to $5$.

This system enables a quick determination of the relative pipcount.



## Definitions

- $n_i$: Number of checkers in slice $i$  
- $s_i$: Slice value in the Criss-Cross system  
- There are 8 slices in total  
- Reference distribution: 15 checkers per side



## General Formula

### Criss-Cross Count

$$
C = \sum_{i=1}^{8} n_i \cdot s_i
$$

### Distribution Correction

$$
\Delta = (\text{bottom player checkers on top}) - (\text{top player checkers at bottom})
$$

$$
C_{\text{corr}} = C + 5 \cdot \Delta
$$

### Fine Adjustment

$$
C_{\text{final}} = C_{\text{corr}} + \varepsilon
$$



## References
- [Max Glaezer's Paper](https://docs.google.com/document/d/1HVZ16CDjVmcH_fK2l3giedqwForgpnLmB5aRF_j1pmc/edit?tab=t.0#heading=h.wc0r227g8i1a) – Original reference list and methodology  (as of 18 January 2026)
- [Nack Ballard's Extended Explanation](https://www.bgonline.org/forums/webbbs_config.pl?noframes;read=208404) – Further details and discussion  (as of 18 January 2026)



## Features

| Shortcut       | Action                                                                 |
|----------------|------------------------------------------------------------------------|
| **⌘ + L** | Display a **random reference position** (PDF reference shown in title) |
| **⌘ + R** | Generate a **random position**                              |
| **⌘ 1-4** | Show a **visual representation** of the respective step               |
| **⌘ + D** | Display the **full calculation** for the current position             |
| **⌘ + E** | Export **XGID** to Clipboard             |


## Screenshots

![CCC](https://github.com/user-attachments/assets/b65ebf63-6cbf-467e-a4a9-2b9ed4ce79df)
![CCC](https://github.com/user-attachments/assets/91dcfa98-e93d-4d1b-a58f-4cf17af1e915)
![Full CCC](https://github.com/user-attachments/assets/24f03017-0db3-48c5-9830-049949834cc7)


## Gatekeeper Notice

The release version of this application (**DMG**) is **not signed** by an Apple Developer certificate.  
As a result, macOS Gatekeeper will prevent the app from opening by default.  

To run the app, you may need to:

1. Control-click (right-click) the app icon and select **Open**  
2. Confirm that you want to open the app despite the warning  
3. Future launches should then work normally

> This is a standard precaution for unsigned macOS applications and does not indicate a security issue with the app itself.


## Installation & Compiling from Source

1. **Download the source code**  
2. Make the build script executable:
   ```bash
   chmod a+x ./do_app.sh
3. Run the build script:
   ```bash
   ./do_app.sh
4. After successful compilation, the app will be available in the bin/ directory.
5. Launch the app by opening the compiled file from bin/.

## Usage

- Launch the application on macOS.  
- Use the keyboard shortcuts from the **Features** table to navigate reference positions, random exercises, or full calculations.  
- Train systematically with the reference list or challenge yourself with random positions.

## Known Issues

- Menubar is not always visible (Mac OS 11)

## Privacy

- The application **does not collect any data**  
- The application **does not transmit any files**

## Disclaimer

The use of this application is **entirely at your own risk**.  
The author **assumes no liability** for any direct or indirect damages, losses, or consequences arising from the use of this software.  
By using this application, you acknowledge and accept these terms.


