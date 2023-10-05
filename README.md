# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
## PROGRAM:
Find out the ip address of the attackers system
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/c84932dc-ec7d-46a9-af78-53c3b5e97641)
## invoke msfconsole:
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/87e3d56a-c1a5-473d-bd70-74ed47433dab)
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

## OUTPUT:
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/e8c47689-4ca1-4587-a7e3-1578d9dcfc3d)
Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000




## OUTPUT:
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/2f190985-55e4-4b70-bcc2-51d2d1f6989f)
Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l
## OUTPUT:
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/db7f4a3e-5e5d-4a6b-b654-c00e5366003c)
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/75bc767b-c9af-4097-85f9-113dffe3dffc)
Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit.
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/7ac3c90b-132c-4541-8590-9a522cdf2936)
The info command provides information regarding a module or platform.

## OUTPUT:
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/e612ced4-ad5e-4330-b6c4-920c9280914d)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>.
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/c04a2d00-dd54-4a6b-9f8f-bcc70a4050eb)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql.
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/25863210-c834-49e4-99cc-333c3fdd3b9a)
Use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version.
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/86bc1a62-247e-473c-8ebc-8001eef4e53c)
After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/6d5415e6-7c1a-422b-88e0-02c09099ed96)

set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true.

![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Metasploit-for-reconnaissance/assets/119644432/56ff9388-e9f5-4212-bde6-9f4cc4659e8d)









## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
