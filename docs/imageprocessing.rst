============
Image Processing
============
The image proccessing window handle preprocessing of images before they are used in a print. 
Currently this image processing is only in use for encoding images for Video Pattern projection mode.

Image Encoding
-----------------
.. image:: images/image-process-algorithm.png

The image encoding process takes input 1-bit binary images and converts them to 24-bit images.
Each binary image consists of only 1 bit layer while a 24-bit image contains 24 bit layers. 
The encoded image is created by stacking 24 1-bit images into the RGB channels of the 24-bit image.

Controls
-----------

.. image:: images/image-processing.PNG

**Input Images:**
Select the binary input image to be encoded.

**Select Target Directory:**
Select where the encoded images will be stored.

**Output Images:**
The ouput image window shows the encoded image files that are generated and their location.

**Display Window:**
The display window show the encoded images that are generated. The user should validate that these images
look correct.

**Progress Bar:**
Provides the user with visual feedback on the active encoding.

**Select Encoding Type:**
Starts the encoding process. Select between converting 1-bit images to 24-bit images for 1-bit/binary prints or converting 8-bit images to 24-bit images for 8-bit/grayscale prints

**Terminal Window:**
Provides the user with some live feedback of the encoding process. Also serves as a valuable debug tool.