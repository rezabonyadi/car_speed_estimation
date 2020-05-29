# Car speed estimation

* Use environment.yml to set up your environment
* A couple of points about the problem
    * The velocity cannot be estimated if there is no difference between 
    two consecutive frames
    * The velocity is relative meaning that if we look at a car 
    in front and that car goes a little bit faster than us then what 
    we would estimate is the difference between our speed and that 
    car speed 
    * Given the above, we need to find an area in the camera in which 
    the changes between frames are related to the car movement only, 
    i.e., all objects are still if the car was not moving
 * Some points about the model
    * If we use the first drivitive of frames then it already has speed
    information in it. This enables using a 2D conv filter directly
    on the frames (which are now diff of the original frames) to find
    the relationship between the speed of changes in the image and 
    the speed of the car
    * If we use raw images then a 3D conv accross our frames would be 
    needed to somehow mimic the behaviour of first drivitive accross 
    frames. At the end of the day, the speed of movement is related to 
    the changes between frames rather than each frame in isolation.
 

 
