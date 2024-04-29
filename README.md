# Active Directory Lab

## Objective
Creating and utilizing an Active Directory (AD) lab for simulating MITRE attack techniques involves setting up a controlled environment to mimic a real-world network infrastructure. In this lab, administrators can deploy various Windows servers and workstations configured with Active Directory services. Kali was using to genetrate any MITRE technique by using the crowbar tool and Splunk server was used to show attacks on the environment. By combining Kali Linux for attack simulation and Splunk for security monitoring, administrators and security professionals can effectively detect, analyze, and respond to simulated attacks within the Active Directory lab environment.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Splunk Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Crowbar Attack tool for brute force domain user accounts.
- Atomic Red Team to generate MITRE attack techniques. 

## Steps
# Below we are installing atomic red team on a windows 10 client machine.

<img src="https://github.com/Rapheal93/Active-Directory-Lab/assets/37610656/a1969e9c-8cd6-484f-86b8-6806b67e7a76" />

# Next, We are going to simulate the MITRE attack technique, create account, local account on T1136.001 as shown in the screenshot below.

<img src="https://github.com/Rapheal93/Active-Directory-Lab/assets/37610656/7ea31573-190f-48cb-9f1e-af277a2c1f7d" />

# We execute the technique using the syntax on powershell.

<img src="https://github.com/Rapheal93/Active-Directory-Lab/assets/37610656/7f51b976-3990-4b50-9044-e5474f72a20a" />

# Here, after we run the technique, we see that the user "NewLocalUser" was created.

<img src="https://github.com/Rapheal93/Active-Directory-Lab/assets/37610656/1cc3bcb0-7446-413e-ab9d-33d4b742f5e3" />

# we can confirm our attack was detected by our Splunk machine by editing our search to include event_id = 4720. Which looks for user account creations in the logs.

<img src="https://github.com/Rapheal93/Active-Directory-Lab/assets/37610656/89d2a930-a327-42c2-853c-66b981810504" />
