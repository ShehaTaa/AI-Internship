# 1- What ’re the methods that you used ?

   - OpenCV cv2
        - imread()
        - imshow()
        - waitKey()
        - destroyAllWindows() 
        - cvtColor()
        - resize() 
        - getRotationMatrix2D()
        - warpAffine()
        - rectangle()
        - putText() 
        - imwrite()
        - imwrite()
        - subtract()
        - bitwise_and()
        - bitwise_or()
        - bitwise_not()
        - bitwise_xor()
            
   - matplotlib
        - pyplot.imshow()   
        - pyplot.set_title()
        - pyplot.subplots()
            
   - format
   
   - List   
       
# 2- Explain each method ..

   1. **Reading an image**
        - Read image using openCV imread method 
        - Then print image height and width   

   2. **Extracting the RGB values of a pixel**
        - Read image using openCV imread method
        - Randomly chosen a pixel by passing in 100, 100 for height and width.
        - Then print the values of R, G, and B
        - Then print the pixel value itself 
        
   3. **Extracting the Region of Interest (ROI)**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method
        - Calculate the region of interest by slicing the pixels of the image.
        - Then print the ROI using matplotlib imshow method.
        
   4. **Resizing the Image**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Then using openCV resize method to make image size 800 x 800 
        - Then print the resized image using matplotlib imshow method.       
        
   5. **Rotating the Image**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Calculate the height and width of the image to calc the center of it.
        - then using openCV getRotationMatrix2D to rotate the image around it's center by -45 degree
        - then apply the affine transformation using openCV warpAffine method to perform the rotation.
        
   6. **Drawing a Rectangle**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Draw rectangle using openCV rectangle by assigning
          - The source
          - Top-left corner co-ordinates, 
          - Bottom-right corner co-ordinates,
          - Color (in BGR format)
          - Line width                           

   7. **Displaying text**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Draw a text using openCV putText by assigning
          - The source
          - Text to be displayed
          - Bottom-left corner co-ordinates
          - from where the text should start
          - Font
          - Font size
          - Color (BGR format)
          - Line width 
          
   8. **Reading an image in OpenCV**
        - Read image using openCV imread method
        - Convert image format from BGR to RGB format using cvtColor method.
        - Show image using openCV imshow method and using waitkey(0) to display the window infinitely until any keypress.
        - Then assign the **ESC key** to stop display and destry the window.
        - and also assign the **S key** to save the displayed window.
        
   9. **Addition of Image**
        - Read two images using openCV imread method
        - Convert images format from BGR to RGB format using cvtColor method. 
        - adding the two images using openCV addWeighted to apply particular weights on the final image 
        - Then Show the output image.   
        
   10. **Subtraction of Image**
        - Read two images using openCV imread method
        - Convert images format from BGR to RGB format using cvtColor method. 
        - Subtract the two images using openCV subtract 
        - Then Show the output image.                                                                                                               
      
   11. **Bitwise AND operation on Image**
         - Read two images using openCV imread method.
         - apply bitwise and operation on images using bitwise_and method (conjunction of input array elements)
         - Then show the resulted image. 
         
   12. **Bitwise OR operation on Image** 
         - Read two images using openCV imread method.
         - Apply bitwise and operation on images using bitwise_or method (disjunction of input array elements)
         - Then show the resulted image.  
        
   13. **Bitwise XOR operation on Image**
         - Read two images using openCV imread method.
         - Apply bitwise and operation on images using bitwise_and method (exclusive-OR operation on input array elements)   
         - Then show the resulted image.    
         
   14. **Bitwise NOT operation on Image**
         - Read two images using openCV imread method.
         - Apply bitwise and operation on images using bitwise_not method (inversion of input array elements)   
         - Then show the resulted image.                                                                                                                                   
         
# 3- What’s new for you ?

   - Arithmetic Operations on Images

# 4- Resources ? 

   - https://www.geeksforgeeks.org/python-opencv-cv2-imread-method/
   - https://www.geeksforgeeks.org/matplotlib-pyplot-imshow-in-python/
   - https://matplotlib.org/3.3.2/api/_as_gen/matplotlib.pyplot.imshow.html   
   - https://www.geeksforgeeks.org/python-opencv-cv2-cvtcolor-method/ 
   - https://www.programcreek.com/python/example/89459/cv2.getRotationMatrix2D
   - https://docs.opencv.org/master/da/d6e/tutorial_py_geometric_transformations.html
   - https://www.tutorialkart.com/opencv/python/opencv-python-rotate-image/
   - https://stackoverflow.com/questions/51143458/difference-in-output-with-waitkey0-and-waitkey1/51143586
   - https://www.geeksforgeeks.org/reading-image-opencv-using-python/?ref=lbp
   - https://graphicdesign.stackexchange.com/questions/110960/difference-between-cropping-scaling-resizing-changing-aspect-ration-of-an-im
   - https://www.programmersought.com/article/5817873631/
   - https://www.javatpoint.com/opencv-image-rotation
   - https://www.geeksforgeeks.org/python-opencv-affine-transformation/
   - https://docs.opencv.org/master/d2/de8/group__core__array.html#ga10ac1bfb180e2cfda1701d06c24fdbd6
   - https://docs.opencv.org/2.4/modules/core/doc/operations_on_arrays.html#bitwise-and
