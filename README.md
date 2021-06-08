# HomeWizard P1 meter template for Zabbix

This project contains a template to read the local API of your HomeWizard P1 wifi meter. See: https://www.homewizard.nl/homewizard-wi-fi-p1-meter

# Setup

## Zabbix 5.x

Given I am exporting those templates from 5.4 as of now, you will need Zabbix 5.x minimum to be able to import the templates. 

## Import the template into Zabbix

Import zbx_export_templates.xml into Zabbix, from Configuration > Templates > Import

## Macros
The Macro's below are set for a future update and not used by a trigger. 

### { $HOMEWIZARD_PHASE_LIMIT}
The default value is 5750 Watts (25 Amps per fase * 230 Volts). 

### {$HOMEWIZARD_TOTAL_LIMIT}
The default value is 5750 Watts (25 Amps per fase * 230 Volts * 3 phases)

# Graphs
If everything is working you should be able to see data flowing in the Monitoring > Latest Data section of Zabbix.  Time to set up some graphs.

## Total power usage 
![Total power usage](/images/totalPower.png)

# Todo (Future additions)

## Trigger with the maximum utility limit 
## Plot the voltages of each phase using the RAW API data. 
