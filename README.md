# Redmi Buds 8 Pro – PEQ Tuning Project

Community-oriented parametric EQ (PEQ) profiles and measurement-based tuning notes for the **Redmi Buds 8 Pro**.

**Language / 语言:** [简体中文](README.zh-CN.md)

> **Status:** V1 is the measurement-derived baseline. V2-A is the current default PEQ in the project owner's Redmi K-Pad + Redmi Buds 8 Pro + Poweramp setup, based on the listening evaluation documented in [Listening Notes](documentation/listening-notes.md). V2-A remains a personal listening-based revision, not an official Xiaomi/Redmi product or profile.

## Profiles

| Profile | Description | Preamp | Status |
|---|---|---:|---|
| [V1 – 192 kHz / 32-band](profiles/Poweramp/V1-192k-32Band.txt) | Baseline profile fitted to the ReaLab Target Response (2024) using the 192 kHz measurement dataset | -1.5 dB | Baseline |
| [V2-A – 192 kHz / 32-band](profiles/Poweramp/V2-A-192k-32Band.txt) | V1-derived revision with a modest gain recovery in the low-frequency filters | -1.5 dB | Project owner's current default |

Parameter comparison:
- [CSV: V1 vs V2-A](profiles/Poweramp/PEQ-parameters-V1-V2-A.csv)
- [Excel: V1 vs V2-A](profiles/Poweramp/PEQ-parameters-V1-V2-A.xlsx)

## V2-A changes

V2-A changes only the gain values of Filters 1–7. Filter type, center frequency, Q, Filters 8–32, and Preamp remain unchanged.

| Filter | Type | Frequency | V1 Gain | V2-A Gain | Change |
|---:|---|---:|---:|---:|---:|
| 1 | Low Shelf | 35 Hz | -2.10 dB | -1.60 dB | +0.50 dB |
| 2 | Peaking | 38.0 Hz | -1.44 dB | -0.64 dB | +0.80 dB |
| 3 | Peaking | 45.6 Hz | -1.74 dB | -0.94 dB | +0.80 dB |
| 4 | Peaking | 54.7 Hz | -2.28 dB | -1.48 dB | +0.80 dB |
| 5 | Peaking | 65.6 Hz | -2.37 dB | -1.57 dB | +0.80 dB |
| 6 | Peaking | 78.7 Hz | -1.98 dB | -1.18 dB | +0.80 dB |
| 7 | Peaking | 94.3 Hz | -1.31 dB | -0.51 dB | +0.80 dB |

The change was motivated by listening to the opening cannon sound effects from a recording associated with Tchaikovsky's *1812 Overture*. The initial subjective report described a more convincing sense of a compact explosive core expanding outward, with a less dense decay. This is a listening observation, not an objective measurement of spatial accuracy.

## Measurement and tuning basis

- The baseline profile was fitted to the ReaLab Target Response (2024) using the project's 192 kHz measurement dataset.
- Filter structure: 1 Low Shelf + 31 Peaking filters.
- Fit range: 20 Hz–9 kHz; no compensation above 9 kHz.
- The source workbook reports a model-fit RMSE of 0.174 dB. This is the numerical fitting error of the model, **not** a real-ear measurement error or a guarantee of perceived sound quality.
- V2-A is a controlled listening-led revision derived from V1, not a new target-response fit.

Supporting source measurement data was used during development but is not redistributed in this repository pending confirmation of its reuse terms. See [Measurement Data](measurements/README.md).

## Installation

1. Download the desired `.txt` profile.
2. Import or manually enter the filters in a compatible parametric EQ application such as Poweramp Equalizer.
3. Confirm that the application interprets `LSC` as Low Shelf and `PK` as Peaking.
4. Keep the Preamp value shown in the profile.
5. Listening level, ear-tip seal, fit, firmware, codec, and playback processing can affect results.

The text profiles use a readable AutoEQ/Poweramp-style filter notation. Compatibility may vary by application version.

## Important limitations

- PEQ changes the signal's frequency response; it cannot increase the physical displacement capability or maximum clean output of the earphone driver.
- Digital filter simulations do not predict the earphone's actual acoustic output, distortion, internal DSP, or dynamic limiting.
- The 192 kHz label refers to the measurement dataset used to derive the profile. It does **not** mean Bluetooth transmits audio at 192 kHz.
- Results may vary with individual ear fit, ear tips, hearing, firmware, source device, and listening volume.
- Avoid excessive listening levels. Increased bass boost can increase driver excursion and distortion.

## Repository contents

- `profiles/Poweramp/` – importable text profiles and parameter comparison.
- `measurements/` – notes about supporting frequency-response data.
- `analysis/1812-overture/` – notes about the cannon-effect test; copyrighted audio is not redistributed here.
- `documentation/` – tuning method and listening notes.

## License

Unless otherwise noted, original documentation, parameter compilations, and project-authored analysis in this repository are licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**. See [LICENSE](LICENSE).

Third-party measurement data, target curves, screenshots, product names, and other referenced materials may have separate rights or terms. Their inclusion or mention does not imply that they are relicensed under CC BY 4.0. Check the source terms before redistributing those materials.

Redmi and Xiaomi are trademarks of their respective owners. This is an independent, unofficial project and is not affiliated with or endorsed by Xiaomi.
