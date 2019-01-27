_WORK IN PROGRESS_

Mapped to the ATT&CK Framework, these use cases are intended to guide a SIEM team to...
* ... develop a workflow for content creation (and retirement) in the SIEM and other security tools.
* ... illustrate detection coverage provided.
* ... highlight coverage gaps.
* ... determine whether custom signatures are required where vendor signatures are lacking.
* ... elimiante or add additional layers of coverage based on organizational needs.

#### ATT&CK Abbreviations Used
Initial Access (IA), Execution (Exe), Persistence (P), Privilege Escalation (PE), Defense Evasion (DE), 
Credential Access (CA), Discovery (D), Lateral Movement (LM), Collection (C), Exfiltration (Exf), Command and Control (CC)

## Detect | ATT&CK Tactics Cross Mapping

| Detection Tactic                | [IA](https://attack.mitre.org/tactics/TA0001/) | [Exe](https://attack.mitre.org/tactics/TA0002) | [P](https://attack.mitre.org/tactics/TA0003/) | [PE](https://attack.mitre.org/tactics/TA0004) | [DE](https://attack.mitre.org/tactics/TA0005) | [CA](https://attack.mitre.org/tactics/TA0006) | [D](https://attack.mitre.org/tactics/TA0005) | [LM](https://attack.mitre.org/tactics/TA0008) | [C](https://attack.mitre.org/tactics/TA0006) | [Exf](https://attack.mitre.org/tactics/TA0010) | [CC](https://attack.mitre.org/tactics/TA0011) |
| ------------------------------- | :--------------------------------------------: | :--------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :-------------------------------------------: | :------------------------------------------: | :-------------------------------------------: | :------------------------------------------: | :--------------------------------------------: | :-------------------------------------------: |
| Account Creation                |                       X                        |                                                |                       X                       |                       X                       |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| Account Logon                   |                       X                        |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                                              |                       X                       |                                              |                                                |                                               |
| Account Logon Time              |                       X                        |                                                |                       X                       |                       X                       |                       X                       |                                               |                                              |                       X                       |                                              |                                                |                                               |
| Account Modification            |                       X                        |                       X                        |                       X                       |                       X                       |                       X                       |                       X                       |                                              |                                               |                                              |                                                |                                               |
| Account Simultaneous Logons     |                       X                        |                                                |                       X                       |                       X                       |                       X                       |                                               |                                              |                       X                       |                                              |                                                |                                               |
| API Usage                       |                                                |                       X                        |                                               |                       X                       |                       X                       |                                               |                      X                       |                                               |                      X                       |                                                |                                               |
| Application Log                 |                       X                        |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| Bash Activity                   |                                                |                       X                        |                                               |                                               |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| Browser Extension               |                                                |                                                |                       X                       |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| Child Process Spawning          |                                                |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                                              |                       X                       |                                              |                                                |                                               |
| Command Activity                |                       X                        |                       X                        |                       X                       |                       X                       |                       X                       |                       X                       |                      X                       |                                               |                      X                       |                       X                        |                                               |
| Configuration Change            |                                                |                                                |                       X                       |                                               |                                               |                                               |                                              |                                               |                                              |                       X                        |                                               |
| DLL Loading                     |                                                |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                      X                       |                                               |                                              |                       X                        |                                               |
| Domain Replication Request      |                                                |                                                |                                               |                                               |                                               |                       X                       |                                              |                                               |                                              |                                                |                                               |
| Email Attachment                |                       X                        |                       X                        |                                               |                                               |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| Executable from Removable Media |                       X                        |                       X                        |                                               |                                               |                       X                       |                                               |                                              |                       X                       |                                              |                                                |                                               |
| File Access                     |                       X                        |                       X                        |                       X                       |                       X                       |                       X                       |                       X                       |                                              |                                               |                      X                       |                       X                        |                                               |
| File Contents                   |                       X                        |                       X                        |                       X                       |                                               |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| File Creation                   |                       X                        |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                                              |                                               |                                              |                       X                        |                                               |
| File Deletion                   |                       X                        |                                                |                       X                       |                       X                       |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| File Download Source            |                       X                        |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| File Hash                       |                       X                        |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| File Modification               |                       X                        |                                                |                       X                       |                       X                       |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| File Name                       |                                                |                       X                        |                                               |                                               |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| File Rename                     |                                                |                                                |                       X                       |                       X                       |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| File Signer                     |                                                |                       X                        |                                               |                                               |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| Firmware Modification           |                                                |                                                |                       X                       |                                               |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| GET Parameter (URL)             |                       X                        |                       X                        |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| MBR/VBR Modification            |                                                |                                                |                       X                       |                                               |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| Network Connection Length       |                                                |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                       X                        |                                               |
| Network File Transfer           |                                                |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                       X                        |                                               |
| Network Port Opening            |                       X                        |                                                |                       X                       |                       X                       |                                               |                                               |                                              |                       X                       |                                              |                                                |                                               |
| Network Port Use                |                                                |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| Network Protocol Behavior       |                                                |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                       X                        |                       X                       |
| Network Protocol Use            |                                                |                       X                        |                                               |                                               |                                               |                                               |                                              |                       X                       |                                              |                       X                        |                                               |
| Network Send/Receive Ratio      |                                                |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                       X                        |                       X                       |
| Network Socket                  |                       X                        |                                                |                       X                       |                       X                       |                                               |                       X                       |                                              |                       X                       |                                              |                                                |                                               |
| Network Traffic Interval        |                                                |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                       X                        |                                               |
| Network-Active Process          |                                                |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                       X                        |                       X                       |
| Network-Active System           |                       X                        |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| POST Parameter                  |                       X                        |                       X                        |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| PowerShell Activity             |                                                |                       X                        |                       X                       |                                               |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| Process Argument                |                                                |                       X                        |                       X                       |                       X                       |                       X                       |                       X                       |                                              |                                               |                      X                       |                                                |                                               |
| Process Execution               |                                                |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                      X                       |                       X                       |                                              |                       X                        |                                               |
| Process Hooking                 |                                                |                                                |                       X                       |                       X                       |                                               |                       X                       |                                              |                                               |                                              |                                                |                                               |
| Process Owner                   |                                                |                                                |                                               |                       X                       |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| Process Parent                  |                                                |                                                |                                               |                                               |                                               |                       X                       |                                              |                                               |                                              |                                                |                                               |
| Process Termination             |                                                |                       X                        |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| Registry Entry Access           |                                                |                                                |                                               |                                               |                                               |                       X                       |                      X                       |                                               |                                              |                                                |                                               |
| Registry Entry Creation         |                                                |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                      X                       |                                               |                                              |                                                |                                               |
| Registry Entry Deletion         |                                                |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| Registry Entry Modification     |                                                |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                      X                       |                                               |                                              |                                                |                                               |
| Scheduled Job/Task              |                                                |                       X                        |                       X                       |                       X                       |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| Script Execution                |                       X                        |                       X                        |                                               |                                               |                       X                       |                                               |                                              |                       X                       |                                              |                                                |                                               |
| Service Creation                |                                                |                       X                        |                       X                       |                                               |                       X                       |                                               |                                              |                       X                       |                                              |                                                |                                               |
| Service Modification            |                                                |                                                |                       X                       |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| SQL Command                     |                       X                        |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| System Access                   |                       X                        |                       X                        |                       X                       |                       X                       |                       X                       |                                               |                                              |                                               |                                              |                                                |                                               |
| URL Request                     |                       X                        |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| USB Device                      |                       X                        |                                                |                                               |                                               |                                               |                                               |                                              |                                               |                                              |                                                |                                               |
| WMI Activity                    |                                                |                                                |                       X                       |                                               |                                               |                                               |                                              |                                               |                      X                       |                                                |                                               |