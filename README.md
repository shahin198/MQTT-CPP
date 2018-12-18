# MQTT-CPP
https://www.yatta.de/profiles/hub/rg7l


CMake v3.5 or newer
GCC v4.8 or newer or Clang v3.9 or newer
GNU Make

# On Debian based systems this would mean that the following packages have to be installed:
```
apt-get install build-essential gcc make cmake cmake-gui cmake-curses-gui
```
# Building the documentation requires doxygen and optionally graphviz to be installed:
```
sudo apt-get install doxygen graphviz

sudo apt-get install libssl-dev
```
# First, build and install the Paho C library:
```
$ git clone https://github.com/eclipse/paho.mqtt.c.git
$ cd paho.mqtt.c
$ git checkout v1.2.1
$ cmake -Bbuild -H. -DPAHO_WITH_SSL=ON
$ sudo cmake --build build/ --target install
$ sudo ldconfig
```
# for CPP:
```
$ git clone https://github.com/eclipse/paho.mqtt.cpp
$ cd paho.mqtt.cpp
$ mkdir build
$ cd build
$ cmake -DPAHO_BUILD_DOCUMENTATION=TRUE -DPAHO_BUILD_SAMPLES=TRUE -DPAHO_MQTT_C_PATH=../../paho.mqtt.c ..
$ make
```
