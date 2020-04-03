---
permalink: aiops-alert-monitoring/
audit_date: '2020-03-23'
title: AIOps alert monitoring
type: article
created_date: '2020-03-23'
created_by: JP gonzalez
last_modified_date: '2020-03-23'
last_modified_by: JP Gonzalez
product: Global Support
product_url: undefined
---

This article outlines Rackspace **Fanatical Experience®** for network and server configurations for virtual and physical machines that run a supported operating system. The article presents a high-level overview of changes to Rackspace alert monitoring offerings. Contact Rackspace Sales or your account representative for more information regarding the components of specific features that are supported in Rackspace offerings.



### What is changing

Rackspace has been hard at work to bring you AIOps powered improvements to its event processing system. These improvements are now ready for production and will bring the value of event correlation to Rackspace’s monitoring system.  
The new improvements will provide the following additional features to Rackspace’s monitoring system: 
	• Identification of whether an alert is isolated to a single device or multiple devices 
	• Improved alert routing to the Rackspace team(s) best suited to provide support 
Enhanced alert reporting via “situation” notices, which will aggregate related alerts into a single notification.  

### Why

Rackspace is constantly seeking to improve its event processing system to reduce resolution time, decrease ticket noise, and create a better overall customer experience.

### What is AIOps

Rackspace is utilizing  deterministic clustering algorithms which creates Situations defined by the relationships between alerts. Situation creation is based on sets of filters, triggers, and other calculations such as priority ordering.

### Change details

MyRacksapce RNS notifications and Alert Tickets
	• Alerts will be grouped into correlated situations. 
    • A Rackspace support ticket will be created for each situation. 
    • Situations may contain one or more alerts. 
    • Individual alerts notifications will be sent to Rackspace Notification system along with for each situation ticket created. 

### Situation ticket information

Alert grouping logic checks the alerts for applicable situation groups. Situations are created for single alerts or multiple alerts When an alert is correlated to an event with other alerts from the same deveice or additional reated devices.

|	Group	|	Situation Name	|	Notes	|
|-----------|-------------------|-----------|
|	​RS Situation - Infrastructure	|	Situation for Data Center	|	Data Center	|
|	​RS Situation - Infrastructure	|	Situation for devices located together DC	|	Physical Location	|
|	RS Situation - Account level	|	Situation for custom monitor alerts per tenant	|	Custom Monitors	|
|	RS Situation - Account level	|	Situation for custom monitoring device alerts per tenant	|	Custom Monitoring Device	|
|	RS Situation - Account level	|	Situation for generic alerts per tenant	|	Generic	|
|	RS Situation - Multidevice	|	Situation for associated devices	|	Associated Devices	|
|	RS Situation - Multidevice	|	Situation for clustered devices	|	Clustered Devices	|
|	RS Situation - Multidevice	|	Situation for ping associated alerts	|	Ping Associations	|
|	RS Situation - Multidevice	|	URL-Port-Ping failures and connected device alerts from	|	Remote Monitors	|
|	RS Situation - Device level	|	Alerts with the same classification (type)	|	Classification	|
|	RS Situation - Device level	|	Alerts with similar descriptions	|	Description	|
|	RS Situation - Device level	|	Alerts with similar names	|	Name	|
|	RS Situation - Device level	|	Situation for performance and capacity alert per device	|	Performance Capacity	|
|	RS Situation - Device level	|	MBU alert grouping	|	MBU	|
|	RS Situation - Device level	|	Remaining identical alerts	|	Alert	|


### Sample Situation ticket

SITUATION XXX186:Remaining identical alerts
 
Details
Severity Urgent
Status New
Created Mar 12, 2020 09:57:40 (UTC -0500)
Modified Mar 19, 2020 11:14:02 (UTC -0500)
Category Virtualization General
Subcategory Nimbus Alert
Recipients View Recipients - Update


Hello,
We've received the following Situation:
**********************************************************************************************************************
----------------------------------------------------------------------------------------------------------------------
Situation XXX186 Details
----------------------------------------------------------------------------------------------------------------------
**********************************************************************************************************************
SITUATION: Remaining identical alerts
TIME: 2020-03-12 14:53:57
CLUSTERED ALERTS:
DeviceID   Source:Classification:EventName                                                  Sensor ID                                RNS Thread ID
XXXXXX     Nimbus:RS Alert - VMware-ESX:RS Alert - VMware-ESX - Host Status                 HCXXXXXXXX75-62903                         
----------------------------------------------------------------------------------------------------------------------
ACCOUNT NUMBER: XXXXXXX
RBA EVENT ID: dac4bfad-e925-4090-99f2-e9cf91b27b24
SENSOR ID: Situation_XXX186
**********************************************************************************************************************
A Racker will investigate the issue and update this ticket with their findings. If the situation clears first or is resolved through automated remediation, this ticket will be automatically updated and closed.
If you have any questions about this situation, please feel free to contact us or update this ticket at any time.
Thanks,
Rackspace Hosting
(US) 888-480-7640 or (UK)0800 587 2306


### RNS alert notification information

ALERT:OPSMGR:XXXXXX-mon2.url.com:Total CPU Utilization Percentage is too high
XXXXXX (device number) - XXXXXX-mon2.url.com - Account Name

Thursday, November 7th

Original Message 3:54 PM 
We are notifying you about the following alert: ********************************************************************************************************************** ----------------------------------------------------------------------------------------------------------------------
OPSMGR Details
---------------------------------------------------------------------------------------------------------------------- ********************************************************************************************************************** 
ALERT NAME: Total CPU Utilization Percentage is too high 
TIME (UTC): 2019-11-07 21:50:54 
REASON: The threshold for the Processor Information\% Processor Time\_Total performance counter has been exceeded. The values that exceeded the threshold are: 100.% CPU and a processor queue length of 4. ---------------------------------------------------------------------------------------------------------------------- 
MANAGEMENT GROUP: Account Name 
ACCOUNT NUMBER: Account # 
DEVICE: XXXXXX - XXXXXXX-mon2.url.com 
RBA EVENT ID: 8756f278-a61c-4914-9a51-0ee37bbf9039 
SENSOR ID: 7755c00b-769c-4298-8657-7dcc9855eee0 ********************************************************************************************************************** 
This alert is informational only and no further actions will be taken by Rackspace. If you need any assistance from us, please use the "Create Ticket" button to provide us with your instructions and a Racker will investigate. If it is urgent or an emergency then please call us. 

Thanks, 
Rackspace Hosting
(US) 888-480-7640 or (UK)0800 587 2306

Updated Message 3:55 PM 
Hello, Below are the results of our automated diagnostics scripts in response to the "Total CPU Utilization Percentage is too high" alert: Processor Hardware Details: 
|	Cores Per Processor:	|	1	|
|	Processor Manufacturer:	|	GenuineIntel	|
|	Processor Name:	|	Intel(R) Xeon(R) CPU E5-2630 v3 @ 2.40GHz	|
|	Total Number of Processor/s:	|	1	|

Is Server Physical or Virtual: 
|	PhysicalorVirtual:	|	Virtual
|	VirtualType:	|	VMWare

Server Connections: 
|	Established:	|	19	|
|	Close Wait:	|	0	|
|	Fin wait 2:	|	0	|
|	Time Wait:	|	3	|

Top CPU utilizing processes: 
|	ProcessName	|	%ProcessorTime	|	PID	|
|	SVCHOST_724	|	99	|	724	|


The server is responding at this time, no further investigation will be done. If you have any questions, please feel free to contact us at any time.

Thanks,
Rackspace Hosting US: 888-480-7640 | UK: +44 (0)20 8734 2700

### Correlating an alert to a situation
The alert "SENSOR ID" can used by a Racker to lookup the corrponding situation ticket.