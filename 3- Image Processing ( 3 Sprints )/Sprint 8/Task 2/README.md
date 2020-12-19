# 1- What ’re the methods that you used ?

   - OpenCV
        - imread()
        - cvtColor()
        - resize()
        - imwrite()
        - getRotationMatrix2D()
        - warpAffine() 
        - Canny()
        - GaussianBlur()
        - medianBlur()
        - bilateralFilter()
        
   - matplotlib
        - pyplot.imshow()   
        - pyplot.set_title()
        - pyplot.subplots()      

   - np.float32()
   
# 2- Explain each method ..

   1. **Image Resizing using OpenCV**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - print the original image dimension.
        - Resize the image using openCV resize method by assigning:
          - **src**
            - source/input image
          - **dsize**
            - desired size for the output image
            - The order (width, height) unlike as expected (height, width). 
          - **fx**
            - scale factor along the horizontal axis    
          - **fy**
            - scale factor along the vertical axis
          - **interpolation**
            - INTER_AREA:
              - This is used when we need need to shrink an image. 
            - INTER_CUBIC:
              - This is slow but more efficient.  
              - a bicubic interpolation over 4×4 pixel neighborhood 
            - NTER_LINEAR: 
              - This is primarily used when zooming is required.
              - This is the default interpolation technique in OpenCV. 
            - INTER_NEARSET:
              - nearest neighbor
            - INTER_LANCZOS4:
              - a Lanczos interpolation over 8×8 pixel neighborhood   
        - Then plot the resulted images  
        
   2. **Scaling an Image** 
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Resize the image by half of it's width and height
        - Then print the original and scaled images.
        
   3. **Rotating an image**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Calculate the height and width of the image to calc the center of it.
        - Then using openCV getRotationMatrix2D to rotate the image around it's center by 45 degree
        - Then apply the affine transformation using openCV warpAffine method to perform the rotation.  
        
   4. **Translating an Image**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Create the translate matrix using numpy 
          - we create 2x3 matrix 
            - [1, 0, 100]
            - [0, 1, 50] 
        - Then apply the affine transformation using openCV warpAffine method to perform the translation.   
        
   5. **Edge detection in an Image**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Extract edges from our image using Canny edge detection method from openCV by assiging:  
          - First argument is our input image.
          - Second and third arguments are our minVal and maxVal respectively.
          - Third argument is aperture_size.
            - It is the size of Sobel kernel used for find image gradients --> **By default it is 3**.
          - Last argument is L2gradient which specifies the equation for finding gradient magnitude.
            - If it is True, it uses the equation mentioned above which is more accurate.
              - Edge_Gradient (G) = sqrt(G_x^2 + G_y^2)
            - otherwise it uses this function:
              - Edge_Gradient (G) = |G_x| + |G_y|.
            - By default, it is False.
        
   - **Image blurring using OpenCV**
        - **Image Blurring**
            - refers to making the image less clear or distinct.
            - It is done with the help of various low pass filter kernels.
        - **Advantages of blurring**:
            - It helps in Noise removal.
            - As noise is considered as high pass signal so by the application of low pass filter kernel we restrict noise.
            - It helps in smoothing the image.
            - Low intensity edges are removed.
            - It helps in hiding the details when necessary.
            - For e.g. in many cases police deliberately want to hide the face of the victim, in such cases blurring is required.
        - **Important types of blurring**:
            - **Gaussian Blurring**:
                - is the result of blurring an image by a Gaussian function.
                - It is a widely used effect in graphics software, typically to reduce image noise and reduce detail.
                - It is also used as a preprocessing stage before applying our machine learning or deep learning models.
            - **Median Blur**:
                - The Median Filter is a non-linear digital filtering technique, often used to remove noise from an image or signal.
                - Median filtering is very widely used in digital image processing because, under certain conditions, it preserves edges while removing noise. 
                - It is one of the best algorithms to remove Salt and pepper noise.
            - **Bilateral Blur**:
                - A bilateral filter is a non-linear, edge-preserving, and noise-reducing smoothing filter for images.
                - It replaces the intensity of each pixel with a weighted average of intensity values from nearby pixels.
                - This weight can be based on a Gaussian distribution.
                - Thus, sharp edges are preserved while discarding the weak ones.    
                
   6. **Image blurring using OpenCV**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Apply Gaussian Blur method to our image by assiging:
          - our source image
          - Gaussian kernel size
          - SigmaX = 0
        - Apply Median Blur method to our image by assigning:
          - source image 
          - size of the kernel
        - Apply bilateralFilter method to our image by assiging:
          - Source image
          - The diameter of the pixel neighborhood
          - sigmaColor
            - representing the filter sigma in the color space.
          - sigmaSpace
            - representing the filter sigma in the coordinate space.
        - Then show the resulted images       
                                                                
# 3- What’s new for you ?

  - Reviewing on edge detection and image blurring

# 4- Resources ? 

   - https://www.tutorialkart.com/opencv/python/opencv-python-resize-image/
   - https://www.geeksforgeeks.org/implement-canny-edge-detector-in-python-using-opencv/
   - https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_imgproc/py_canny/py_canny.html
   - https://towardsdatascience.com/canny-edge-detection-step-by-step-in-python-computer-vision-b49c3a2d8123
   - https://docs.opencv.org/master/d4/d86/group__imgproc__filter.html#gaabe8c836e97159a9193fb0b11ac52cf1
   - https://www.tutorialspoint.com/opencv/opencv_median_blur.htm#:~:text=The%20Median%20blur%20operation%20is,edges%20while%20removing%20the%20noise.
   - https://docs.opencv.org/master/d4/d86/group__imgproc__filter.html#ga564869aa33e58769b4469101aac458f9
   - https://docs.opencv.org/master/d4/d86/group__imgproc__filter.html#ga9d7064d478c95d60003cf839430737ed
   - https://www.tutorialspoint.com/opencv/opencv_bilateral_filter.htm
   - https://www.programmersought.com/article/52494917727/
   - https://stackabuse.com/affine-image-transformations-in-python-with-numpy-pillow-and-opencv/
   - https://www.geeksforgeeks.org/what-is-image-blurring/
   - https://docs.opencv.org/master/d4/d13/tutorial_py_filtering.html
   - https://docs.opencv.org/master/dd/d1a/group__imgproc__feature.html#ga04723e007ed888ddf11d9ba04e2232de
