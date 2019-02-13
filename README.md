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
 

 