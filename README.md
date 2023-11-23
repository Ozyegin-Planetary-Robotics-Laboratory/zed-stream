# ZED-Gstreamer

# INTRODUCTION

- This bash script code aims to encode the data it receives from the ZED camera and send it to a websocket, then decode the data they receive from there and display it again.

- "h264" was used to encode and decode the data. ( https://gstreamer.freedesktop.org/documentation/x264/index.html )

# HOW YOU CAN USE THIS ?

1- First of all, you should install gstreamer in your machine. (https://gstreamer.freedesktop.org/documentation/installing/index.html)

2- You should install ZED SDK in your machine. ( https://www.stereolabs.com/docs/gstreamer/#installation ) 

( !!! This SDK has a large size so make sure you have enough space before downloading !!! )

3- Make sure you connect zed camera.

4- Then, first run the transmitter.sh at terminal.

5- Finally, run the receiver.sh at second terminal.

You will see a screen which is shows zed camera.

