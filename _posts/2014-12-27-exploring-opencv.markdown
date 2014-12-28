---
layout: post
title:  "Exploring OpenCV Part 3"
date:   2014-12-27 15:38:28
categories: opencv
---

# Reading OpenCV Essentials, Chapter 3:

Reference the <a href="https://www.packtpub.com/code_download/17932" target="_blank">example code</a> from OpenCV Essentials.

#### Create Histogram
Had enormous trouble today with importing the OpenCV library. While previous scripts had been working without flaw, when I opened the script I recieved a symantic "syntax" error. Reinstalling with brew did not work, unlink/link also failed. Ultimately I had to install MacPorts, install gmp46 via ports, install ffmpeg directly after clearing the system cache, and then install openCv 2.4.10 via ports. Once the library was made this script (<a href="https://gist.github.com/thnkr/802454fb828b3aeb0184" target="_blank">https://gist.github.com/thnkr/802454fb828b3aeb0184</a>) did not work due to some error with cvtColor conversion to black and white. My guess is an issue with QT which is mentioned in the book or some other windows depenedent issue which I cannot test. We get the following error:

<p>
OpenCV Error: Assertion failed (scn == 3 || scn == 4) in cvtColor, file /opt/local/var/macports/build/_opt_mports_dports_graphics_opencv/opencv/work/opencv-2.4.10/modules/imgproc/src/color.cpp, line 3739
libc++abi.dylib: terminating with uncaught exception of type cv::Exception: /opt/local/var/macports/build/_opt_mports_dports_graphics_opencv/opencv/work/opencv-2.4.10/modules/imgproc/src/color.cpp:3739: error: (-215) scn == 3 || scn == 4 in function cvtColor
</p>

Testing on other scripts with the libraries imported works. 

#### Create Histogram Graph
Interestingly the example after the one above worked: <a href="https://gist.github.com/thnkr/94198b85741d4c093444" target="_blank">https://gist.github.com/thnkr/94198b85741d4c093444</a>

#### Brightness & Contrast
Note, the Scheme included a command line argument. <a href="https://gist.github.com/thnkr/caea9a4667e80e80577e" target="_blank">https://gist.github.com/thnkr/caea9a4667e80e80577e</a>

#### Histograph Matching
Also works no problem with source code examples. <a href="https://gist.github.com/thnkr/72e562803ac88203b55a" target="_blank">https://gist.github.com/thnkr/72e562803ac88203b55a</a>

#### Import and convert using multiple color channels
<a href="https://gist.github.com/thnkr/d1ce78ceba2171ca90f8">https://gist.github.com/thnkr/d1ce78ceba2171ca90f8</a>

#### (Filtering Retina) Examing Motion
This first introduced the concept of magnocellular and parvocellular cells which deal with what and how. Magno particularlly deals with how or why (like how move limbs in relation to objects) and parvo deals with "what" the object actually in. This case focuses on magnocellular (we will need some level of motion analyses). It seeks to extract motion from a picture.

<a href="https://gist.github.com/thnkr/a688dcd5d778089b3b9b" target="_blank">https://gist.github.com/thnkr/a688dcd5d778089b3b9b</a>

# REFERENCE FROM CHAPTER 7

#### Direct from video Camera convert to greyscale:
<a href="https://gist.github.com/thnkr/be301c70b954cdce633f">https://gist.github.com/thnkr/be301c70b954cdce633f</a>

#### Motion Tracking
A good candidate for the conference prototype, tracks motion. <a href="https://gist.github.com/thnkr/6eb0dde7dbad447cade9" target="_blank">https://gist.github.com/thnkr/6eb0dde7dbad447cade9</a>

# REFERENCE FROM CHAPTER 8

#### Detect Edges
<a href="https://gist.github.com/thnkr/e7b178686abafb01a719">https://gist.github.com/thnkr/e7b178686abafb01a719</a>

#### Detect Specific Colors
<a href="https://gist.github.com/thnkr/dc532a71dfca91d10ff1">https://gist.github.com/thnkr/dc532a71dfca91d10ff1</a>

# Custom Trainer
Successfully trained HAAR Cascade on negative and positive images for two stages. However, the sample video run-through with <a href="https://gist.github.com/thnkr/5a0016dc61e0e9391b5a" target="_blank">this script</a> did not detect the target. Only ran through 2 stages, going to move the computation burden of to a cloud machine (CXS) for the time being and bump things to 20 stages.

<a href="https://bitbucket.org/thnkr/opencv_face_training_patrick">https://bitbucket.org/thnkr/opencv_face_training_patrick</a>

