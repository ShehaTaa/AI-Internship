# 1- What ’re the methods that you used ?

   - OpenCV
        - VideoCapture()
        - isOpened()
        - read()
        - cvtColor()
        - waitKey()
        - release()
        - destroyAllWindows() 
        - imwrite()
        - CascadeClassifier()
        - detectMultiScale()
        - rectangle()
   
   - matplotlib
        - pyplot.imshow()   
        - pyplot.set_title()
        - pyplot.subplots()    
   
   - OS
        - path.exists()
        - makedirs() 

# 2- Explain each method ..

   1. **Play a video using OpenCV**
        - **VideoCapture syntax**: 
          - cv2.VideoCapture(0):
            - Means first camera or webcam.
          - cv2.VideoCapture(1):
            - Means second camera or webcam.
          - cv2.VideoCapture("file name.mp4"):
            - Means video file
          
        - Read video file using openCV VideoCapture method
        - Then check if the video is open or not
          - if not open, print error message
        - if it's open, then loop through it and read it frame by frame 
        - Then print the frame resulting.
    
   2. **Extract images from video** 
        - Read video file using openCV VideoCapture method
        - Create a directory to save all frames in it using Os library.
        - Then loop through it and read all frames 
        - convert frame format from BGR to RGB using openCV cvtColor method
        - Then store each frame in the directory
        
   3. **Face Detection using Python and OpenCV** 
        - Load the our cascade classifier using openCV CascadeClassifier 
        - Capture video from webcam using openCV VideoCapture(0) 
        - Read the frame using openCV videoCapture.read
        - Then detect faces using face_cascade.detectMultiScale by specifing:
          - The source image frame
          - scaleFactor 
            - Parameter specifying how much the image size is reduced at each image scale.
          - minNeighbors 
            - Parameter specifying how many neighbors each candidate rectangle should have to retain it.
        - Then draw rectangle around detedcted face using openCV rectangle method.
        - Convert image from BGR to RGB format to show it.                


# 3- What’s new for you ?

   - Video using OpenCV
   - Face detection from live video
   
# 4- Resources ? 

   - https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_gui/py_video_display/py_video_display.html
   - https://docs.opencv.org/3.4/d8/dfe/classcv_1_1VideoCapture.html
   - https://www.learnopencv.com/read-write-and-display-a-video-using-opencv-cpp-python/
   - https://www.geeksforgeeks.org/extract-images-from-video-in-python/?ref=lbp
   - https://docs.opencv.org/master/d4/da8/group__imgcodecs.html
   - https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html
   - https://docs.opencv.org/2.4/modules/objdetect/doc/cascade_classification.html?highlight=detectmultiscale
   - https://stackoverflow.com/questions/20801015/recommended-values-for-opencv-detectmultiscale-parameters
   - https://towardsdatascience.com/a-guide-to-face-detection-in-python-3eab0f6b9fc1
   
   
