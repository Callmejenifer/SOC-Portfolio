# TryHackMe: Humans as Attack Vectors

**Path:** SOC Level 1
**Platform:** TryHackMe
**Status:** Completed

## Overview
This room covers how attackers target people instead of systems, and how a SOC analyst protects employees. It had an introduction, the human element, attacks on humans, defending humans, and a hands-on practice room where I acted as a SOC analyst.

## Practice room: cases I investigated
1. **Blocked installer:** A new engineer's setup file from an untrusted site was blocked by antivirus six times. I quarantined the file and pointed him to the official 7-Zip installer instead of excluding the file from antivirus.
2. **Fake Stripe invoice:** An email to the finance director claimed a $23,650,000 payment, came from a look-alike domain (stripe-payments.xyz), and had a password-protected RAR attachment. I blocked the email and started an analysis, because it was phishing.
3. **Deepfake CEO call:** IT support reset the CEO's password after a 9 p.m. call from a hidden number, and the CEO could not be reached. I disabled the account until he confirmed. It was a deepfake voice call.
4. **Anomalous login:** An HR assistant logged in from London instead of her usual Oxford. The location was a distraction. The real clue was a fake Microsoft 365 login page (.ru domain) visited just before. I disabled her account.

## Security policy review
I approved four measures to protect employees from future attacks:
- Security awareness program (quarterly phishing training)
- Access management policy (how IT verifies password resets and access requests)
- Antivirus solution on all workstations
- Anti-phishing solution to block malicious emails

## What I learned
- Attackers target people because humans are often the easiest way in.
- Check the sender's domain, the attachment type, and any urgency or pressure in a message.
- Never exclude a blocked file from antivirus just to make it run. Point users to official sources.
- Look at the URLs visited before a suspicious login, not just the location.
- A familiar voice is not proof of identity. Verify through a second, trusted channel before resetting credentials.
- Good policy combines training, verification procedures, and technical protection.
