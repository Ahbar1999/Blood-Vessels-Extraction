# Blood Vessel Segmentation in Fundus Images

## Overview
This project implements blood vessel segmentation from retinal fundus images using Python and OpenCV. The segmentation pipeline includes image preprocessing, edge detection, and morphological operations to accurately extract blood vessels.

## Requirements
- Python 3.x
- OpenCV (`cv2`)
- NumPy
- Matplotlib (optional, for visualization)


Segmented images will be saved in the `output/` directory.

## Methodology

The segmentation involves these main steps:

### 1. Image Preprocessing
- Convert RGB fundus image to grayscale.
- Apply Gaussian Blur to reduce noise.
- Thresholding (`cv2.THRESH_TOZERO_INV`) enhances vessel visibility.

### 2. Edge Detection
- Perform Canny edge detection at two thresholds (15-50 and 100-200).
- Subtract the two edge maps to highlight vessel structures.

### 3. Morphological Operations
- Dilate and erode using elliptical kernels:
  - Dilation connects vessel segments.
  - Erosion removes small artifacts.

### 4. Output Generation
- Save final segmented images as `.png` files in `output/`.

## Visualization
Intermediate results (blurred grayscale and final segmented images) are displayed for visual assessment.

## Applications
Useful for:
- Diabetic retinopathy detection.
- Retinal disease analysis.
- Ophthalmology screening systems.

## Future Improvements
Possible enhancements:
- Integrate deep learning models for higher accuracy.
- Adaptive thresholding techniques.
- Quantitative evaluation metrics.

## License
MIT License.


