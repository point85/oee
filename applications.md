---
layout: page
title: Applications
permalink: /apps/
---
<h2>JavaFX Applications</h2>
<h3>Designer Application</h3>
The Designer configures all aspects of equipment in order to enable OEE calculations. It has editors for defining the plant model, reasons, materials, units of measure and work schedule. 

<img src="../resources/images/designer-plant-entities.png" alt="Designer" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

Design-time data can also be backed up and restored or imported from a file.  The Designer can also display a dashboard for the selected equipment.

The Designer and Monitor have a trending capability to observe the input and output values of a configured data source. In this example, OPC DA.

<img src="../resources/images/designer-opc-da-trend.png" alt="OPC DA Trend" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

<h3>Collector Application</h3>
The Collector application runs as a Windows service or Unix daemon on the configured host computer. A Collector executes equipment event resolver scripts upon receipt of an input value and stores the availability, production, material or job change event data in the database. This data is used for OEE, MTBF and MTTR calculations.

<h3>Monitor Application</h3>
The Monitor application has three main functions, to observe:
- Equipment performance via metrics available in the dashboard.
- Notifications from the data collectors for abnormal conditions
- Data collector status

An example of dashboard tiles is:

<img src="../resources/images/dashboard-tiles.png" alt="Dashboard Tiles" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

Production and availability events can be shown in chronological order, for example:

<img src="../resources/images/dashboard-events.png" alt="Dashboard Events" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

Production and availability events can also be shown in a trend chart, for example:

<img src="../resources/images/availability-trend.png" alt="Availability Trend" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

The time-losses tab shows a bar chart of the OEE loss categories:

<img src="../resources/images/dashboard-time-losses.png" alt="Time Losses" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

A first-level Pareto chart show the time losses in percentage terms, for example:

<img src="../resources/images/dashboard-first-level-pareto.png" alt="First Level Pareto" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

A second-level Pareto displays the reasons for an availability category, for example for Minor Stoppages:

<img src="../resources/images/dashboard-second-level-pareto.png" alt="Second Level Pareto" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

<h3>Operator Desktop Application</h3>
The Operator application is a desktop application that allows a user to enter availability, performance, production, material change and job events. The events can be recorded in chronological order as they happened or in summary form over a period of time by duration of the event.

<img src="../resources/images/operator-production.png" alt="Operator Production" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

<h2>Flutter Applications</h2>
The Flutter/Dart applications allow a user to enter availability, performance, production, material change and job events. The events can be recorded in chronological order as they happened or in summary form over a period of time by duration of event.  A demonstration HTTP server is running a Collector at IP address 52.37.56.187 on port 8182 hosted on AWS Lightsail.
<h3>iOS Mobile Application</h3>
Below are screen shots of the home page showing the plant entity tree, availability page for entering equipment events, production page for entering produced material quantities and the equipment setup page:

<img src="../resources/images/iOSHomePage.png" alt="iOS Home" style="width: 45%; display: inline-block; margin-right: 5%;">
<img src="../resources/images/iOSAvailabilityPage.png" alt="iOS Availability" style="width: 45%; display: inline-block;">

<img src="../resources/images/iOSProductionPage.png" alt="iOS Production" style="width: 45%; display: inline-block; margin-right: 5%;">
<img src="../resources/images/iOSSetupPage.png" alt="iOS Setup" style="width: 45%; display: inline-block;">

<h3>Android Mobile Application</h3>
The Android screens are similar to the iOS screens.  For example, the home entity and availability pages are:

<img src="../resources/images/AndroidHomePage.png" alt="Android Home" style="width: 45%; display: inline-block; margin-right: 5%;">
<img src="../resources/images/AndroidAvailabilityPage.png" alt="Android Availability" style="width: 45%; display: inline-block;">

<h3>macOS Application</h3>
The screen capture below is from the macOS application home page:

<img src="../resources/images/macOSHomePage.png" alt="Mac Home" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

<h3>Windows Application</h3>
The screen capture below is from the Windows application home page:

<img src="../resources/images/WindowsHomePage.png" alt="Windows Home" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

<h3>Linux Application</h3>
The screen capture below is from the Linux application home page:

<img src="../resources/images/LinuxHomePage.png" alt="Linux Home" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

<h3>Chrome/Edge Application</h3>
The screen capture below is from the Chrome/Edge application home page:

<img src="../resources/images/ChromeHomePage.png" alt="Chrome Home" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

<h2>Vaadin Application</h2>

The Operator web application is browser-based and allows a user to enter availability, performance, production, material change and job events. The events can be recorded in chronological order as they happened or in summary form over a period of time by duration of event.

Below is the screen for entering summarized availability data.

<img src="../resources/images/operator-web-availability.png" alt="Operator Web" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

<a href="./index.html">Back to Applications</a>