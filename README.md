# Auditd-Configurations
AUDITING SYSTEM INFO
	• Kernel space audit
	• User space audit daemon (auditd)-> write the logs which comes from kernel in message and its config(auditd.conf), auditctl : its a tools to query logs, the other tools (aureport,audispd,ausearch)
	• The rules:
	• 1 auditing control
	• 2 file system
	• 3 system calls
	• We can intercat with those rules using auditctl
	• Files monitors 
	• The audit system (monitor and tracks any changes)

AUDITING SYSTEM RULES
At level of file system: in case of changing of permissions or file we will get logs
auditctl -w /home/vagrant/file1.txt -p wa -k [any name]
W : watch, -p : permisssion, -k: key to understand
We will find the changing in audit.log
Get rules auditctl -l

Rule 2: auditing control: contrôle the audit systemctl itself auditctl -s
Auditctl -e0 -> e: enable and so on: value 0 to 2
![image](https://user-images.githubusercontent.com/112700922/211508777-813ee05e-0944-4c9b-ac51-a282c6daa58c.png)
