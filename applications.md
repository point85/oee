---
layout: page
title: Applications
permalink: /apps/
---
<h2>JavaFX Applications</h2>
<h3>Designer Application</h3>
The Designer configures all aspects of equipment in order to enable OEE calculations. It has editors for defining the plant model, reasons, materials, units of measure and work schedule. 
<img src="../resources/images/designer-plant-entities.png" alt="Designer" style="width:100%; display: block; margin-left: auto; margin-right: auto;"> 
Design-time data can also be backed up and restored or imported from a file.
​
The Designer can also display a dashboard for the selected equipment.

Para:
The Designer and Monitor have a trending capability to observe the input and output values of a configured data source. In this example, OPC DA.
Collector Application Para:
The Collector application runs as a Windows service or Unix daemon on the configured host computer. A Collector executes equipment event resolver scripts upon receipt of an input value and stores the availability, production, material or job change event data in the database. This data is used for OEE, MTBF and MTTR calculations.
Monitor Application Para:
The Monitor application has three main functions, to observe:
Equipment performance via metrics available in the dashboard.

Notifications from the data collectors for abnormal conditions

Data collector status.



An example of dashboard tiles is:
Para:
Production and availability events can be shown in chronological order, for example:
Para:
Production and availability events can also be shown in a trend chart, for example:
Para:
The time-losses tab shows a bar chart of the OEE loss categories:
Para:
A first-level Pareto chart show the time losses in percentage terms, for example:
Para:
A second-level Pareto displays the reasons for an availability category, for example for Minor Stoppages:
Operator Desktop Application Para:
This Operator application is a desktop application that allows a user to enter availability, performance, production, material change and job events. The events can be recorded in chronological order as they happened or in summary form over a period of time by duration of the event.
<h2>Flutter Applications<h2>
<h2>Vaadin Application<h2>