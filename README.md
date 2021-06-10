# RaspiCam

First enable the camera:

```
sudo raspi-config
```

For test pruposes execute:

```
raspistill -t 0
```

The command above will open the camera preview window. If you want to take a photo use the following commands:

```
raspistill -o namefile.jpg
raspistill -vf -hf -o namefile.jpg
```

The seccond command options above -vf and -hf are use for vertical and horizontal flip correction in case the camera has been positioned upside-down.

To take video use:

```
raspivid -o namefile.h264 -t 1000
```

The last option specifies the time in ms

# UDP Video Streaming

Installing prerequisites for OpenCV:

```
sudo apt-get install libhdf5-dev libhdf5-serial-dev libatlas-base-dev libjasper-dev libqtgui4 libqt4-test
```

Now proceed to install OpenCV, it's recomenended to specify a version for control pruposes and avoid errors:
``
pip3 install opencv-contrib-python==4.1.0.25
``

