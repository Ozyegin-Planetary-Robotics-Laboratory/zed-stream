#sudo docker run -it --gpus all --privileged stereolabs/zed:4.0-tools-devel-jetson-jp4.6.1
  
FROM stereolabs/zed:4.0-tools-devel-jetson-jp4.6.1

RUN apt-get update

RUN apt-get install -y wget git build-essential cmake libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libgstreamer-plugins-bad1.0-dev gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-tools gstreamer1.0-x gstreamer1.0-alsa gstreamer1.0-gl gstreamer1.0-gtk3 gstreamer1.0-qt5 gstreamer1.0-pulseaudio libgstreamer1.0-0      gstreamer1.0-libav      libgstrtspserver-1.0-0      gstreamer1.0-tools      gstreamer1.0-x      gstreamer1.0-alsa      gstreamer1.0-gl      gstreamer1.0-gtk3      gstreamer1.0-qt5      gstreamer1.0-pulseaudio      libgstreamer1.0-dev      libgstrtspserver-1.0-dev      libgstreamer-plugins-base1.0-0      libgstreamer-plugins-base1.0-dev      libgstreamer-plugins-good1.0-0      libgstreamer-plugins-good1.0-dev      libgstreamer-plugins-bad1.0-0      libgstreamer-plugins-bad1.0-dev

RUN git clone https://github.com/stereolabs/zed-gstreamer.git

WORKDIR zed-gstreamer

RUN mkdir build

RUN cmake -DCMAKE_BUILD_TYPE=Release .

RUN make

RUN make install

WORKDIR /usr/local/zed

RUN git clone https://github.com/Ozyegin-Planetary-Robotics-Laboratory/zed-stream.git

WORKDIR zed-stream

CMD bash zed_transmit 8080 10.200.92.21