# Active Directory Home Lab Setup

Welcome to the Active Directory Home Lab Setup repository. This lab will walk you through how I created an Active Directory lab environment on your local machine for learning and testing.

## Table of Contents
1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Lab Setup](#lab-setup)
4. [Usage](#usage)

## Introduction
In this lab, I learnt how to set up a local Active Directory (AD) environment for educational purposes. Active Directory is a critical component of Windows network management.

## Prerequisites
Before I began, I made sure I had the following in place:
- A Windows-based computer (Windows 10 or later).
- Administrative privileges on my Windows machine.
- Internet access to download necessary resources.
- Sufficient system resources (CPU, RAM, and storage).

## Lab Setup

### Step 1: Navigate to the Lab Directory
- Change your current directory to the lab's directory.
cd Active-Directory-Home-Lab

### Step 2: Run the Installation Script
- Execute the installation script to set up your Active Directory environment.cd Active-.\install.ps1

### Step 3: Access Active Directory Users and Computers
- Launch the "Active Directory Users and Computers" console to start managing your Active Directory.Active-.\install.ps1

## Configuration
### Domain Creation
- Open Powershell as an administrator
- Run the following Powershell script to create a new domain:
- .\Create-NewDomain.ps1 -DomainName "yourdomain.com" -NetBiosName "YourDomain"
- Replace "yourdomain.com" with your desired domain name and "YourDomain" with your NetBIOS name.

Create Domain

## User Management
- Create a new user
New-ADUser -Name "John Smith" -SamAccountName "jsmith" -UserPrincipalName "jsmith@yourdomain.com" -Enabled $true

- Reset user's password
Set-ADAccountPassword -Identity "jsmith" -Reset -NewPassword (ConvertTo-SecureString -AsPlainText "newpassword" -Force)

- Disable a user
Disable-ADAccount -Identity "jsmith"

User Management

### Usage
You can use this Active Directory Home Lab to practice various tasks, such as:

- Creating and managing organizational units.
- Configuring Group Policy Objects (GPOs).
- Testing PowerShell scripts for Active Directory management.


