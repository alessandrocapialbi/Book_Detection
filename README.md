# Book Detection with SIFT & FLANN

This project detects multiple instances of books in scene images using **SIFT feature extraction**, **FLANN-based feature matching**, and **RANSAC homography**. It visualizes detected books with color-coded bounding boxes and computes internal metrics to assess detection quality.

---

## Features

- Detect multiple instances of the same book in a scene.
- Color-coded bounding boxes per model.
- Iterative detection for crowded scenes.
- Internal quality metrics:
  - Number of good matches
  - Inlier ratio from RANSAC
  - Reprojection error
  - Bounding box area and aspect ratio
- Debug mode for visualizing keypoints, matches, and masks

---

## Dependencies:

1. OpenCV (opencv-python)

2. NumPy

3. Matplotlib

4. Jupyter 

## Usage

1. Put the dataset.zip file under a new folder in your named as you want. Just remember to change the path when extracting in the notebook.
   
2. Open the notebook:
   ```sh
   jupyter notebook book_detection.ipynb
   ```
3. Execute cells sequentially.

4. Provide paths for /models and /scenes folders if required.

Outputs:

Number of instances for each model and bounding boxes with drawn on scene images with different colors.

## Configuration

scale_factor: scale applied during preprocessing (default 3.0)

min_matches: minimum number of good matches for RANSAC (default 30)

colors: list of RGB colors for bounding boxes

debug: True to visualize intermediate results (keypoints, matches, masks)

## Example

<p float="left">
  <h1> Before detection </h1><img src="https://github.com/alessandrocapialbi/Book_Detection/blob/main/scene_18.jpg" width="400" />
  <h1> After detection </h1><img src="https://github.com/alessandrocapialbi/Book_Detection/blob/main/scene18_bounding_boxes.png" width="400" />
</p>

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.




