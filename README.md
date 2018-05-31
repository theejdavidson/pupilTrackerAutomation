# pupilTrackerAutomation
**Pupil tracking test:**
-run methods in order, be sure to have pupeTrackr.mp4 in directory, or change file name to given mp4 you wish to pull frames from.  Run the method and stop at the given frame you want to analyze, then continue to run the rest of the methods.  May need to play with SLSQP parameters in optimize fit to optimize the fit properly.

**Dependencies:** Utilizing scipy.optimize package: Nelder-Mead Simplex & SLSQP Algorithm. Matplotlib, NumPy, Pillow, PyLab, & OpenCV2.

Hugh circle transform (utilizing ellipse transform method):
still needs fixing to analyze custom image, we are unsure why method is returning an image that cannot be analyzed.  Possible that io.imRead does not perform the same function as the data.directoryFile() used in example code.

