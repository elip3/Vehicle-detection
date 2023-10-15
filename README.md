# Vehicle-detection
This project has two main components: vehicle detection and tracking using Kalman filters and HOG+SVM, and lane detection using computer vision techniques.

# Module 1. 
The vehicle detection consists of the following files.

Desc.py responsible for computing HOG
Detect.py main module which our main test file calls. This wraps the descriptor, sliding window, Kalman filter and threshold methods in one file

Scan.py performs sliding window detection at different scales

Train.py performs training using SVM

Track.py and match.py are modules responsible for perfoming Kalman filter tracking and then selecting the most likely candidates for the bounding boxes 


# Module 2. 
The lane detection consists of the following files. 

Calibrate_cameras.py and perspective_transform.py perform camera calibration and perspective mapping

Combined_thresh.py performs the next step - edge filtering and to get a better understanding of the lane markers we also augment the previous filtered result with an HLS filter.

Lanefit.py performs the line detection

Finally for visualization purposes two files are provided one for image and one for video these are implemented in generate_examples.py and line_fit_video.py These algorithms were then tested on two videos challenge_video and project_video. The result can be viewed in challenge_video_result and project_video_result.
