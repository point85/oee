---
layout: page
title: Implementation
permalink: /impl/
---
<h2>Overview</h2>
The time-loss model discussed in the <a href="../index.html">Introduction</a> is implemented by open source projects hosted on GitHub. The parent project is the [OEE Designer](https://github.com/point85/OEE-Designer).  From the latest release, download the Point 85 OEE Getting Started and Point 85 OEE User Guide documents for more details. The binary code is in the oee-*version*.zip file on this page.
​
The Point 85 OEE applications enable:
- Collection of equipment data from multiple sources to support OEE calculations or general purpose data acquisition
- Resolution of a collected data value into an availability reason or produced material quantity to provide input to the performance, availability and quality components of OEE
- Calculation of the OEE key performance indicator for the equipment using an optional work schedule for defining the scheduled production time
- Monitoring of equipment availability, performance and quality events

<h2>Data Collection</h2>
Sources of equipment availability, performance and quality event data include:
- **Manual**: web browser, Android app or iOS app data entry
- **OPC DA**: classic OLE for Process Control (OPC) Data Acquisition (DA)
- **OPC UA**: OLE for Process Control Unified Architecture (UA)
- **HTTP/S**: invocation of a web service via an HTTP/S request
- **RMQ Messaging**: an equipment event message received via a RabbitMQ message broker
- **JMS Messaging**: an equipment event message received via a JMS message broker
- **MQTT Messaging**: an equipment event message received via an MQTT message server
- **Kafka Messaging**: an equipment event message received via a Kafka message server
- **Web Socket Messaging**: an equipment event message received via a web socket server
- **Email**: an equipment event message received via an email server
- **Database Interface Table**: a predefined table for inserting OEE events from a relational database
- **File Share**: a server hosting OEE event files
- **Modbus**: a Modbus master communicating with its slaves.
- **Cron Job**: a cron job scheduled to execute at specified points in time
- **GE Proficy Historian**: a historian collecting tag data

<h2>Applications</h2>
The Point85 applications supporting OEE are:
- **Designer**: a desktop GUI application for defining the plant equipment, data sources, event resolution scripts, manufacturing work schedule, availability reasons, produced materials and units of measure for data collectors. The designer also includes a dashboard and trending capabilities.
- **Collector**: a headless Windows service or Unix deamon to collect the equipment event data and store it in a relational database
- **Monitor**: a desktop GUI application with a dashboard to view the current equipment OEE and status
- **Operator**: a desktop GUI application for manual entry of equipment events
- **Operator Web**: a web-application for manual entry of equipment events
- **Operator Mobile iOS App**: an iOS application for manual entry of equipment events available in the Apple App Store
- **Operator MacOS App**: a MacOS application for manual entry of equipment events available in the Apple App Store
- **Operator Mobile Android App**: an Android application for manual entry of equipment events available in the Google Play Store
- **Operator Windows App**: a Windows app for manual entry of equipment events
- **Operator Linux App**: a Linux app for manual entry of equipment events
- **Operator Web App**: a Chrome/Edge browser app for manual entry of equipment events

In addition, two GUI test applications assist in the development of an OEE solution:
- **Tester**: a desktop HTTP requester and a message publisher
- **Test Collector**: a desktop UI front-end for a data collector

The data for calculating OEE can be entered manually (for example at the end of a shift) or be collected from a data acquisition system event from one or more of the above data sources. For manual data collection the data can be summarized over a period of time (e.g. a shift) or entered as the events occurred. Collecting data at the event level allows for Mean Time Between Failure (MTBF) and Mean Time to Repair (MTTR) calculations.

<h2>System Architecture</h2>

The diagram below is an section of the system architecture:
<img src="../resources/images/system-architecture.png" alt="System Architecture" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 

The OEE applications can be grouped into design-time and run-time. The design-time Designer application is used to define the plant equipment, data sources, event resolution scripts, manufacturing work schedule, availability reasons, produced materials and units of measure for data collectors. The designer also includes a dashboard and trending capabilities.

​An automated run-time data collector receives an input value from a data source source and executes a JavaScript resolver on this input to calculate an output value. The output value is a reason (mapped to an OEE loss category) for availability or performance events, a new production count (good, reject/rework or startup) for quality events or a material/job change event. For the case of a custom event, the output value is ignored.

The event data is stored in a relational database using the Java Persistence API (JPA) where it is available for OEE calculations. Microsoft SQL Server, Oracle, MySQL, PostgresQL and HSQLDB are currently supported.

A mobile or web-based manual data collector running in a web server records the OEE events based on information entered by an operator. Similar to the automated collector, this data is also stored in the relational database.

If the system is configured for messaging, the event data is also sent to a RabbitMQ, JMS, MQTT or Kafka message broker to which a run-time monitor application can subscribe. A monitor displays a dashboard for viewing equipment OEE events. It also displays collector notifications and status information.

The Java Persistence 2.2 API (JPA) as implemented by the Hibernate ORM framework together with the Hikari connection pool is used to persist OEE information to the database.

<h2>Database</h2>
Hibernate and JPA abstract away database specific aspects of inserting, updating, reading and deleting records in the tables. The API is designed to work with any relational database supported by Hibernate.

Microsoft SQL Server, Oracle, MySQL, PostgresQL and HSQLDB are currently supported.

<h2>Getting Started</h2>
The source code, binaries and documentation can be downloaded from these Github repositories:
- JavaFX desktop applications (Designer, Monitor, Operator, Collector & Tester): [OEE Desktop](https://github.com/point85/OEE-Designer)
- OEE domain library: [OEE Domain](https://github.com/point85/OEE-Domain)
- Collector service: [OEE Collector](https://github.com/point85/OEE-Collector)
- Vaadin web application: [OEE Vaadin](https://github.com/point85/OEE-Operations)
- Flutter applications (iOS, Android, Linux, Windows, macOS, Chrome/Edge): [OEE Flutter](https://github.com/point85/OEE-Mobile)

The JavaFX desktop applications along with the collector service are packaged in the oee-*version*.zip file in the latest Git release. Download the and expand the archive into a folder of your choice. Next, download the *Point85 OEE Getting Started Guide* and follow instructions in that document. Additional information may be found in the *Point85 OEE User Guide*.

The Vaadin web application is packaged in the OEE-Operator-*version*.war file in the latest Git release. Download the file and deploy it to a web server that supports war deployment, e.g. Tomcat.

The Flutter iOS and macOS apps can be downloaded from the Apple App Store (search for "Point85 OEE") and the Android app from the Google Play Store (search for "OEE Point85").  The Windows, Linux and Chrome/Edge apps can be downloaded from the latest release in the git repository - oee_win_*version*.zip, oee_linux_*version*.zip or oee_web_*version*.zip.  Expand the archives into a folder of your choice.  For Windows and Linux, run the respective executable files (e.g. oee_win.exe).  For Chrome, start a web server from the index.html file location.

<a href="./index.html">Back to Implementation</a>