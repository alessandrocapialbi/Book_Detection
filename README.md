# Book Detection with SIFT & FLANN

This project detects multiple instances of books in scene images using SIFT (Scale-Invariant Feature Transform) for feature extraction, FLANN-based matching for efficient feature comparison, and RANSAC homography estimation to localize each book accurately.

📝 Project Overview

Given a set of model images (reference images of books) and scene images (images containing multiple books), the project:

1. Preprocesses images to improve SIFT efficiency.

2. Extracts keypoints and descriptors from models and scenes using SIFT.

3. Matches features using FLANN with Lowe's ratio test.

4. Estimates homography using RANSAC for each detected instance.

5. Draws bounding boxes around detected books, each book model assigned a distinct color.

6. Provides internal metrics such as area for potential evaluation.

⚙️ Features

Detect multiple instances of the same book in a scene.

Supports color-coded bounding boxes for each model detected.

Handles multiple scene images in order.

Internal metrics for detection quality:

Area

Easy to extend for further evaluation or visualization.

💻 Installation

Clone the repository:

git clone https://github.com/yourusername/book-detection.git
cd book-detection

Dependencies include:

OpenCV (opencv-python)

NumPy

Matplotlib

🏃 Usage

Prepare folders:

/models      # reference images of books
/scenes      # images containing multiple books


Run the detection script:

python book_detection.py


Outputs:

Terminal prints of detected instances with coordinates and area.

Visualized images with color-coded bounding boxes for each detected book.

🔧 Configuration

scale_factor: scaling applied during preprocessing (default 3.0).

min_matches: minimum number of good matches required for RANSAC (default 30).

colors: list of RGB colors for bounding boxes per model.

debug: set True to visualize keypoints, matches, masks, and intermediate steps.


📊 Metrics & Evaluation

Even without ground truth, the following internal metrics are computed per detected instance:

Aspect ratio / shape validation → filters invalid boxes

These can be used to filter unreliable detections or to analyze detector performance statistically.

🖼 Example

Scene image before detection:

Scene image after detection:

⚡ Future Improvements

Support for more models than colors with automatic cycling.

Optional clustering of multiple detections per model (for very crowded scenes).

Export detection results to JSON for further processing.

Integration with ground truth for precision/recall evaluation.

📄 License

This project is licensed under the MIT License. See the LICENSE
 file for details.
