# **Finding Lane Lines on the Road** 

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I call to gaussian_blur function, after that i call to canny algorithm and after i made a mask using the vertices that i calculated according the image shape with region_of_interest function. After that i called the hough_lines function with the parameters i calculated (one for the white line video and other to the yellow line video) and at the end i called weighted_img function for creating a new video with the extrapolated line layered on the original video.

In order to draw a single line on the left and right lanes, I implemented a new function called extended_lines that take the max and min y points and connect them to average the line.


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the line is not stright, if there were any curve it seems that the pipeline will not be correct.

Another shortcoming could be at night, the image won't be the same as at day and it would be hard to identify the lines.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use other method (if there is any)

Another potential improvement could be to use always videos from ir cameras.
