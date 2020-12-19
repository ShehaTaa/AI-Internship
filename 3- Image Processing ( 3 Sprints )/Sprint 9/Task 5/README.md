# 1- What ’re the methods that you used ?

   - **OpenCV**
        - imread()
        - cvtColor
        - CascadeClassifier()
        - detectMultiScale()
        - rectangle()
      
   - **matplotlib**
        - pyplot.imshow()   
        - pyplot.set_title()
        - pyplot.subplots()  

# 2- Explain each method ..

   - **Virtual Environment**
        - A Virtual Environment is a python environment that is:-
          - an isolated working copy of Python, which allows you to work on a specific project without affecting other projects
          - So basically it is a tool that enables multiple side-by-side installations of Python, one for each project. 
          -  Is a tool that helps to keep dependencies required by different projects separate by creating isolated python virtual environments for them. 
          - There are no limits to the number of environments you can have.
          - It should be used whenever you work on any Python based project.
          - It is generally good to have one new virtual environment for every Python based project you work on.
          - **Installing virtualenv**
              1. pip install virtualenv
              2. Test your installation:
                 - virtualenv --version 
              3. Create a virtualenv using the following command:   
                 - virtualenv my_name   
              4. If you want to specify Python interpreter of your choice:-
                 - virtualenv -p /usr/bin/python3 virtualenv_name 
                 - virtualenv -p /usr/bin/python2.7 virtualenv_name   
              5. Activate the relevant virtual environment every time you work on the project using:
                 - source virtualenv_name/bin/activate
              6. Once the virtual environment is activated, the name of your virtual environment will appear on left side of terminal. 
              7. You can install dependencies related to the project in this virtual environment like:
                 - (virtualenv_name)$ pip install Django==1.9
              8. Once you are done with the work, you can deactivate the virtual environment by the following command:
                 - (virtualenv_name)$ deactivate        

        - **Using mkvirtualenv to create new Virtual Environment**
            1. There are multiple ways of creating new Virtual Environment as using mkvirtualenv command.
               - you need to have virtualenvwrapper installed using:
                 -  sudo pip3 install virtualenvwrapper
             2. Open bashrc by 
                - sudo gedit ~/.bashrc
             3. add the following  lines to it
                - export WORKON_HOME=$HOME/.virtualenvs
                - export PROJECT_HOME=$HOME/Devel
                - source /usr/local/bin/virtualenvwrapper.sh    
                
   - **Detect an object with OpenCV-Python**
        - **Object Detection**: 
            - Is a computer technology related to computer vision, image processing, and deep learning that deals with detecting instances of objects in images and videos. 
            - **Haar Cascades**:
                - Is a machine learning-based approach where a lot of positive and negative images are used to train the classifier.
                  - Positive images
                    - These images contain the images which we want our classifier to identify.
                  - Negative Images
                    - Images of everything else, which do not contain the object we want to detect.
                

# 3- What’s new for you ?

   - Virtual Environment 
   - virtualenvwrapper
   
# 4- Resources ? 

   - https://www.geeksforgeeks.org/creating-python-virtual-environment-windows-linux/?ref=lbp
   - https://www.geeksforgeeks.org/python-virtual-environment/?ref=lbp
   - https://www.geeksforgeeks.org/create-virtual-environment-using-venv-python/?ref=lbp
   - https://www.geeksforgeeks.org/using-mkvirtualenv-to-create-new-virtual-environment-python/?ref=lbp
   - https://www.geeksforgeeks.org/detect-an-object-with-opencv-python/?ref=lbp
   - https://docs.opencv.org/3.4/d1/de5/classcv_1_1CascadeClassifier.html#aaf8181cb63968136476ec4204ffca498
   - https://www.researchgate.net/publication/3940582_Rapid_Object_Detection_using_a_Boosted_Cascade_of_Simple_Features
   - https://stackoverflow.com/questions/20801015/recommended-values-for-opencv-detectmultiscale-parameters
