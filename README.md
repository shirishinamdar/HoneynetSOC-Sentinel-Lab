Developed custom Azure Sentinel SIEM content and data visualizations to extract geographic insights from 2000+ RDP brute forcealerts enabling global attack pattern analysis.
**VM Creation:**
Using Azure portal, provision a Windows 10 VM in West US region with inbound port 3389 open for Remote Desktop Protocol (RDP) access.
Configure networking settings to allow all traffic to the VM.
**Logging Setup:**
Set up Log Analytics Workspace to ingest logs from the VM, particularly focusing on Windows event logs.
Integrate Azure Sentinel with the Log Analytics Workspace to enable advanced security analytics.
**Logging Enablement:**
Within Microsoft Defender for the Cloud (formerly Security Center), ensure that logging from the VM is enabled and configured to send logs to the Log Analytics Workspace.
**VM Access:**
Connect to the VM using RDP and disable Windows Defender to prevent interference with logging and analysis.
IP Geolocation Integration:
Acquire an API key from ipgeolocation.io to access IP geolocation data.
Incorporate this API key into a provided PowerShell script, which will be used to extract IP geolocation information from the incoming logs.
**Custom Logging Script:**
Utilize a provided PowerShell script, tailored for exporting failed login attempts from Windows event logs.
This script parses the event logs, captures relevant data (like IP addresses), and exports it for further analysis.
**Custom Log Configuration:**
Configure Log Analytics Workspace to accommodate custom logs.
Define the structure of the custom log to store data extracted by the PowerShell script, including fields like hostname, username, IP, etc.
**Data Extraction:**
Extract necessary fields from the logged data using Log Analytics Workspace capabilities.
Save extracted data fields, such as IP addresses, usernames, and geographic locations, for subsequent analysis.
**Analysis and Response:**
Analyze the collected data to identify patterns and trends in attempted cyberattacks.
Utilize the insights gained to enhance security measures, such as updating firewall rules or implementing additional threat detection mechanisms
