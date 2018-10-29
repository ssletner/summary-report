# summary-report

This playbook generates reports of the lab environment build in this class. 

The playbook reports.yml performs the following actions.

- Makes the directories /docs/reports and /docs/reports/yml
    - /reports is used for the reports generated following the j2 template
    - /reports/yml is used for the the dumps of all facts in yml format
    - /docs is where the master reports are stored

- Gathers IOS facts from all iosxe devices in the lab
    - creates a text files using j2 template per device
    - creates a yml file of ALL found on the device

- Gathers NXOS facts from all nxos devices in the lab
    - creates a text files using j2 template per device
    - creates a yml file of ALL found on the device

- Generates final report
    - master text report which combines all text files created from j2 template 
    - master yml report which combines all yml files and includes all facts


The report includes the following information:
Hostname:      
Vendor:        
Model:         
OS Version:    
Serial Number: 

## Lab

The <a href="https://github.com/ssletner/virl-lab">virl-lab</a>  topology was used for the report. 

![alt text](https://github.com/ssletner/virl-lab/blob/master/virl-lab-leaf-spine.jpg "Lab Topology")
