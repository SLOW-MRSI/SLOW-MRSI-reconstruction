# SLOW-MRSI reconstruction

MATLAB scripts for reconstruction, draft metabolite-map generation, and spectrIm export of 3D SLOW-MRSI data.

Download from [Download SLOW-MRSI reconstruction.zip](https://github.com/slow-mrsi/slow-mrsi-reconstruction/releases/download/20260817_v2/SLOW.recon_20260817_v2.zip)

## Workflow

1. Put the required Siemens raw-data `.dat`/Twix files in the working folder.
2. Open MATLAB in this repository folder.
3. Edit the user settings in `Run_01_recon.m` (especially `cfg.measID`).
4. Run the scripts in order:

```matlab
Run_01_recon
Run_02_map
Run_03_export
```

The scripts create `processedData/` and `data4spectrIm/` locally. These generated folders and raw MRI data are excluded from version control by `.gitignore`.

## Notes

- `Run_02_map.m` produces draft peak-integration maps for quality control and region-of-interest selection; it is not a replacement for quantitative spectral fitting.
- The code expects MATLAB with the toolboxes required by the functions used in the scripts. Parallel execution can be disabled in `Run_01_recon.m` if needed.

## Author

Dr. Guodong Weng, University of Bern.

## Citation

If you use this code in academic work, please cite:

Weng G, Radojewski P, Sheriff S, Kiefer C, Schucht P, Wiest R, Maudsley AA, Slotboom J. SLOW: A novel spectral editing method for whole-brain MRSI at ultra high magnetic field. *Magnetic Resonance in Medicine*. 2022;88(1):53–70. [doi:10.1002/mrm.29220](https://doi.org/10.1002/mrm.29220)

## License

The original reconstruction code in this repository is released under the MIT License; see [LICENSE](LICENSE).

Third-party components retain their original copyright notices and license terms. The SLOW-MRSI pulse sequence and the post-processing tools in spectrIm are distributed separately and are not covered by this repository's MIT License.
