# vex-smart-scan

Presenting Smart Scan, the intelligent Android app and REST API for Vex Robotics Competition scouting from team 4001A - Aetherium. 

This repository consists of three parts - the smart-scan backend, the smart-scan-server, and smart-scan-app. 

The backend is compiled to a Java .jar which takes a tournament SKU as a command line argument upon execution.
After doing its calculations and making its requests to the VexDB API, the jar returns a JSON list of teams and their associated scores. 

The Node.js server takes this JSON data and returns it to a client (usually the Flutter app built for this project) upon receiving a GET request from the client. It also caches it in a MongoDB database, and refreshes approximately every 20 minutes. 

The front facing app is written with Flutter, the cross-platform SDK for Android and iOS app development. You can use the Flutter CLI to build the APK (compiled package/app) needed to install this app on Android. You can also use Xcode to build this app on iOS. 

Usage, modification, and sharing of this app and source code behind it is permitted in accordance with the GNU GPL v3.0 license. In accordance with the usage regulations set out in that license, Vex Robotics Competition teams are required to credit and acknowledge the original developers (Arjun Vedantham and VRC team 4001A) in documentation and judges' interviews. 
