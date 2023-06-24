2 #Second project encompasses grayscaling and RGB channeling an image.
baby.jpg and raga.jpg are images used.
first,
import numpy as np
matplotlib.pyplot as plt

##To Read Image##
import cv2
declare variable 'image' with imread function as
image = cv2.imread("baby.jpg")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

title as 'original' and display
plt.title("Original")
plt.imshow(image_rgb)

##grayscaling the image##
gray_image= cv2.imread("baby.jpg", cv2.COLOR_BGR2GRAY)

###save with imwrite func###

cv2.imwrite("baby_gray.jpg", gray_image)

plt.title("Gray-Scale")
plt.imshow(gray_image)


###load and display the image###

img= cv2.imread("baby_gray.jpg")

###displaying the image###
title as Saved Image and display

plt.title("Saved Image")
plt.imshow(img)

CONSIDER ABOVE PROGRAM AS TUTORIAL

'''Convert color image to gray scale'''

import cv2
src = 'raga.jpg'
input_image = cv2.imread(src)
cv2.imshow('Original Image', input_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
if input_image is None:
    print ('Could not open image', inout_image)
    exit(0)
    

####grayscale version of the image###
gray = cv2.cvtColor(input_image, cv2.COLOR_BGR2GRAY)

####display the grayscale version###

cv2.imshow('Grayscale Image', gray)

cv2.waitKey(0)
cv2.destroyAllWindows()

'''Separating BGR and Combining BGR channels'''

import cv2
import numpy as np
src = 'raga.jpg'
input_image = cv2.imread(src)
if input_image is None:
    print ('Could not load image', input_image)
    exit(0)
    
###splitting image in RGB channels###
blue, green, red = cv2.split(input_image)
cv2.imshow('Blue - Gray scale', blue)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('Green - Gray scale', green)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('Red - Gray scale', red)
cv2.waitKey(0)
cv2.destroyAllWindows()

###create dummy 3d array###
blue_channel = np.zeros(input_image.shape, input_image.dtype)
green_channel = np.zeros(input_image.shape, input_image.dtype)
red_channel = np.zeros(input_image.shape, input_image.dtype)
cv2.mixChannels([blue, green, red], [blue_channel], [0,0])
cv2.mixChannels([blue, green, red], [green_channel], [1,1])
cv2.mixChannels([blue, green, red], [red_channel], [2,2])
cv2.imshow('Blue Channel', blue_channel)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('Green Channel', green_channel)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('Red Channel', red_channel)
cv2.waitKey(0)
cv2.destroyAllWindows()

####Blurring Image###

###Blurring image###
import cv2
img = cv2.imread('raga.jpg')
cv2.imshow('original image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
blur_image = cv2.medianBlur(img,13)
cv2.imshow('Blurred image', blur_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
