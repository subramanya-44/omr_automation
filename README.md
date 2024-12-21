# Sign Language Detector using Python

## Techniques Used
- Document Scanner
- Sorting contours
- Perspective transform for a top-down view

## Steps Involved
1. Detect OMR sheet
2. Apply perspective transform
3. Extract bubbles
4. Sort bubbles row-wise
5. Identify answer bubbles
6. Compare with the correct answers for all rows

## Assumptions
- OMR sheet is the main focus of the image.
- All 4 edges of the OMR sheet are visible.
- Largest rectangle in the image is the OMR document.

## Implementation Details
- **Answer Keys**: Stored in a Python dictionary.
- **Edge Detection**: Canny edge detection with Gaussian blur for noise reduction.
- **Top-Down View**: Achieved using OpenCV perspective transform.
- **Thresholding**: Used Otsu’s method.
- **Bubble Detection**: Bubbles identified based on aspect ratio ≈ 1.
- **Filled Bubble Detection**: Determined using bitwise masking and pixel shading.

## Requirements
- **Python**: 3.7.3
- **OpenCV**: 4.1.0
- **NumPy**: 1.16.4
- **Imutils**: 0.5.2

## Run Command
```bash
python test_grader.py --image images/test_02.png
![OMR Grading Output](output/test_result.png)
