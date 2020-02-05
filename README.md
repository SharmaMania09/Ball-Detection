# Ball-Detection

First, all the important packages are imported such as numpy, argparse, cv2 etc.

After that, as we know that the tennis ball is green in color and comes under a color range.
So, define greenLower and greenUpper containing the RGB color.

After that resize the frame and convert it into HSV i.e Hue, Saturation and value. We are converting RGB into HSV because R, G, B in RGB are all co-related to the color luminance( what we loosely call intensity),i.e., We cannot separate color information from luminance. HSV or Hue Saturation Value is used to separate image luminance from color information. This makes it easier when we are working on or need luminance of the image/frame.

Then, find contours in the mask and initialize the current (x, y) center of the ball, to join all the continous points having same color or intensity.
If we are able to find contour then we will proceed.
Find the largest contour in the mask and then use it to compute the minimum enclosing circle and centroid.
After that on finding the center, we will draw the circle to show the detection.
