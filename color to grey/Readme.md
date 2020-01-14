# Color to greyscale image conversion
	
	Name: ABHINAV SINGH 
	COURSE ID : CPSC-6820 
	Section number :003 
	
## Approach
In this project, the program takes a ppm format colored image as an input, and output a pgm grayscale image. <br />
There are methods like **lightness** and **average** to turn image into greyscale, where in lightness method by taking average of most and least outstanding RGB colors the greyscale image is formed, but the drawback is that it reduces contrast of the image. In average method, the average of contribution of all RGB colors is taken, where each color of RGB contributes 33%, and the result is greyscale image, but more inclination towards being black in color. It happens because each color is not weighted according to their respective wavelengths. 

The approach used in the program is **Luminosity method** which weighs the Red, green and blue according to their wavelengths. As eyes are more sensitive towards Green then Red and least towards Blue, which leads to formula as follows:

**Grey =  0.21 R + 0.72 G + 0.07 B**

Process followed:

* ppm format file is given as input using PIL.
* Input image is then converted into 3-D array, which has separate RGB channels.
* Luminosity method is applied on RGB channel. 
* pixel value of each channel is changed to **Grey** for respective RGB channels.<br />
 for example:<br />
 	[R, G, B] would become [**Grey**, **Grey**, **Grey**]<br />
 	This is for converting the colored ppm format image to greyscale ppm format image.
*  For pgm format image a 1-D array with single channel would be sufficient with minimum value of 0(Black) and maximum of 255(White).<br />
This 1-D array is used to store **Grey** value that is calculated by lumniosity method by using values at RGB channels.
*  After calculating the values to be entered in the output files as arrays, respective headers are created for ppm file(P6 magic number header) and pgm file(P5 magic number header) and added to the output file then arrays are inserted.
*  Magic numbers signifies that if the image is stored whether in ASCII or in Binary format.
*  P5 for pgm is in Binary.



	


## Dependencies
* [Python 3.0.x](https://www.python.org/download/releases/3.0/)
* [NumPy](https://numpy.org/)
* [Pillow](https://pillow.readthedocs.io/en/stable/)


## Technologies
* [Jupyter notebook](https://jupyter.org/)



Both Jupyter notebook file(.ipynb) and python file(.py) is provided.
