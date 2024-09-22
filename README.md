# Azure Sentinel Honeypot: Mapping Live Cyber Attacks

## Overview

This project demonstrates how to set up an Azure honeypot virtual machine and configure Azure Sentinel to visualize and analyze live cyber attacks from around the world. By creating an intentionally vulnerable system, we gain valuable insights into the tactics, techniques, and procedures (TTPs) used by attackers, enabling us to enhance our security posture and incident response capabilities proactively.

## Key Features

- Real-time monitoring of global cyber attacks
- Geolocation data for attack sources
- Custom log ingestion for failed login attempts
- Azure Sentinel integration for advanced threat analytics
- Visualizations of attack patterns and sources

## Setup Instructions

1. **Create a Virtual Machine**
   - Use a Windows 10 image
   - Open inbound port 3389 (RDP) for remote access

2. **Configure Network Security**
   - Create a Network Security Group (NSG)
   - Allow all inbound traffic to make the VM discoverable

3. **Set up Log Analytics Workspace**
   - Ingest logs from the virtual machine
   - Enable integration with Microsoft Defender for Cloud

4. **Configure Azure Sentinel**
   - Add Sentinel to your Log Analytics Workspace
   - Connect to the honeypot VM via RDP
   - Disable Windows Defender on the VM

5. **Collect Failed Login Logs**
   - Use the Custom_Security_Log_Exporter.ps1 script
   - Integrate with ipgeolocation.io for geolocation data

6. **Ingest Custom Logs into Azure Sentinel**
   - Create a custom log table in Log Analytics Workspace
   - Configure appropriate collection paths and field details

7. **Visualize and Analyze Cyber Attacks**
   - Extract relevant fields from log entries
   - Use Azure Sentinel's mapping capabilities
   - Create custom dashboards and visualizations

## Benefits

- **Real-world Threat Intelligence**: Gain insights into current attack trends and techniques.
- **Improved Incident Response**: Develop and test response strategies based on actual attack data.
- **Enhanced Security Posture**: Use attack pattern analysis to strengthen defenses proactively.
- **Geographical Attack Mapping**: Visualize the global distribution of attack sources.
- **Custom Threat Detection**: Develop and refine detection rules based on observed attack behaviors.

## Cautions

- This project involves creating an intentionally vulnerable system. Ensure it's isolated from your production environment.
- Follow all relevant legal and ethical guidelines when setting up and operating a honeypot.
- Regularly monitor and maintain the honeypot to prevent it from being used as a launch point for attacks on other systems.

## Further Reading

- [Microsoft Azure Sentinel Documentation](https://docs.microsoft.com/en-us/azure/sentinel/)
- [Honeypot Security: Pros and Cons](https://www.cloudflare.com/learning/security/glossary/honeypot-security/)
- [SANS Institute: Building a Honeypot](https://www.sans.org/reading-room/whitepapers/detection/building-honeypot-169)

## Contributing

We welcome contributions to improve this project. Please submit pull requests or open issues on our GitHub repository.

## License

This project is licensed under CC BY 4.0. See the LICENSE file for details.
