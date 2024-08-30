### Operation: CR!T!C@L M!SS!0N !MP0SS!BL3

#### **Final Mission Brief**

**Objective:**  
Analyze network traffic (PCAP files) related to a critical infrastructure ICS attack. Identify Indicators of Compromise (IoCs), map them to MITRE ATT&CK for ICS, and document the industrial protocols exploited by the attacker. Deliver a comprehensive report with all findings and optional detection rules in Snort, STIX, Sigma, and YARA formats.

---

### **PCAP Files Location**

The PCAP files necessary for this analysis can be found in the following directory:

```plaintext
/operation_critical_mission_impossible/pcaps/
```

Please ensure to download and review these files thoroughly as they contain the network traffic data required to complete the mission.

### **Executive Summary Structure**

Your **Executive Summary** should be delivered in a file named `index.md` with the following structure:

```markdown
# Executive Summary

**Operation:** CR!T!C@L M!SS!0N !MP0SS!BL3  
**Date:** [Insert Date]  
**Mission Lead:** [Your Name]

## Incident Overview
A critical infrastructure facility experienced a coordinated cyber attack targeting its Industrial Control System (ICS). This report details the findings, including all identified Indicators of Compromise (IoCs), MITRE ATT&CK mappings, and the exploitation of industrial protocols by the attacker.

## Indicators of Compromise (IoCs)
- **IP Addresses:**
  - `192.0.2.123` (Public)
  - `192.168.1.15` (Private - Critical Infrastructure)

- **File Hashes (MD5):**
  - `5d41402abc4b2a76b9719d911017c592`
  - `d2d2d2d2d2d2d2d2d2d2d2d2d2d2d2d2`

- **MAC Addresses:**
  - `00:0a:95:9d:68:16`
  - `00:14:22:01:23:45`

- **Domains/URLs:**
  - `malicious-domain.com`
  - `suspicious-site.org`

## MITRE ATT&CK Mappings
- **Initial Access:**
  - Tactic `TA0001` - Technique `T1078` (Valid Accounts)
  - Tactic `TA0001` - Technique `T1190` (Exploit Public-Facing Application)

- **Lateral Movement:**
  - Tactic `TA0008` - Technique `T1021.002` (SMB/Windows Admin Shares)
  - Tactic `TA0008` - Technique `T1210` (Exploitation of Remote Services)

- **Command and Control:**
  - Tactic `TA0011` - Technique `T1071.001` (Application Layer Protocol: Web Traffic)
  - Tactic `TA0011` - Technique `T1071.002` (Standard Application Layer Protocol: DNS)

## Exploited Industrial Protocols
- **Protocols Used:**
  - `modbus`
  - `dnp3`
  - `iec104`
  - `bacnet`

## Recommendations
- **Security Enhancements:** Immediate measures to protect critical infrastructure.
- **Future Monitoring:** Implement continuous monitoring using the provided detection rules.

---

### **File Format and Submission Instructions**

#### **File Formats:**

Deliver all IoCs and detection rules in the following formats:
- **Snort**: `.rules` files for network-based detection rules.
- **STIX**: `.json` files for structured threat intelligence bundles.
- **Sigma**: `.yml` files for log-based detection rules.
- **YARA**: `.yara` files for file-based detection rules.

**Note:** There is no need to maintain a specific directory structure. Simply ensure that each file is named appropriately and contains the required information.

#### **Submission Instructions:**

To submit your completed files, use the following `curl` command to upload them directly. Replace `<docker-server-ip>` with the IP address of the Docker server hosting the submission endpoint:

```bash
curl -X POST http://<docker-server-ip>:3000/upload -F file=@path/to/your/index.md -F file=@path/to/your/snort_rule1.rules -F file=@path/to/your/ioc_stix_bundle1.json -F file=@path/to/your/ioc_sigma_rule1.yml -F file=@path/to/your/ioc_yara_rule1.yara | python -m json.tool | pygmentize -l json
```

Upload each file individually using the `-F file=@path/to/your/file` option for all relevant files.

---

### **Closing Notes**

This challenge is your opportunity to showcase your expertise in cybersecurity and digital forensics. **Operation: CR!T!C@L M!SS!0N !MP0SS!BL3** demands precision, insight, and a strategic mindset. We trust in your ability to deliver crucial information that will protect our critical infrastructure. **Good luck!** 🚀

---

Feel free to adjust or ask for any more details if needed!