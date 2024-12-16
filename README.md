# Windows Network Analysis

<h2>Description</h2>
In this task, I used windows cmd tools like net view, net session, net use, netstat, and tcpview to analyze running processes on my windows vm.    


<h2>Languages and Utilities Used</h2>

- <b>Windows cmd</b>
- <b>linux CLI</b>


<h2>Environments Used </h2>

- <b>Unbuntu</b>
- <b>Windows 10 Enterprise</b> 

<br />
<br />
On Ubuntu, create an exmaple folder called Exfil and used netshare to set the path on windows to share it on my windows vm. 

![1) net share](https://github.com/user-attachments/assets/5626124d-97f2-4f38-b4ac-1ff88172e05f)

<br />
<br />
Running net view shows the Exfil file being shared on disk. Running net share shows the path to the file share. 

![2) net share successful](https://github.com/user-attachments/assets/c4de2121-3743-4d60-92cd-4495a6619473)

<br />
<br />  
Using net use to map the X: drive to the Exfil folder on the local machine 127.0.0.1

![3) creating session as attacker in X drive](https://github.com/user-attachments/assets/fee92feb-08ee-4f32-8d98-684126b59a26)

<br />
<br />
Using net session shows the connected system on the windows vm. Net use shows which systems our windows vm is communicating outbound with. 

![4) net sessions net use ](https://github.com/user-attachments/assets/51394995-beaa-4bd2-9642-eab3d00dfa1a)

<br />
<br />
Running netstat -anob shows the notmalware tcp connection.

![5) netstat -anob shows active connections of notmalware to attacker](https://github.com/user-attachments/assets/ef34a4d4-2907-4fba-9894-ce48bc885046)

<br />
<br />
Similarly, using tcpview will also show the notmalware tcp connection. 

![6) tcpview sysinternals](https://github.com/user-attachments/assets/e7ca885f-a921-46a9-8295-caeed9b214d6)

<br />
<br />
