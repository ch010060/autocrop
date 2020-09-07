# autocrop
Automatically crop and rotate scanned images using OpenCV.
Should work on Windows, Linux and Mac.

## New feature at this fork
**1. Support multiprocessing to improve performance**  
**2. Support DPI setting of the output image**  
**3. Support filename with Unicode characters**   
**4. Add some error handling for infinity loop problem**  

## Install requirements

```bash
pip install python-opencv
pip install numpy
pip install Pillow
```

## Usage

`python autocropy.py <THRESHOLD> <MIN_CROP>`

Place autocrop.py into a folder of scanned images. Those images should be roughly cropped already (see examples). 
Also: only one image per scan!

Run script as described above. THRESHOLD and MIN_CROP are optional. Results will be stored in /crop/.

- `<THRESHOLD>`: threshold value to find image borders, default is 220
- `<MIN_CROP>`: additional cropped pixels to avoid unclean borders of the result, default is 15 pixels

## Troubleshooting

### Problem:
`ValueError: too many values to unpack (expected 2)`
### Solution:
You likely use an outdated version of OpenCV. Make sure you have OpenCV 4.0 or higher installed. The version can be checked by executing the following code in your favorite python interpreter:

```python
>>> import cv2
>>> print("OpenCV version: ", cv2.__version__)
OpenCV version: 4.2.0
```

## Todo: executables for Windows + basic GUI
To make it usable for less nerdy people.
