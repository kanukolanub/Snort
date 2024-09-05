# Snort

## Overview
SNORT is an open-source, rule-based Network Intrusion Detection and Prevention System (NIDS/NIPS).
* Snort is the foremost Open Source Intrusion Prevention System (IPS) in the world. 
* Snort IPS uses a series of rules that help define malicious network activity and uses those rules to find packets that match against them and generate alerts for users.

This repository contains a project on how to use snort in Sniffer, Packet Logger, IDS/IPS Modes: 

**1. Run the Snort instance and check the build number.**

![image](https://github.com/user-attachments/assets/42ca249d-58b1-49a8-8888-cd1cbf1095ea)

**2. Run Snort in Sniffer Mode**

Sniffer mode parameters are mentioned in the table below
In a new terminal run the following command to generate incoming traffic
ubuntu@ip-10-10-39-8:~/Desktop/Task-Exercises$ sudo ./traffic-generator.sh

And in a separate terminal run the commands using individual sniffer mode parameters. 

![image](https://github.com/user-attachments/assets/aa7f2600-31bf-40f5-9365-1d457e6c13e9)

![image](https://github.com/user-attachments/assets/fce04ab0-596d-46f4-b5e1-d651d8aee184)

![image](https://github.com/user-attachments/assets/3731ebbe-c674-4538-917d-7e3263568125)

![image](https://github.com/user-attachments/assets/a224bc8e-11d7-43da-9335-5b732bf958d5)

![image](https://github.com/user-attachments/assets/202b53ae-bdf9-4558-9537-260e8385a666)

**3. Run Snort in Logger Mode**

logger mode parameters are mentioned in the table below

![image](https://github.com/user-attachments/assets/0fe1da57-4729-4ea9-9476-83e88f04c34e)

Investigate the traffic with the default configuration file with ASCII mode.

sudo snort -dev -K ASCII -l .

Execute the traffic generator script and choose "TASK-6 Exercise". Wait until the traffic ends, then stop the Snort instance. Now analyse the output summary and answer the question.
sudo ./traffic-generator.sh

Now, you should have the logs in the current directory. Navigate to folder "145.254.160.237". 
**What is the source port used to connect port 53? Answer is UDP 3009**

![image](https://github.com/user-attachments/assets/00c4271f-e6b8-4a93-9ba4-c21250cc7ed1)

![image](https://github.com/user-attachments/assets/76019415-fea2-4b5f-bd0a-44dc990e6617)

![image](https://github.com/user-attachments/assets/5653e30b-0ee6-411a-96da-bfbf45993cc2)

**Use snort.log.1640048004 Read the snort.log file with Snort; what is the IP ID of the 10th packet?**
**Answer is ID 49313**

![image](https://github.com/user-attachments/assets/1d71122a-732f-4ac2-b295-5e11f398f212)

![image](https://github.com/user-attachments/assets/a8db1673-e9b6-4051-bba2-47d86c690bc2)

**Read the "snort.log.1640048004" file with Snort; what is the referer of the 4th packet?**
**Answer is www.ethereal.com/development.html**
![image](https://github.com/user-attachments/assets/65e8d0de-1026-4ca5-a8d2-98b98b5156d2)

![image](https://github.com/user-attachments/assets/47e57055-5a17-4714-bf3b-4b7f6e7bed4a)

