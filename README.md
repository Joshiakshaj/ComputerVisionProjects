Image Flipping using Python
sample.pmg is an image used

first
import cv2
from matplotlib import pyplot as plt

to load/read and rename image and thereafter display image

img = cv2.imread('sample.png')

name = 'OpenCV Python Image'

plt.title(name)

plt.imshow(img)

To Flip Horizontally, rename and display

horizontal_flip = cv2.flip(img,1)

name = 'OpenCV Python FLipped Horizontally'

plt.title(name)

plt.imshow(horizontal_flip)

To Flip Verically, rename and display

vertical_flip = cv2.flip(img,0)

name = 'OpenCV Python flipped vertically'

plt.title(name)

plt.imshow(vertical_flip)

To Flip Horizontally AND Vertically, rename and display

vertical_horizontal = cv2.flip(img, -1)

name = 'OpenCV Python flipped vertically and horizontally'

plt.title(name)

plt.imshow(vertical_horizontal)

TO CONVERT IMAGE TO HIGH CONTRAST

directly read image
high_contrast = cv2.imread('redearedslider.jpg')

plt.imshow(high_contrast)

TO CONVERT TO LOWER CONTRAST

low_contrast = cv2.bitwise_not(high_contrast)

plt.imshow(low_contrast)

cv2.imwrite('lowered_contrast.jpg',low_contrast)

ARRAY
from PIL import Image

from numpy import array

im_1 = Image.open('redearedslider.jpg')

arr_1 = array(im_1)
arr_1

im_2 = Image.open('lowered_contrast.jpg')

arr_2 = array(im_2)
arr_2

------------------------------------------------------------------------------------------------


