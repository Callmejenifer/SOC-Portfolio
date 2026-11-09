# TryHackMe: Systems as Attack Vectors

**Path:** SOC Level 1
**Platform:** TryHackMe
**Status:** Completed

## Overview
These rooms cover how attackers exploit software flaws and misconfigured systems, and how a SOC analyst responds. The practice room had me review systems at risk and build a remediation plan.

## Key concepts
- Every piece of software has flaws, and some stay hidden for years. Shellshock, a Linux flaw, existed from 1992 until 2014.
- A zero-day is a flaw attackers find before anyone else, so no patch exists yet.
- Public flaws get a CVE number: CVE, the year, then a unique number.
- The response to a CVE is a patch from the vendor. While waiting for one, restrict access to trusted IPs, monitor for exploitation, and apply the vendor's temporary measures.
- Room question: the critical SharePoint flaw "ToolShell" is CVE-2025-53770. The room text didn't state it, so I searched the nickname plus "CVE" and confirmed it with official sources (CISA, MITRE).

## Practice room: cases I handled
1. **Exchange server, CVE-2024-49040:** I chose to patch and update Exchange. A patch fixes the real flaw. Restricting access is only temporary, and changing passwords doesn't close the hole.
2. **WordPress site defaced after an admin brute force:** I chose to change the admin password. Restoring a backup alone lets the attacker return through the same weak password.
3. **Warning about a neighbour's ransomware via an old Cisco firewall:** I chose to patch and audit all firewalls. The brand wasn't the problem, outdated software was. Disabling firewalls during an audit would leave the network open.
4. **Trusted 3D app running malicious commands after an update:** I chose to investigate a supply chain attack, because the behaviour started right after the update. Blaming the user is never the first step.

## Remediation plan I approved
- Patch management policy
- Secure password policy for admin and service accounts
- Security training for IT staff on misconfiguration
- Antivirus protection on critical systems

I rejected blocking the public website (it breaks the business), a shared account (no accountability), and random server names (security through obscurity).

## What I learned
- Fix the cause, not just the symptom.
- A patch answers a known CVE. Restrict access and monitor when no patch exists.
- After a warning about someone else's breach, audit and patch my own devices.
- Never switch off security tools during an audit.
- Research unfamiliar threats using trusted sources and confirm with more than one.

