# SOC Fundamentals

## SOC Team Roles

### SOC Analyst (Level 1)
Anything detected by the security solution would pass through these analysts first. These are the **first responders** to any detection. SOC Level 1 Analysts perform basic alert triage to determine if a specific detection is harmful. They also report these detections through proper channels.

### SOC Analyst (Level 2)
While Level 1 does the first-level analysis, some detections may require deeper investigation. Level 2 Analysts help them **dive deeper into the investigations** and correlate the data from multiple data sources to perform a proper analysis.

### SOC Analyst (Level 3)
Level 3 Analysts are experienced professionals who **proactively look for any threat indicators** and support in the incident response activities. The critical severity detections reported by Level 1 and Level 2 Analysts are often security incidents that need detailed responses, including **containment, eradication, and recovery**.

### Security Engineer
All analysts work on security solutions. These solutions need deployment and configuration. Security Engineers **deploy and configure** these security solutions to ensure their smooth operation.

### Detection Engineer
Security rules are the logic built behind security solutions to detect harmful activities. Level 2 and 3 Analysts often create these rules, while the SOC team can sometimes also utilize the **Detection Engineer** role independently for this responsibility.

### SOC Manager
The SOC Manager **manages the processes** the SOC team follows and provides support. The SOC Manager also remains in contact with the organization's **CISO** (Chief Information Security Officer) to provide updates on the SOC team's current security posture and efforts.

## Incident Investigation: The 5 Ws

| Question | Answer |
|----------|--------|
| **What?** | A malicious file was detected on one of the hosts inside the organization's network. |
| **When?** | The file was detected at 13:20 on June 5, 2024. |
| **Where?** | The file was detected in the directory of the host: "GEORGE PC". |
| **Who?** | The file was detected for the user George. |
| **Why?** | After investigation, the file was downloaded from a pirated software-selling website. The user downloaded the file to use software for free. |

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
