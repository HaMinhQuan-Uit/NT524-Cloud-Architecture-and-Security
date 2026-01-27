# NT524-Cloud-Computing-Architecture-and-Security
------
# Project
•	On project implements a Security Information and Event Management (SIEM) framework using the ELK Stack (Elasticsearch, Logstash, Kibana) to monitor a Hybrid Cloud environment. The infrastructure integrates OpenStack (Private Cloud) and Amazon Web Services (Public Cloud), connected securely via a WireGuard VPN. The system centralizes logs from web servers, database servers, and network devices to detect security threats in near real-time

## Solution architecture for SIEM systems
<img width="921" height="694" alt="image" src="https://github.com/user-attachments/assets/17e7131d-c195-462b-a988-57e85ff97483" />


• Application Flow:
  First, the user connects to the website via an API connecting to a web server located on an AWS EC2 virtual machine.
The web server retrieves information from the Openstack database server, which is a virtual machine instance, via two VPN virtual machines between different cloud platforms.

• SIEM Flow:
  Filebeat is installed on the web server and database server, collecting information from applications used to run services.
Filebeat then pushes logs to Logstash, which normalizes the logs and pushes them to Elasticsearch.
Kibana retrieves the analytics from Elasticsearch, displays the results, and provides alerts on the interface.

## Solution architecture for SIEM systems
<img width="902" height="683" alt="image" src="https://github.com/user-attachments/assets/c164723b-b797-48a5-9e61-8018fba2a05b" />
