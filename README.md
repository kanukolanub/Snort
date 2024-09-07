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

**Read the "snort.log.1640048004" file with Snort; what is the Ack number of the 8th packet?**
**Answer is 0x38AFFFF3**
![image](https://github.com/user-attachments/assets/9a33c026-c50a-4861-8d33-ef239a53d297)

![image](https://github.com/user-attachments/assets/f2c73d2a-20aa-4c14-b736-3588439bd17c)

**Read the "snort.log.1640048004" file with Snort; what is the number of the "TCP port 80" packets?**
**Answer is 41**
![image](https://github.com/user-attachments/assets/e0764d77-28c9-4b61-9b67-67d92a334e04)

![image](https://github.com/user-attachments/assets/882f17a3-2e8f-4e65-8479-8b708f5c02cf)

**4. Snort in IDS/IPS Mode**
![image](https://github.com/user-attachments/assets/a58093c5-5313-4a78-aea1-e9e47b2f22ee)

**Investigate the traffic with the default configuration file.**
**sudo snort -c /etc/snort/snort.conf -A full -l .**

**Execute the traffic generator script and choose "TASK-7 Exercise". Wait until the traffic stops, then stop the Snort instance. Now analyse the output summary and answer the question.**
**sudo ./traffic-generator.sh**

**What is the number of the detected HTTP GET methods?**

![image](https://github.com/user-attachments/assets/97c87f36-fd1f-44de-9028-4c5f1efca6f6)
**Answer is 2**
![image](https://github.com/user-attachments/assets/1ba33f63-743b-479b-ad4b-5b34be3d4ada)

![image](https://github.com/user-attachments/assets/6ad3f7ad-540d-4eb0-bee9-5e36186b2fc4)

![image](https://github.com/user-attachments/assets/2f8dc26c-9f6b-4160-8b22-1d24b6fa38dd)

**5. Investigating PCAPs with Snort**

![image](https://github.com/user-attachments/assets/012337aa-4240-41db-9c4d-697ef843f5ed)

**Investigate the mx-1.pcap file with the default configuration file.
sudo snort -c /etc/snort/snort.conf -A full -l . -r mx-1.pcap
What is the number of the generated alerts?** **Answer is 170**

![image](https://github.com/user-attachments/assets/2882fa82-dfd5-4ea9-86a3-c837dfd92948)

![image](https://github.com/user-attachments/assets/8993aed1-8afe-4f31-8a24-a212277d920d)

![image](https://github.com/user-attachments/assets/910962e3-3982-466c-80c3-616967b02564)

**Keep reading the output. How many TCP Segments are Queued?** **Answer is 18**
**Keep reading the output.How many "HTTP response headers" were extracted?** **Answer is 3**

![image](https://github.com/user-attachments/assets/27447682-61d4-4769-a677-20e5966a9061)

**Investigate the mx-1.pcap file with the second configuration file.
sudo snort -c /etc/snort/snortv2.conf -A full -l . -r mx-1.pcap
What is the number of the generated alerts?** **Answer is 68**

![image](https://github.com/user-attachments/assets/8adbfcf7-f953-4272-94a7-5d145859c291)

![image](https://github.com/user-attachments/assets/3b93b52d-753e-4d15-b84d-129db8cee6f7)

**Investigate the mx-2.pcap file with the default configuration file.
sudo snort -c /etc/snort/snort.conf -A full -l . -r mx-2.pcap**
**Keep reading the output. What is the number of the detected TCP packets?** **Answer is 82**

**![image](https://github.com/user-attachments/assets/89e838c2-5d0f-4cf2-a9c9-d74eaac4b832)
Investigate the mx-2.pcap and mx-3.pcap files with the default configuration file.
sudo snort -c /etc/snort/snort.conf -A full -l . --pcap-list="mx-2.pcap mx-3.pcap"**
**What is the number of the generated alerts?** **Answer is 1020**

![image](https://github.com/user-attachments/assets/8a87eb09-7d12-464d-81f9-29c20081dda2)

![image](https://github.com/user-attachments/assets/9e83999b-fac7-4ed5-a0b0-04f072725b5e)

