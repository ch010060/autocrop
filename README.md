# autocrop
Automatically crop and rotate scanned images using OpenCV.
Should work on Windows, Linux and Mac.

## Install requirements

- pip install cv2
- pip install numpy

## Usage: python autocropy.py (THRESHOLD) (MIN_CROP)

Place autocrop.py into a folder of scanned images. Those images should be roughly cropped already (see examples). 
Also: only one image per scan!

Run script as described above. THRESHOLD and MIN_CROP are optional. Results will be stored in /crop/.

- THRESHOLD: threshold value to find image borders, default is 220
- MIN_CROP: additional cropped pixels to avoid unclean borders of the result, default is 15 pixels

## Todo: executables for Windows + basic GUI
To make it usable for less nerdy people.
