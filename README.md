# EMG Fitness Device
HKUST Final Year Project

![EMG Lift](/assets/img/EMG_Lift.png)


# <a href="https://youtu.be/pZxpOF_Pch0">YouTube Demo</a>

# Description
This project aims to build a portable and affordable personal muscle monitoring system, consisting of a wearable device containing EMG(Electromyography) sensors to track muscle signals and a mobile application (Android) to assist users in preventing muscle injuries during workouts or in daily life. The wearable device transmits real-time EMG data to the mobile application for signal analysis. When a drop in the median frequency in EMG is detected, the application will prompt the user to cease further activity to prevent injury. A TensorFlow model was included to classify the actions being taken by the user.

To use this this product, the user can simply strap the sensor onto the group of muscle they would like to monitor, connect to it with the Andriod application via BLE(Bluetooth Low Energy), and start working out.

The technology used for this project are: Java, Android, BLE, C++, Arduino, TensorFlow.

IDE Used: Android Studios, Arduino IDE

# Electrode Circuit And Arduino Component
The electrode circuit is responsible for collecting and amplifying the surface EMG signal; the arduino component is responsible for picking up the signal from the electrode circuit, package it, and send it to the mobile application for further analysis via BLE.

These two components are enclosed into a compact 3D-printed enclosure. It is powered by attaching it to a power source via USB. Attaching the device to a power bank makes it portable.

# <a href="https://github.com/whiteunicorn3404/JQ03a-21_EMG_FYP">Arduino Code</a><br>
![Enclosure](/assets/img/FYP_0.png)
![EMG_Device](/assets/img/FYP_1.png)

# Android Application
The Android application connects to the Arduino component via BLE and receives real-time data from it. The application has rolling window that analyze the recent muscle activities. When a drop in the median frequency of the EMG singals are detected, it may indicate muscle fatigue from the user. The application will then warn the user about the fatigue via buzzing and a non-blocking prompt.

The application also contains a Tensorflow model that classify the actions of the user and a recording function that helps user collect information on their muscle performance.<br>
![EMG_App](/assets/img/FYP_2.png)
