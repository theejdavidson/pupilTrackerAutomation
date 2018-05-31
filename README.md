# pupilTrackerAutomation
## Pupil Tracking Test:

Run methods in order, be sure to have pupeTrackr.mp4 in directory, or change file name to given mp4 you wish to pull frames from.  Run the method and stop at the given frame you want to analyze, then continue to run the rest of the methods. May need to play with SLSQP parameters in optimize fit to optimize the fit properly.

## Dependencies: 

Utilizing scipy.optimize package: Nelder-Mead Simplex & SLSQP Algorithm. Matplotlib, NumPy, Pillow, PyLab, & OpenCV2.

## Hugh Circle Transform (utilizing ellipse transform method):

Still needs fixing to analyze a custom image. We are unsure as to why the method is returning an image that cannot be analyzed.  Possible that io.imRead does not perform the same function as the data.directoryFile() used in example code.

## Canny Edge Detection:

**cv.Canny():** First argument is input image. Second & Third argument represent minVal & maxVal respectively. Note that the third argument is aperture_size and it is utilized for finding image gradients. (Third argument defaults to a value of 3. We may implement edge detection before HCT is utilized on a pupil frame so that we can remove persistent false circle detection).

## Description of the parameters for the cv2.HoughCircles function (Note that these parameters will have to be manually adjusted per frame in order to achieve optimal pupil fit)

**img:** Input image (grayscale)

**cv2.HOUGH_GRADIENT:** Define the detection method

**dp** = 2: The inverse ratio of resolution

**min_dist** = 50 Minimum distance between detected centers

**param1** = 30: Upper threshold for the internal Canny edge detector

**param2** = 195: Threshold for center detection.

**minRadius** = 100: Minimum radio to be detected. If unknown, put zero as default.

**maxRadius** = 200: Maximum radius to be detected. If unknown, put zero as default
