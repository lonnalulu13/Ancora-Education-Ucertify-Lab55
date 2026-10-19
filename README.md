# Ancora-Education-Ucertify-Lab55
# Testing the Security of Accounts

> **Original Lab Source**
> 
> This lab was available through:
>
> [https://ancoraeducation.ucertify.com/app/?func=navigate_items&item_sequence=8]

## Objective of the Lab
In this lab, you will learn to test the security of accounts. Here in this lab, you will test the security of accounts by creating five user accounts with different passwords for each account. Then, run the Johnny password attack tool on these new accounts and see which passwords were compromised by the tool. 
## Instructions 
### Caution 
* You will not be able to see the password being typed in.
* Retype the password whenever asked.
### STEP 1 
On the left sidebar, click the Terminal icon to open the Terminal window. 
### STEP 2 
Execute the following commands to create five accounts and assign each account a password (Note: Enter one command at a time):
```bash
useradd -d /home/test1 -m test1
```
```bash
useradd -d /home/test2 -m test2
```
```bash
useradd -d /home/test3 -m test3
```
```bash
useradd -d /home/test4 -m test4
```
```bash
useradd -d /home/test5 -m test5
```
### STEP 3
Execute the following command to create the password and enter Password as uc1, when prompted and retype the password:
```bash
passwd test1
```
### STEP 4
Execute the following command to create the password and enter Password as (uc2), when prompted:
```bash
passwd test2
```
### STEP 5
Execute the following command to create the password and enter Password as uc3, when prompted:
```bash
passwd test3
```
### STEP 6
Execute the following command to create the password and enter Password as uc4, when prompted:
```bash
passwd test4
```
### STEP 7
Execute the following command to create the password and enter Password as (uc5), when prompted:
```bash
passwd test5
```
### STEP 8
Execute the following command to create a file that combines the /etc/passwd and /etc/shadow files:
```bash
cat /etc/passwd /etc/shadow > /root/johnny_file
```
### STEP 9
Execute the following command to create a file:
```bash
nano password.lst
```
### STEP 10
Add the following in the file and press CTRL+X, type (y), and then press the Enter key to save the changes:
```bash
uc1
uc2
uc3
uc4
uc5
```
### STEP 11
On the desktop, navigate to Applications > 05 - Password Attacks > johnny, to start the johnny program. 
### STEP 12 
Navigate to Open password file > Open password file (PASSWD format) and open johnny_file.
### STEP 13
From the left sidebar, go to Options, under Attack mode, click Wordlist and click Browse for the Wordlist file, and then go to root > password.lst.
### STEP 14
From the menu bar, click Start new attack. 
### STEP 15 
From the left sidebar, go to Passwords to view the cracked password in the Password column. 
### STEP 16
From the right-top corner, check Show only cracked.
### STEP 17 
Select all the cracked passwords and from the menu, go to Export > Export to CSV. 
### STEP 18 
At the Save file dialog box, in the Name box, type (cracked) and click Save.

## Disclaimer

This repository is for **educational and personal learning purposes only**.  

The original lab content belongs to **uCertify / Ancora Education** and remains their copyrighted material.  
This repository is not affiliated with, endorsed by, or sponsored by uCertify or Ancora Education.  

No copyright infringement is intended.  
Use of any tools or techniques mentioned here should only be performed in authorized, legal environments.
