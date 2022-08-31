<h1>Configuring an SSH Server</h1>


<h2>Description</h2>
In this lab, I learned to configure an SSH server. SSH (secure shell) is a protocol for securely exchanging data between two computers over an untrusted network. It protects the privacy and integrity of the transferred identities, data, and files. It runs on most computers and practically every server.
<br />



<h2>Environments Used </h2>

- <b>Kali GNU/Linux Rolling</b> 
- <b>Terminal</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar click Terminal and type in command "service --status-all" : <br/>
<img src="https://i.postimg.cc/T19GnTxg/Screen-Shot-2022-08-30-at-7-52-49-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the Terminal window type in "apt-get install openssh-server" and verify that ssh is in the list. Also when prompted do you wish to continue type "y" then enter  <br/>
<img src="https://i.postimg.cc/bw8P3Drb/Screen-Shot-2022-08-30-at-7-55-09-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
  
<br />
In the terminal window execute the following commands <br/>
1. service ssh start <br/>
2. service ssh status <br/>
then use ctrl+c to exit <br/>
<img src="https://i.postimg.cc/6p8YDw30/Screen-Shot-2022-08-30-at-8-00-41-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the terminal window type in the following commands: <br/>
1. cd /etc/ssh <br/>
2. ls <br/>
3. nano sshd_config <br/>
Then find Port 22 and type the next line as Port 1986 <br/>
<img src="https://i.postimg.cc/zvZPSf1v/Screen-Shot-2022-08-30-at-8-05-35-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the sshd_config editor press ctrl+x then type y and press enter to to save configuration file.  <br/>
<img src="https://i.postimg.cc/y871VVtF/Screen-Shot-2022-08-30-at-8-06-51-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />





<br />
In the terminal window type service ssh restart.  <br/>
<img src="https://i.postimg.cc/GhyW6Zpv/Screen-Shot-2022-08-30-at-8-09-36-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the terminal type in the "ssh-keygen -t rsa" command then press enter three times <br/>
<img src="https://i.postimg.cc/Nft0J7sG/Screen-Shot-2022-08-30-at-8-11-30-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />




<br />
In the terminal window type command "service ssh status" then press ctrl+c to to exit.  <br/>
<img src="https://i.postimg.cc/tgLb1P2V/Screen-Shot-2022-08-30-at-8-14-14-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />






<br />
In the terminal window type command "sudo grep Port /etc/ssh/sshd_config" to verify ssh is using port 1986.  <br/>
<img src="https://i.postimg.cc/tTYzcnjD/Screen-Shot-2022-08-30-at-8-17-14-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
















  
  
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
