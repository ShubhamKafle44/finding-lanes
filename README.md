**Lane Detection with OpenCV**
This project demonstrates a lane detection system using OpenCV and NumPy. It processes both images and video streams to identify lane markings on the road. The algorithm leverages edge detection, region masking, and the Hough Transform to identify lines and mark the lanes.

**Features**
  Canny Edge Detection: Detects edges in the image using OpenCV's Canny method.
  Region of Interest: Focuses on a specific region of the image to improve accuracy.
  Hough Line Transform: Detects lines in the processed image, using probabilistic Hough line detection.
  Lane Averaging: Averages multiple detected lines to produce a smoother lane display.
  Alpha-Beta Smoothing: Combines the original image with lane markings using a weighted sum to overlay the detected lanes onto the frame.\
  
**Usage**

  Image Lane Detection
  The image test_image.jpg is loaded.
  The image undergoes Canny edge detection and region masking.
  Lane lines are detected and drawn on the image.
  The result is displayed, showing the detected lanes on the original image.
  
  Video Lane Detection
  A video test2.mp4 is loaded.
  Each frame is processed similarly to the image, with lanes being detected and marked.
  The video with overlaid lane markings is displayed frame by frame.


**Code Overview**
**Core Functions**
  make_coordinates(image, line_parameters): Converts line parameters (slope, intercept) into pixel coordinates for drawing.
  average_slope_intercept(image, lines): Averages the detected lines to create smooth lane lines.
  canny(image): Applies Canny edge detection on the image to highlight lane edges.
  display_lines(image, lines): Draws detected lane lines on an image.
  region_of_interest(image): Focuses on a specific polygonal region of the image, masking irrelevant parts.
  
**Dependencies**
OpenCV: Used for image and video processing (cv2).
NumPy: Used for mathematical operations and array manipulation.
Matplotlib: Used for displaying images.
