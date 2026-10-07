# Windows Security Monitoring Lab

## Overview

This project demonstrates hands-on Windows security monitoring and SOC investigation techniques using a Windows 11 virtual machine.

The lab focuses on identifying, analyzing, and documenting Windows authentication events using Windows Event Viewer and Windows Security logs.

## Lab Environment

- Windows 11 Pro
- UTM Virtual Machine
- Apple Silicon host
- Windows Event Viewer
- Windows Security Logs
- PowerShell
- Test workstation: SOC-WIN11-LAB

## Project Objectives

- Analyze Windows Security Event Logs
- Investigate failed authentication attempts
- Understand common Windows Event IDs
- Interpret Windows status and substatus codes
- Practice SOC alert triage
- Document security investigations
- Build practical cybersecurity experience

## Investigation 01 — Failed Windows Logon

A controlled failed authentication attempt was generated against a local Windows test account.

Windows recorded:

**Event ID 4625 — An account failed to log on**

### Key Findings

| Field | Value |
|---|---|
| Event ID | 4625 |
| Target User | LabUser |
| Target Domain | SOC-WIN11-LAB |
| Status | 0xC000006D |
| SubStatus | 0xC000006A |
| Logon Type | 2 |

The investigation determined that the account was valid but an incorrect password was supplied.

### Evidence

![Windows Event 4625](screenshots/01-event-4625-failed-logon.png)

### Full Investigation

[View the complete Event ID 4625 investigation](incident-reports/failed-logon-investigation.md)

## Skills Demonstrated

- Windows Event Log Analysis
- Authentication Analysis
- SOC Alert Triage
- Event ID Investigation
- Windows Security Monitoring
- PowerShell
- Incident Documentation

## Future Lab Development

This lab will be expanded to include:

- Multiple failed-login detection
- Successful logon analysis
- Account creation monitoring
- Privilege escalation events
- PowerShell activity monitoring
- Sysmon
- SIEM log ingestion
- Detection rules
- Incident response investigations

## Disclaimer

All activity in this repository was generated in a controlled lab environment for cybersecurity education and defensive security training.
