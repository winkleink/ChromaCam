# ChromaCam

Using Raspberry Pi and CSI camera module to do green screen.
With this program you can do greeen screen images.  Taking out the background and replacing them with a different background.

Using the following libraries

import sys
import pygame
from pygame import locals
from picamera import PiCamera
from time import sleep, time
import subprocess 
import os
import shlex
import glob
import tweepy 


Copy code to folder /home/pi/chromaCam
Create subfolder

sourcebg   - storage for possible background images
background - where background images are stored at the required resolution

Also, needed an overlap_640.png (assuming resolution is 640x480) that is added to the image when it is tweeted.  This file is in the /home/pi/chromaCam folder

With these 2 sub folders you can start with images at any resolution and store them in sourcegb.  When the code starts it copies the images and resizes them putting them in the background folder.

Use keys left/right to change the background and enter to take a picture and tweet it.
Alternative if you have a gamepad attached can use the gamepad 
I use a small Bluetooth gamepad as it's hardly visible in the persons hand and means the person can control the background the final picture themself.







