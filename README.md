# IT-Helpdesk-Ticketing-Lab

## Overview
Simulated IT help desk environment for practicing ticket management, Windows troubleshooting, incident documentation, and technical support workflows.

The lab is being built as a hands-on learning project to develop practical skills relevant to entry-level IT support and service desk roles.

## Objectives

- Practice managing and documenting IT support tickets
- Develop a consistent troubleshooting methodology
- Practice identifying symptoms, root causes, and resolutions
- Document technical issues clearly for future reference
- Gain hands-on experience with a help desk ticketing platform
- Simulate common Tier 1 IT support scenarios
- Practice communication technical solutions clearly

## Lab Environment

- Oracle VirtualBox
- Ubuntu GLPI Server
- Windows 10 client and Technician virtual machine
- GLPI ticketing system

## Infrastructure Build Log
### Challenge 1
#### The Problem
#### The Diagnostic Process
#### The Solution
#### Engineering Takeaways


## Planned Support Scenarios

- Windows login problems
- Account issues
- Software problems
- Printer problems
- Network connectivity issues
- Hardware/device issues
- New user onboarding
- Access and permission issues

## Projects Status

*In Progress* 

The lab is currently being built.
Additional documentation, troubleshooting scenarios, and ticket examples will be added as the environment develops.

## Ticket Logs and Troubleshooting

### Ticket 001
#### Issue Description 
Hardware degradation; user reports physical swelling of the chassis around the trackpad and keyboard array, accompanied by thermal spikes.

#### Root Cause Analysis
Internal Lithium-ion polymer battery failure resulting in cell outgassing and volumetric expansion (swollen battery), presenting a severe thermal and physical hazard.

#### Resolution Steps
1. Instructed user to safely power down the machine immediately and disconnect the AC adapter.
2. Recovered the physical asset using safety gear and isolated it in a fire-retardant charging bag.
3. Extracted the degraded battery cell following proper electronic waste guidelines.
4. Installed a certified OEM replacement battery, reassembled the chassis, and verified normal charging cycles.

#### Knowledge Base & Preventive Action 
KB Article: Handling Swollen Lithium-Ion Batteries Safely.
Implemented a hardware lifecyle rule in GLPI to flag and proactively replace laptop models exceeding 48 months of active deployment to prevent cyclic degradation.

### Ticket 002
#### Issue Description
Potential security incident; user clicked an unverified external hyperlink and inputted corporate credentials into a malicious spoofed landing page.

#### Root Cause Analysis
Successful external credential phishing attack targeting end-user vulnerability via identity spoofing (fake courier notification).

#### Resolution Steps
1. Isolated the user's host endpoint from the local network segment via the network switch management console.
2. Forced a global password reset and revoked all active authentication sessions/tokens in Entra ID (Active Directory).
3. Audited account sign-in logs for anomalous IP addresses or unexpected geographic access tokens.
4. Cleared browser cache and cookies on the target machine and verified endpoint security tools showed no active malicious payloads

#### Knowledge Base & Preventive Action
KB Article: Reporting Suspected Phishing Attempts via Outlook.
Escalated domain data to the security operations team to update the network firewall's global URL blocklist.
