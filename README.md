---
platform: Linux
device: Pronto Industrial RTU
language: NA
---

Configure a simple MODBUS database data mapping and transmission
===
---

# Table of Contents

-   [Introduction](#Introduction)
-   [Step 1: Prerequisites](#Prerequisites)
-   [Step 2: Prepare your Device](#PrepareDevice)
-   [Step 3: Build and Run the Sample](#Build)
-   [Next Steps](#NextSteps)

<a name="Introduction"></a>
# Introduction

**About this document**

This document describes how setup a transmission agent that transmit data to Azure IoT Hub. This multi-step process includes:

-   Configuring Azure IoT Hub
-   Registering your IoT device
-   Proton Configuration

<a name="Prerequisites"></a>
# Step 1: Prerequisites

You should have the following items ready before beginning the process:

-  A computer this Chrome web browser
-  [Setup your IoT hub](https://github.com/Azure/azure-iot-device-ecosystem/blob/master/setup_iothub.md)
-  [Provision your device and get its credentials](https://github.com/Azure/azure-iot-device-ecosystem/blob/master/manage_iot_hub.md)
-  Proton Unit.

<a name="PrepareDevice"></a>
# Step 2: Prepare your Device
Configure device and gateway IPs

# Step 3: Run Sampple

<a name="Create"></a>
## 3.1 Create a transmission agent

![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img1.png)
****
![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img2.png = 100x20)

<a name="Credentail"></a>
## 3.2 Set device credentials and transmission scheme

![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img3.png = 100x20)
****
![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img4.png = 100x20)

<a name="Mapping"></a>
## 3.3 Map MODBUS database variables to IoT transmission frame

![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img5.png = 100x20)
****
![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img6.png = 100x20)


<a name="Status"></a>
## 3.3 Verify tranmission status

![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img7.png = 100x20)


<a name="Run"></a>
# 4 Validate
   In this section you will run the Azure IoT client SDK samples to validate communication between your device and Azure IoT Hub. You will send messages to the Azure IoT Hub service and validate that IoT Hub has successfully receive the data. You will also monitor any messages sent from the Azure IoT Hub to client.








### 4.1 Send Device Events to IoT Hub:



### 4.2 Receive messages from IoT Hub



<a name="NextSteps"></a>
# Next Steps
 

# Azure IoT C SDK Compilation on VAR-SOM-MX7 : NXP/Freescale iMX7
## WiFi Setup
``
 nano /etc/wpa_supplicant.conf
``
```ruby
 network={
         ssid="wifi_name"
         psk="wifi_key"
}
```
 
```ruby
ip link set wlan0 down
ip link set wlan0 up
wpa_supplicant -iwlan0 -c /etc/wpa_supplicant/wpa_supplicant.conf
```
 
In a different terminal
``
dhclient wlan0
``
Once internet acces is verified
## Azure IoT dev apt-get
```ruby
ap-get update
apt-get install -y git 
apt-get install -y cmake
apt-get install -y build-essential
apt-get install -y curl
apt-get install -y libcurl4-openssl-dev
apt-get install -y libssl-dev
apt-get install -y uuid-dev
```
 
### Install rsync
```
ap-get update
apt-get install rsync
```
 
### sync usr and lib into development machine
``
rsync -rl --safe-links pi@<your Pi identifier>:/{lib,usr} /home/sergio/usr_lib.DEV/
``
 
### openssl path setup
in home/.profile add
``
export OPENSSL_ROOT_DIR=/home/sergio/usr_lib.DEV/usr/lib/arm-linux-gnueabihf
``
 
then
``
. ~/.profile
``
 
### Cmake compilation
```ruby
root@var-som-mx7:/home/user/home/sergio/azure-iot-sdk-c# mkdir cmake
root@var-som-mx7:/home/user/home/sergio/azure-iot-sdk-c# cd cmake/
root@var-som-mx7:/home/user/home/sergio/azure-iot-sdk-c/cmake# ls

root@var-som-mx7:/home/user/home/sergio/azure-iot-sdk-c/cmake# cmake ..
-- The C compiler identification is GNU 6.3.0
-- The CXX compiler identification is GNU 6.3.0
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- IoT Client SDK Version = 1.2.13
-- Looking for include file stdint.h
-- Looking for include file stdint.h - found
-- Looking for include file stdbool.h
-- Looking for include file stdbool.h - found
-- target architecture: ARM
-- Performing Test CXX_FLAG_CXX11
-- Performing Test CXX_FLAG_CXX11 - Success
-- Found OpenSSL: /usr/lib/arm-linux-gnueabihf/libssl.so;/usr/lib/arm-linux-gnueabihf/libcrypto.so (found version "1.1.0j")
-- Could NOT find PkgConfig (missing:  PKG_CONFIG_EXECUTABLE)
-- Found CURL: /usr/lib/arm-linux-gnueabihf/libcurl.so (found version "7.52.1")
-- Found CURL: /usr/lib/arm-linux-gnueabihf/libcurl.so
-- target architecture: ARM
-- target architecture: ARM
-- target architecture: ARM
-- target architecture: ARM
-- iothub architecture: ARM
-- Configuring done
-- Generating done
-- Build files have been written to: /home/user/home/sergio/azure-iot-sdk-c/cmake
```
### Compilation commands
``
sergio@ubuntu:~/azure-iot-sdk-c/build_all/linux$ ./build.sh --toolchain-file toolchain-prtn.cmake  --no-amqp --no-http -cl -DMBED_BUILD_TIMESTAMP  -cl --sysroot=/home/sergio/usr_lib.DEV
``