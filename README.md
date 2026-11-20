# lecture8-image-processing-fundamentals
# Image Processing Experiment – Option A

## Project Description

This project compares three image denoising filters using MATLAB Image Processing Toolbox.

The purpose is to investigate how different filters remove Gaussian and salt-and-pepper noise while preserving image quality.

## Reference Image

- `rice.png` – MATLAB sample image used as the original reference image.
- The image was degraded using Gaussian noise and salt-and-pepper noise.

## Methods

Three denoising methods were implemented:

1. Median filter (3×3).
2. Gaussian filter (sigma 1.5).
3. Median filter (3×3) followed by Gaussian filter (sigma 1).

The random seed was set to 42 to make the noise generation reproducible.

## Results

| Filter | PSNR (dB) | SSIM |
|---|---:|---:|
| Median 3×3 | 25.370 | 0.62323 |
| Gaussian sigma 1.5 | 25.755 | 0.69213 |
| Median + Gaussian | 26.368 | 0.70515 |

The combined median and Gaussian filter achieved the best results.

## Main Conclusion

The combined filter provided the highest PSNR and SSIM values. It reduced both salt-and-pepper and Gaussian noise more effectively than either individual filter in this experiment.

## Limitation

The experiment used only one image and one noise realization. The results may differ with other images, noise levels and filter settings. PSNR and SSIM also do not fully measure the preservation of small image details.

## Files

- `analysis.mlx` – Executed MATLAB Live Script.
- `analysis.pdf` – PDF export of the experiment.
- `results/` – Saved filtered images, comparison figures and metrics.

## How to Run

1. Open MATLAB.
2. Open `analysis.mlx`.
3. Make sure the Image Processing Toolbox is available.
4. Run the entire Live Script.
5. The output figures and metrics are saved in the `results` folder.

## AI Assistance

AI assistance was used to help organize the MATLAB code, explain image denoising methods, interpret PSNR and SSIM results, and prepare the project documentation. All MATLAB code was executed and the results were checked in MATLAB.
