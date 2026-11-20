# Image Processing Experiment — Option A

## Project description
This project compares three denoising methods using MATLAB's `rice.png` sample image:

1. 3-by-3 median filter.
2. Gaussian filter with sigma 1.5.
3. 3-by-3 median filter followed by Gaussian filtering with sigma 1.

The image is degraded using the exact noise settings in the assignment. The random seed is fixed at 42.

## Files
- `analysis.m` — MATLAB script containing the experiment, metrics, figures, and saving commands.
- `results/metrics.csv` — PSNR and SSIM values recorded from the completed MATLAB run.
- `results/` — the MATLAB script writes the processed images and comparison figures here when executed.

> **Important:** The assignment asks for an executed MATLAB Live Script (`analysis.mlx`) and its PDF export (`analysis.pdf`). This package contains `analysis.m`, not a genuine `.mlx` file. Open `analysis.m` in MATLAB, save/convert it as a Live Script, run all sections, and export the executed Live Script to `analysis.pdf`. Do not submit a PDF that has not been generated from your executed Live Script.

## Recorded results
These values were read from the user's MATLAB results screenshot. Re-run the script on your MATLAB installation to verify them.

| Filter | PSNR (dB) | SSIM |
|---|---:|---:|
| Median 3x3 | 25.370 | 0.62323 |
| Gaussian sigma 1.5 | 25.755 | 0.69213 |
| Median 3x3 + Gaussian sigma 1 | 26.368 | 0.70515 |

## Main conclusion
For this image and noise realization, the combined median-plus-Gaussian filter achieved the highest PSNR and SSIM. The median filter removes many isolated salt-and-pepper noise pixels, while Gaussian smoothing reduces remaining noise. The combined process can still blur fine details.

## Limitation
Only one image and one fixed noise realization were evaluated. Results may differ for other images, noise levels, and filter settings. PSNR and SSIM also do not fully represent perceived visual quality or preservation of every small detail.

## How to run
1. Open MATLAB with the Image Processing Toolbox available.
2. Make sure `rice.png` is on the MATLAB path (it is a MATLAB sample image).
3. Open and run `analysis.m`.
4. Check the Command Window for the metrics table.
5. Check the `results/` folder for the generated PNG figures and CSV file.
6. Save the work as `analysis.mlx`, run it, and export it as `analysis.pdf` for the required submission.

## AI assistance
AI assistance was used to help organize the MATLAB code, explain the denoising methods and image-quality metrics, and draft the project documentation. The MATLAB code was run in MATLAB, and the reported metric values were read from the experiment screenshot. The student should verify the results and be able to explain the implementation.
