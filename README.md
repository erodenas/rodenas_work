# CEF Context Broker - Functional documentation of the enabler

**Table of Contents**
#### 1 [Introduction](https://github.com/rodenas_work/README.md "Introduction")

# 1 Introduction
The aim of this document is to create a functional guide to ensure the understanding of the enabler, so the users are able to exploit it to its fullest.  
This enabler is pretended to ease the use of Context Broker and to fasten its learning curve for new stakeholders to experiment. It consists in a visualization layer over the Sandbox environment of the Context Broker used for playground purposes.  
The enabler will be available for use in local or remote environments and will help the user to further deepen the knowledge about the use of Context Brokers and their uses. Furthermore, there is the possibility to represent it in visual forms as tables or graphics in the visualization layer and export compatible historical data stored from the sensors so as to allow the user to use it with different applications.

## 1.1 How to Acces the Enabler
In order to access the Enabler, the user will have to access to the link provided and download the Enabler's code, then display the code in their Context Broker. In case of any doubt, this process is explained in the technical manual that can be found here. The user can follow this manual to correctly implement the enabler in the Context Broker.  
Once the user has correctly displayed the code following the technical documentation provided, to access the enabler the following link should be clicked or copied to the web browser's search bar.  
The user can also add this code in their FIWARE lab and work in the cloud instead of local, also explained in the technical documentation.
## 1.2 Initial configuration Assistant
 The first time the user access to the enabler there will be an initial configuration assistant so as to help the user familiarize with its configuration. Hence, a pop-up will appear giving the option to the user to be redirected to the configuration window.  
If the user decides to empty the map, this assistant will appear again.  

![](https://github.com/erodenas/rodenas_work/blob/master/Diapositiva1.PNG)
# 2 Dashboard
## 2.1 Maps
The map that supports the Enabler is the open source World map [OpenStreetMaps](https://www.openstreetmap.org/). Since the CB has its real-time data geolocalized, it will appear automatically when the user adds any new CB.   
The Enabler supports the use of various CB, therefore, all of the CBs added will be shown in the map with the real-time information they provide from the sensors.
## 2.2 Icons
The icons that appear in the map respond to a list of categories that classifies the data in different groups depending on the type of information it gives:
-    Alerts: for information about risks or warnings.
-    Smart Environment: for Environment, Waste management and Weather.
-    Environment: monitoring air quality and other environmental conditions.
-    Point of interest: locations that may be useful or interesting.
-    Civic issue tracking:
-    Street lighting: modeling street lights and their controlling equipment
-    Device: for IoT devices.
-    Transportation: transportation data models
-    Indicators: KPI to measure the success of organizations.
-    Waste management: for efficient, recycling waste management.
-    Parking: status of the parking spots (on street and off street)
-    Weather: weather observed, forecasted or warnings for potential extreme conditions.

If more information about these categories is needed, the FIWARE data models can be consulted through this  [link](https://www.fiware.org/developers/data-models/).

## 2.3 Search Bar
A search bar is available to localize places in a faster way. The user has to introduce the name of the location they wish to see and it will automatically appear in the map. If the location does not appear, the user may try a similar location.
## 2.4 Filters
The user will be able to add dynamic filters to eliminate certain icons from the map in case they want to focus in a specific aspect of any of the attributes. For example, if there is a need to localize the higher priority risk alerts in order to take actions faster.  
If the user wants to add any filter, the conditions will be available when unfolding the attribute options as seen in illustration x. Furthermore, the user will be able to uncheck any of the information that was previously added in the CB’s initial configuration. If the user wants to eliminate any of the entities or attributes that were included before, it will be possible to modify this configuration from this interface.
### 2.4.1 Adding Conditions
In order to add a new condition to any of the attributes the user has to press the button shown in the illustration x. It appears automatically when displaying the options for any attribute.   
Depending on the type of attribute, text or numerical, a different type of filter will appear and the user will be able to add the desired condition.
- Numerical conditions. The user introduces the desired numeric value and chooses between:
	- Greater than “>”.
	- Greater or equal to “>=”.
	- Less than “<”.
	- Less or equal to “<=”.
	- Equal to “=”.
- Text conditions.
	- Contains “Word”.
	- Has prefix or suffix.

# 3 Configuration
There will be an administration panel available for the user, so as to configure the different context brokers the user may want to add and their entities.
## 3.1 Configuring Context Broker
When the user wants add a new Context Broker, the “Add Context Broker” option at the left part of the illustration x, should be clicked. A configuration page will be opened where the user should introduce the desired name for that particular Context Broker, the URL where the data is available and the number of the chosen port. When that configuration is settled the user should check the status of that Context Broker and ensure that the configuration provided is valid and ready to go.   
After the initial configuration of the Context Broker is cleared, it will appear in the list of available Context Brokers, shown in the left part of the illustration x.
## 3.1.1 Services
The information of a Context Broker can be organized and divided in what is called “Services”. With this, the information can be encapsulated in different groups and access to them has to be granted. The aim of this tool, that is optional, is to increase the security of the CB data, by dividing it in groups and only grant access to specific users. A user may have access to one service but not to the rest. Therefore, the user has the option of adding a service if necessary.  
If the user has access to one or several services, they can be added, edited and eliminated. In order to add a new service to a Context Broker, the user should click the “Add Service” option, shown at the bottom of the illustration x.  
The user will need to configure the name of the service and the service path, at the right part of the service list, the user will find the edit and eliminate options, in case they want to modify the initial configuration that was given.
## 3.2 Historical data tools
The use of the historical data is completely optional. If the user does not wish to use it, is configuration is avoidable with any impact to the rest of the Enabler.   
The historical data has available two tools that must be configured for each of the Context Brokers as they work together, if any of the tools is not available, the configuration and exportation of the historical data will not be possible.
The first of this two tools is Cygnus. It acts as a connector between the CB’s information that the sensors produce and the MongoDB database that will storage that information. Basically, Cygnus storages the information the CB produces and creates the historical data for the database. More information can be found at this [link](https://fiware-cygnus.readthedocs.io/en/latest/).  
The second tool is STH-Comet. In essence, this tool retrieves the historical data created by Cygnus from the database and allows the user to work with it in forms of tables or graphics. Furthermore, it can be exported to a CSV file. If needed, the user can find more information [here](https://www.fiware.org/developers/data-models/https://fiware-sth-comet.readthedocs.io/en/latest/).  
In conclusion, if the user wants to use the historical data, Cygnus and STH-Comet must be configured for each of the Context Brokers. The user should introduce the desired URL and the chosen port for each of the tools and check the availability for them. If any of the tools is not available, the configuration and exportation of the historical data will not be possible.
# 4 Historical data
When selecting a sensor there might be a “Show historical data” option available in the pop-up as shown in illustration x. In order for this option to appear, the Context Broker that provides information for that selected sensed has had to be integrated with the historical data tools aforementioned.   
IMAGEN  
With this option, the user will be redirected to the historical data consultation page for that sensor. In this page, this data will be read from the database and the user can choose the rage of time for it to be represented i.e.: days or months. Note that the applied filters will be maintained when consulting the historical data.
## 4.1 Range
The user will be able to choose different ranges of time for a same attribute. The ranges of times available are:
- Hours
- Days
- Months
- Years

The user will also be able to customize the beginning and the end of the time period depending on the range selected, in case a specific range of dates or times is required. The table or graphic will show up to the next time level. For instance, if the user selects hours, information up to a day will appear. Note that the range selection is independent for tables and graphics.

## 4.2 Tables
After selecting the option of visualizing historical data from a sensor and configuring the range of time desired to consult, a table with the sensor’s attributes’ information will appear. This table will maintain the filters that were configured before and will allow the attributes to be ordered in the table. This attributes can be ordered in ascendant or descendant order and will have up to X entries per page so as to not overload the table and make it difficult to read.
## 4.3 Graphics
The purpose of is this functionality is to help the user to further study one of the attributes’ measures. With the aid of the graphic representation of the attribute’s evolution, the user can study more specific aspects about it.  
The user should choose one of the attributes from the sensor and the range of time desired to be visualized in the graphic, as mentioned before, up to a greater unit will be represented. After selecting all the options, a simple graphic will appear automatically with the configuration that the user chose. If the range of time selected is greater than the data available no graphic will appear for the lacking data.

## 4.4 CSV data export
After the table has been configured, the user will have the opportunity to export the historical data visualized in it to a compatible format file such as CSV.   
The aim of this compatible data exportation is to allow the user to further study the data with other programs without the need to know how to order and extract the historical data from the database, which can be difficult to accomplish.
