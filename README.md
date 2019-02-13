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

This document describes how to connect UP-Squared running Android Nougat (v7.1) with Azure IoT SDK. This multi-step process includes:

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

<a name="Load"></a>
## 3.1 Create a transmission agent

![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img1.png)
****
![picture](https://bitbucket.org/sergiojx/proton-azure-iot/downloads/img2.png = 100x20)

<a name="BuildSamples"></a>
## 3.2 Build the samples

1.   Start a new instance of Android Studio and open Android project from here:

        azure-iot-sdk-java/device/iot-device-samples/android-sample/

2.   Go to **MainActivity.java**, replace the **[device connection string]** placeholder with connection string of the device you have created in [Provision your device and get its credentials](local://base_request.html/Azure/azure-iot-device-ecosystem/blob/master/manage_iot_hub.md) and save the file. An example of IoT Hub Connection String is as below:

        HostName=[YourIoTHubName];SharedAccessKeyName=[YourAccessKeyName];SharedAccessKey=[YourAccessKey]
  Also replace the device ID with AAEON-UP-SQUARED-ANDROID device ID

3.   Build your project by going to **Build** menu **> Make Project**.

<a name="Run"></a>
## 3.3 Run and Validate the Samples
   In this section you will run the Azure IoT client SDK samples to validate communication between your device and Azure IoT Hub. You will send messages to the Azure IoT Hub service and validate that IoT Hub has successfully receive the data. You will also monitor any messages sent from the Azure IoT Hub to client.

### 3.3.1 Run the Sample:

### Run on the Device

-   Select one of your project's files and click Run from the toolbar.

-   In the Choose Device window that appears, select the **Choose a running device** radio button, select AAEON-UP APL01 device, and click OK.

-   Android Studio will install the app on your connected device and starts it.


### 3.3.2 Send Device Events to IoT Hub:

-   See [Manage IoT Hub](local://base_request.html/Azure/azure-iot-device-ecosystem/blob/master/manage_iot_hub.md) to learn how to observe the messages IoT Hub receives from the application.
-   As soon as you run the app on your device, it will start sending messages to IoTHub.
-   Check the **Android Monitor** window in Android Studio. Verify that the confirmation messages show an OK. If not, then you may have incorrectly copied the device hub connection information.
-   use device explorer application in Azure Iot SDK to watch the sent messages

### 3.3.3 Receive messages from IoT Hub

-   See [Manage IoT Hub](local://base_request.html/Azure/azure-iot-device-ecosystem/blob/master/manage_iot_hub.md) to learn how to send cloud-to-device messages to the application.
-   Click the **Receive Messages** button from the sample App UI.
-   Check the **Android Monitor** window in Android Studio. You should be able to see the command received.
-   use device explorer application in Azure Iot SDK to watch the received messages

<a name="NextSteps"></a>
# Next Steps
 
You have now learned how to run a sample application that collects sensor data and sends it to your IoT hub. To explore how to store, analyze and visualize the data from this application in Azure using a variety of different services, please click on the following lessons:
 
-   [Manage cloud device messaging with iothub-explorer]
-   [Save IoT Hub messages to Azure data storage]
-   [Use Power BI to visualize real-time sensor data from Azure IoT Hub]
-   [Use Azure Web Apps to visualize real-time sensor data from Azure IoT Hub]
-   [Weather forecast using the sensor data from your IoT hub in Azure Machine Learning]
-   [Remote monitoring and notifications with Logic Apps]   
 
[Manage cloud device messaging with iothub-explorer]: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-explorer-cloud-device-messaging
[Save IoT Hub messages to Azure data storage]: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-store-data-in-azure-table-storage
[Use Power BI to visualize real-time sensor data from Azure IoT Hub]: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-live-data-visualization-in-power-bi
[Use Azure Web Apps to visualize real-time sensor data from Azure IoT Hub]: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-live-data-visualization-in-web-apps
[Weather forecast using the sensor data from your IoT hub in Azure Machine Learning]: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-weather-forecast-machine-learning
[Remote monitoring and notifications with Logic Apps]: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-monitoring-notifications-with-azure-logic-apps
[setup-devbox-linux]: https://github.com/Azure/azure-iot-device-ecosystem/blob/master/get_started/node-devbox-setup.md
[lnk-setup-iot-hub]: ../setup_iothub.md
[lnk-manage-iot-hub]: ../manage_iot_hub.md
 