# CEF Context Broker - Functional Documentation of the Enabler

**Table of Contents**
1. [Introduction](#introduction)  
    1.1 [How to Access the  Enabler](#subparagraph1)  
    1.1 [Initial configuration Assistant](#subparagraph2)  
2. [Configuration](#paragraph2)  
    2.1 [Configuring Context Broker](#subparagraph7)  
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.1.1 [Services](#subsubparagraph2)   
    2.2 [Historical Data Tools](#subparagraph8)   
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.2.1 [Cygnus](#subsubparagraph2)  
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.2.2 [STH-Comet](#subsubparagraph3)   
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.2.3 [Tool Configuration](#subsubparagraph4)   
3. [Dashboard](#paragraph1)  
    3.1 [Map](#subparagraph3)  
    3.2 [Sensors](#subparagraph4)  
    3.3 [Search Bar](#subparagraph5)  
    3.4 [Managing the Sensors](#subparagraph6)  
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.4.1 [Layers](#subsubparagraph1)  
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.4.2 [Filters](#subsubparagraph1)   
4. [Historical Data](#paragraph3)    
    4.1 [Tables](#subparagraph10)  
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.1.1 [Filters](#subsubparagraph5)   
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.1.2 [Information](#subsubparagraph6)   
    4.2 [Graphics](#subparagraph11)   
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.2.1 [Filters](#subsubparagraph7)   
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4.2.2 [Information](#subsubparagraph8)   
    4.3 [CSV Data Export](#subparagraph12)

# 1 Introduction <a name="introduction"></a>
The aim of this document is to create a functional guide to ensure the understanding of the enabler, so the users are able to exploit it to its fullest.
This enabler has been created to ease the understanding of data and use of the Context Broker and to fasten its learning curve for new stakeholders who would like to experiment. It consists in a visualization layer over the Sandbox environment of the Context Broker used for playground purposes.
The enabler is available for use in local or remote environments. There is available an installation manual to ease its implementation and deployment. 
On the other hand, the enabler gives the opportunity to play with a sensor’s historical data, if configured. Having selected a range of time, it can be represented in a table or even downloaded in a CSV file to further exploit. Furthermore, one of the attributes at a time can be selected and represented in a graphic.  

## 1.1 How to access the Enabler <a name="subparagraph1"></a>
Once the Enable has been deployed either on local, remote server or Sandbox, the user is able to access via web browser, as this Enabler is a web application. This deployment is further explained in the technical documentation, which can be found here.
In order to access the user should introduce in the web browser’s search bar the URL where the Enabler has been deployed, i.e. localhost:5200 is set by default.
>*IMAGEN 1*

## 1.2 Initial configuration Assistant <a name="subparagraph2"></a>
Once the user access for the first time to the Enabler, there is not information to be displayed. It is necessary to configure one instance of a Context Broker at least. Hence, a pop-up will appear giving the option to the user to be redirected to the Configuration page and start configuring a new instance.  
> *IMAGEN 2*

# 2 Configuration <a name="paragraph2"></a>
With the purpose of facilitating the integration of one or various Context Brokers and historical data tools, the Enabler provides a configuration panel that is visual and intuitive. The user can use this panel to configure the information that is desired to be visualized.
This configuration is divided into three sections: how to configure and edit a Context Broker, how to add services, if any, and how to configure the historical data tools if necessary.   

## 2.1 Configuring Context Broker <a name="subparagraph7"></a>
The “Add Context Broker” button at the top part of the illustration x, should be clicked to a new configuration tab for a Context Broker. For the first access, the tab for the configuration of a new instance is automatically opened.
When an empty tab is open, the user should introduce the desired name for that particular Context Broker and the URL where the data is available. Note that there may be the need to indicate the Context Broker’s port if the instance is serving in determined one. For example, if it is configured in local and the port number is 1026, the URL should be localhost:1026.
When that configuration is settled, the user should check the status of that Context Broker and ensure that the configuration provided is valid and ready to go, this can be done by clicking the yellow checkbox next to the URL.  
>*IMAGEN 3*  
>*IMAGEN 4*    

If the URL introduced for the Context Broker is incorrect, a message under the URL box will appear informing of the unsuccessful connection.      
>*IMAGEN 5*  


After the initial configuration of the Context Broker is cleared, the user should choose the desired entities and attributes from it by clicking the bottom option shown in the illustration 9.  

>*IMAGEN 6*  
>*IMAGEN 7*  

The entities and attributes can be selected and unselected by clicking on the checkbox or the name of the desired option. If no entities are selected in the Context Broker an error message will appear, as shown in illustration x.  
If various Context Brokers are added, they will appear as a list where each one can be displayed for its edition. If the user desires to delete a Context Broker the icon at the right part of the name should be clicked. A message will appear asking to confirm the action, this should be done by clicking the delete option in illustration x.     

>*IMAGEN 8*   
>*IMAGEN 9*  

### 3.1.1 Services <a name="subsubparagraph2"></a>
The information of a Context Broker can be organized and divided in what is called “Services”. With this, the information can be encapsulated in different groups and access to them has to be granted. The aim of this tool, that is optional, is to increase the security of the CB data, by dividing it in groups and only grant access to specific users. A user may have access to one service but not to the rest. Therefore, the user has the option of adding a service if necessary. If more information is needed, it can be found here.
If the user has access to one or several services, they can be added, edited and eliminated. In order to add a new service to a Context Broker, the checkbox marked in the illustration 22 should be clicked. A new box with the Services configuration will be opened where the user can start configuring them.   

>*IMAGEN 10*  

The user should click the “Add Service” option, shown at the top of the illustration x, so as to add as many Services as needed.  

>*IMAGEN 11*  

The user will need to configure the name of the service and, if desired, the service path. To check its availability, the “choose entities and attributes” button should be clicked. If this configuration is incorrect a message indicating so will appear informing that there are no entities for it.     

>*IMAGEN 12*  
>*IMAGEN 13*  

If the configuration is correct, a list of the available entities and attributes will appear, where the user can select or unselect the desired ones. However, at least one entity has to be selected, if not an error message, shown in illustration 27, will appear.  

>*IMAGEN 14*  
>*IMAGEN 15*  

A list of the introduced services will appear where the user can edit by clicking the service name or deleted by clicking the icon in the right part of the illustration. A confirmation message will appear where the user should click the delete option to finish the action.    

>*IMAGEN 16*  
>*IMAGEN 17*  

  

## 2.2 Historical Data Tools <a name="subparagraph8"></a>
In order to complement the real-time data, the Enabler offers the possibility to combine it with historical data. Hence, the user is able to optionally configure tools for its implementation in the Configuration page.
The historical data in the Enabler supports two tools that must be configured for each of the Context Brokers as they work together, if any of the tools is not available, the visualization of the historical data will not be possible. The supported tools for the historical data are Cygnus and STH-Comet.
### 2.2.1 Cygnus <a name="subsubparagraph2"></a>  
The first of this two tools is Cygnus. It acts as a connector between the Context Broker’s information that the sensors produce and the MongoDB database that will storage that information. Basically, Cygnus is subscribed to the information the CB produces and creates the historical data for the database. More information can be found at this [link](https://fiware-cygnus.readthedocs.io/en/latest/).   
### 2.2.2 STH-Comet <a name="subsubparagraph3"></a>    
The second tool is STH-Comet. In essence, this tool retrieves the historical data created by Cygnus from the database and allows the user to consult and work with it. If needed, the user can find more information [here](https://fiware-sth-comet.readthedocs.io/en/latest/).  
### 2.2.3 Tool Configuration <a name="subsubparagraph4"></a>    
In conclusion, if the user wants to use the historical data, Cygnus and STH-Comet must be configured for each of the Context Brokers. The user should introduce the desired URL and the chosen port for each of the tools and check the availability for them. If any of the tools is not available, the configuration and exportation of the historical data will not be possible.
If the introduced URL is not correct, an error message informing the unsuccessful connection will appear.

>*IMAGEN 18*    
>*IMAGEN 19*  

# 3 Dashboard <a name="paragraph1"></a>
## 3.1 Map <a name="subparagraph3"></a>
The map that supports the Enabler is the open source World map [OpenStreetMaps](https://www.openstreetmap.org/). Since the CB has its real-time data geolocalized, it will appear automatically when the user adds any new CB.   
The Enabler supports the use of various CB, therefore, all of the CBs added will be shown in the map with the real-time information they provide from the sensors.
## 3.2 Sensors <a name="subparagraph4"></a>
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

## 3.3 Search Bar <a name="subparagraph5"></a>
A search bar is available to localize places in a faster way. The user has to introduce the name of the location they wish to see and it will automatically appear in the map. If the location does not appear, the user may try a similar location.
## 2.4 Filters <a name="subparagraph6"></a>
The user will be able to add dynamic filters to eliminate certain icons from the map in case they want to focus in a specific aspect of any of the attributes. For example, if there is a need to localize the higher priority risk alerts in order to take actions faster.  
If the user wants to add any filter, the conditions will be available when unfolding the attribute options as seen in illustration x. Furthermore, the user will be able to uncheck any of the information that was previously added in the CB’s initial configuration. If the user wants to eliminate any of the entities or attributes that were included before, it will be possible to modify this configuration from this interface.
### 2.4.1 Adding Conditions <a name="subsubparagraph1"></a>
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


# 4 Historical data <a name="paragraph3"></a>
When selecting a sensor there might be a “Show historical data” option available in the pop-up as shown in illustration x. In order for this option to appear, the Context Broker that provides information for that selected sensed has had to be integrated with the historical data tools aforementioned.   
IMAGEN  
With this option, the user will be redirected to the historical data consultation page for that sensor. In this page, this data will be read from the database and the user can choose the rage of time for it to be represented i.e.: days or months. Note that the applied filters will be maintained when consulting the historical data.
## 4.1 Range <a name="subparagraph9"></a>
The user will be able to choose different ranges of time for a same attribute. The ranges of times available are:
- Hours
- Days
- Months
- Years

The user will also be able to customize the beginning and the end of the time period depending on the range selected, in case a specific range of dates or times is required. The table or graphic will show up to the next time level. For instance, if the user selects hours, information up to a day will appear. Note that the range selection is independent for tables and graphics.

## 4.2 Tables <a name="subparagraph10"></a>
After selecting the option of visualizing historical data from a sensor and configuring the range of time desired to consult, a table with the sensor’s attributes’ information will appear. This table will maintain the filters that were configured before and will allow the attributes to be ordered in the table. This attributes can be ordered in ascendant or descendant order and will have up to X entries per page so as to not overload the table and make it difficult to read.
## 4.3 Graphics <a name="subparagraph11"></a>
The purpose of is this functionality is to help the user to further study one of the attributes’ measures. With the aid of the graphic representation of the attribute’s evolution, the user can study more specific aspects about it.  
The user should choose one of the attributes from the sensor and the range of time desired to be visualized in the graphic, as mentioned before, up to a greater unit will be represented. After selecting all the options, a simple graphic will appear automatically with the configuration that the user chose. If the range of time selected is greater than the data available no graphic will appear for the lacking data.

## 4.4 CSV Data Export <a name="subparagraph12"></a>
After the table has been configured, the user will have the opportunity to export the historical data visualized in it to a compatible format file such as CSV.   
The aim of this compatible data exportation is to allow the user to further study the data with other programs without the need to know how to order and extract the historical data from the database, which can be difficult to accomplish.
