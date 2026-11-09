# Tuning Methodology

## Baseline (V1)
The baseline is a 32-filter Poweramp-style PEQ profile derived from the 192 kHz measurement dataset in the supplied frequency-response workbook. The profile uses one Low Shelf filter and 31 Peaking filters. The reported fitting range is 20 Hz to 9 kHz, with no correction above 9 kHz.

The source workbook describes a fixed center-frequency distribution, RBJ biquad model, and regularization strategy, with gain and Q independently fitted. Its reported RMSE is 0.174 dB. This metric describes model fit to the target correction curve; it does not describe actual in-ear response error.

## Low-frequency experiment (V2-A)
V2-A was created by changing only the gain values of Filters 1–7. All center frequencies, Q values, filter types, Filters 8–32, and Preamp remain identical to V1. This isolates a modest low-frequency adjustment for listening comparison.

## Listening-led evaluation
The cannon-effect recording associated with Tchaikovsky's *1812 Overture* was used as a demanding transient/low-frequency listening example. An initial listener report described stronger perceived impact and a more convincing sense of a compact sound core expanding outward and becoming less dense during decay.

This is a subjective observation. It does not establish that the earphone's acoustic output, distortion, or spatial reproduction has objectively improved. Further evaluation with vocals, acoustic instruments, piano, bass, and percussion is pending.

## Interpretation limits
A digital PEQ simulation can calculate how a linear filter changes the recorded waveform. It cannot, by itself, predict the acoustic output of a particular earphone at the eardrum. Driver excursion limits, nonlinear distortion, fit/seal, firmware DSP, playback volume, and any dynamic processing can all affect the result.
