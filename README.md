# Active Directory Home Lab Setup

Welcome to the Active Directory Home Lab Setup repository. This lab will walk you through how I created an Active Directory lab environment on your labtop using oracle virtual machine and powershell for learning and testing.

## Table of Contents
1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Lab Setup](#lab-setup)
4. [User Management]
5. [Usage](#usage)

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
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/ae36f5c8-bafb-4145-8c4c-06bebf6ba53e" width="300" alt="screenshot">


### Step 2: Run the Installation Script
- Execute the installation script to set up your Active Directory environment.cd Active-.\install.ps1
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/af822b2d-378f-40f9-bb79-fc8259d941e4" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/798dcc56-8418-4512-ad7e-1237aafb824d" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/bee6ab3a-4486-40b6-9d19-f929fcb47927" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/f3dad438-3551-4a1c-82a5-0b46d3b488d1" width="300" alt="screenshot">


### Step 3: Access Active Directory Users and Computers
- Launch the "Active Directory Users and Computers" console to start managing your Active Directory.Active-.\install.ps1
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/f3e07b04-4c55-44e0-91ec-0ca3a5df28b5" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/080207d6-5e4a-4ad6-a541-ac17e51181d0" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/1f59ce3c-7b5d-4429-92f8-742f11924da0" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/d304f837-cb6b-4f9f-9f30-9f19c700ccc5" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/b3796a64-e8a8-4fe1-b771-353f0f9ec984" width="300" alt="screenshot">


## Configuration
### Domain Creation
- Open Powershell as an administrator
- Run the following Powershell script to create a new domain:
- .\Create-NewDomain.ps1 -DomainName "yourdomain.com" -NetBiosName "YourDomain"
- Replace "yourdomain.com" with your desired domain name and "YourDomain" with your NetBIOS name.
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/c943a3b1-ce6a-4b0f-8bde-b9c533304c9c" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/39756b0a-64e7-42f6-978b-7445ec02062f" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/00a89989-a0d4-4aa6-a859-96bacf42f00d" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/d83a20dd-ffcf-42b7-89cc-b6df6cf348fd" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/2f418365-d167-447d-8275-f127bd0519f5" width="300" alt="screenshot">


## User Management
- Create a new user
New-ADUser -Name "John Smith" -SamAccountName "jsmith" -UserPrincipalName "jsmith@yourdomain.com" -Enabled $true

- Reset user's password
Set-ADAccountPassword -Identity "jsmith" -Reset -NewPassword (ConvertTo-SecureString -AsPlainText "newpassword" -Force)

- Disable a user
Disable-ADAccount -Identity "jsmith"
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/4aa6f308-ac17-4f08-9d45-3067d64699c9" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/395d9408-d46c-4bc7-9c92-34ab1c8a2aee" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/dea0069f-ce67-4885-a22a-ba2b935f2ecb" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/611197d4-6360-47de-a216-82a17c2724ca" width="300" alt="screenshot">
<img src="https://github.com/ElizabethEtsegbe/Active-Directory-Home-Lab/assets/148573965/9223b30b-1d0b-493e-8f41-d052c7d87011" width="300" alt="screenshot">


### Usage
You can use this Active Directory Home Lab to practice various tasks, such as:

- Creating and managing organizational units.
- Configuring Group Policy Objects (GPOs).
- Testing PowerShell scripts for Active Directory management.


