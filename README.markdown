# Cyber Security Internship - Task 4: Firewall Configuration

## Overview
This repository documents the setup and testing of a firewall using UFW (Uncomplicated Firewall) on Kali Linux, as part of the Cyber Security Internship Task 4. The objective was to configure and test basic firewall rules to allow or block network traffic.

## Tools Used
- **UFW (Uncomplicated Firewall)** on Kali Linux

## Configuration Steps

### 1. Initial Setup
- **Action**: Checked the initial firewall status.
- **Command**: `sudo ufw status`
- **Result**: Firewall was inactive.

### 2. Firewall Activation
- **Action**: Enabled the firewall.
- **Command**: `sudo ufw enable`
- **Result**: Firewall activated successfully.

### 3. Rule Listing
- **Action**: Listed current firewall rules with numbering.
- **Command**: `sudo ufw status numbered`
- **Result**: Displayed existing rules for reference.

### 4. Rule Configuration
- **Action**: Added a rule to block inbound traffic on port 23 (Telnet).
- **Command**: `sudo ufw deny 23`
- **Result**: Rule applied successfully.
- **Action**: Added a rule to allow SSH traffic on port 22.
- **Command**: `sudo ufw allow 22`
- **Result**: Rule applied successfully.
  
### 5. Testing
- **Action**: Tested the block rule on port 23.
- **Method**: Attempted a Telnet connection.
- **Result**: Connection was blocked.
- **Action**: Tested the allow rule on port 22.
- **Method**: Established an SSH connection locally.
- **Result**: Connection successful.

### 6. Rule Cleanup
- **Action**: Removed the test block rule for port 23.
- **Command**: `sudo ufw delete 1`
- **Result**: Rule deleted, original state restored.

### 7. Final Verification
- **Action**: Checked the updated firewall status.
- **Command**: `sudo ufw status numbered`
- **Result**: Verified the updated rule set.


## Summary
The firewall effectively filters network traffic by enforcing rules to allow or deny access on specific ports. UFW simplifies firewall management with intuitive commands, enhancing security by controlling traffic and blocking unsecured services like Telnet (port 23) while permitting essential services like SSH (port 22).

## Key Takeaways
- Gained proficiency in firewall configuration and rule management using UFW.
- Understood the importance of securing unused ports (e.g., Telnet on port 23).
- Recognized the need to allow critical services (e.g., SSH on port 22) for operational continuity.

## Submission Details
- **Date**: June 27, 2025
- **Time**: 08:08 PM IST
