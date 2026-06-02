# Wazuh, Caldera, Sysmon, and AI Log Analysis Lab

## Project Overview

This project involved building a cybersecurity lab environment to simulate cyberattacks, monitor security events, and analyze logs using Wazuh, Sysmon, MITRE Caldera, and AI-assisted log analysis.

---

## Step 1: Create the Virtual Machines

Using VirtualBox, I created three virtual machines:

- Ubuntu Server VM (Wazuh Server)
- Windows 10 VM (Target Endpoint)
- Kali Linux VM (Attacker Machine)

### Screenshot: Virtual Machines

![Virtual Machines](images/vms-overview.png)

---

## Step 2: Install and Configure Wazuh

I installed Wazuh on the Ubuntu Server VM and configured the Wazuh Manager, Indexer, and Dashboard. After installation, I verified all services were running and confirmed access to the web dashboard.

### Screenshot: Wazuh Installation

![Wazuh Installation](images/wazuh-installation.png)

### Screenshot: Wazuh Dashboard

![Wazuh Dashboard](images/wazuh-dashboard.png)

---

## Step 3: Add the Windows 10 Endpoint

I installed the Wazuh Agent on the Windows 10 virtual machine and registered it with the Wazuh Manager. Once connected, the endpoint began sending logs and security events to the Wazuh server for monitoring.

### Screenshot: Windows Agent Installation

![Windows Agent](images/windows-agent.png)

### Screenshot: Endpoint Connected to Wazuh

![Connected Endpoint](images/endpoint-connected.png)

---

## Step 4: Install and Configure Sysmon

To enhance endpoint visibility, I installed Sysmon (System Monitor) on the Windows 10 VM. Sysmon was configured to log detailed system activity, including process creation, network connections, file modifications, registry changes, and PowerShell execution events. Wazuh was configured to ingest Sysmon logs, providing deeper visibility into endpoint behavior and improving threat detection capabilities.

### Screenshot: Sysmon Installation

![Sysmon Installation](images/sysmon-install.png)

### Screenshot: Sysmon Events in Wazuh

![Sysmon Events](images/sysmon-events.png)

---

## Step 5: Install Kali Linux and MITRE Caldera

I configured a Kali Linux virtual machine and installed MITRE Caldera. Caldera was used to simulate adversary behavior and execute attack techniques based on the MITRE ATT&CK framework.

### Screenshot: Kali Linux

![Kali Linux](images/kali-linux.png)

### Screenshot: Caldera Installation

![Caldera Installation](images/caldera-install.png)

### Screenshot: Caldera Dashboard

![Caldera Dashboard](images/caldera-dashboard.png)

---

## Step 6: Execute Attack Simulations

Using MITRE Caldera, I launched attack simulations against the Windows 10 endpoint. The exercises included reconnaissance, privilege escalation, persistence, credential access, and command execution techniques. Sysmon captured detailed telemetry during these attacks, while Wazuh generated alerts based on the collected data.

### Screenshot: Attack Execution

![Attack Execution](images/caldera-attack.png)

### Screenshot: MITRE ATT&CK Techniques

![MITRE ATT&CK](images/mitre-techniques.png)

---

## Step 7: Monitor and Investigate Alerts in Wazuh

While the attacks were running, Wazuh collected Windows Event Logs and Sysmon telemetry, generating alerts for suspicious activity. I reviewed alerts, investigated events, analyzed indicators of compromise (IOCs), and correlated attack activity with MITRE ATT&CK techniques.

### Screenshot: Security Alerts

![Wazuh Alerts](images/wazuh-alerts.png)

### Screenshot: Event Investigation

![Event Investigation](images/event-investigation.png)

---

## Step 8: AI-Assisted Log Analysis

I used AI tools to analyze security logs generated during the attack simulations. AI was used to summarize alerts, identify suspicious behavior, explain detections, highlight indicators of compromise, and assist with incident investigation. This improved the efficiency of reviewing large amounts of security data.

### Screenshot: AI Log Analysis

![AI Analysis](images/ai-analysis.png)

### Screenshot: AI Findings

![AI Findings](images/ai-findings.png)

---

## Skills Demonstrated

- Wazuh SIEM Administration
- Sysmon Configuration and Monitoring
- Endpoint Detection and Response (EDR)
- Security Information and Event Management (SIEM)
- Threat Detection and Analysis
- MITRE ATT&CK Framework
- Adversary Emulation
- Incident Response
- Threat Hunting
- Log Analysis
- AI-Assisted Security Analysis
- Security Operations Center (SOC) Workflows

---

## Project Architecture

```text
+------------------+
|   Kali Linux     |
| MITRE Caldera    |
+--------+---------+
         |
         | Attack Simulation
         v
+------------------+
|   Windows 10     |
| Wazuh Agent      |
| Sysmon           |
+--------+---------+
         |
         | Logs & Telemetry
         v
+------------------+
| Ubuntu Server    |
| Wazuh Manager    |
| Wazuh Dashboard  |
+--------+---------+
         |
         | Log Analysis
         v
+------------------+
| AI Analysis Tool |
+------------------+
```

### Screenshot: Architecture Diagram

![Architecture Diagram](images/architecture-diagram.png)

---

## Conclusion

This lab provided hands-on experience with security monitoring, endpoint visibility, threat detection, adversary emulation, incident investigation, and AI-assisted log analysis. By integrating Sysmon with Wazuh and generating attack activity through MITRE Caldera, I gained practical experience with SOC workflows and cybersecurity tools commonly used in enterprise security environments.
