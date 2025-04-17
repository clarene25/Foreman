<h1>Foreman</h1>

 
<h2>Description</h2>
Foreman is a complete lifecycle management tool for physical and virtual servers. We give system administrators the power to easily automate repetitive tasks, quickly deploy applications, and proactively manage servers, on-premise or in the cloud. <br />

<br />


<h2>Languages and Utilities Used</h2>

- <b>Foreman</b> 


<h2>Environments Used </h2>

- <b>Centos 7  </b>

<h2>Tooling Walkthrough:</h2>

<p align="center">
Steps to add your server to Foreman
<br />
<br />
   <p align="left">
1. SSH into your server and perform the following steps<br />
 <br />
- add foreman server DNS name to your client machine (path--- /etc/hosts file)<br />
- install the Subscription Manager --on client machine<br />
 yum -y install subscription-manager<br />
- install the Agent certificate from the Foreman Server<br />
 curl --insecure --output katello-ca-consumer-latest.noarch.rpm "http link for foreman site" <br />
 - yum localinstall katello-ca-consumer-latest.noarch.rpm<br />
 - subscribe to the Foreman Organization<br />
 subscription-manager register --org="Procore" --activationkey="ProcoreKey"<br />
<br />
2.  Create Repo and Install the Katello Agent<br />
    



3. Start and enable mariadb server<br />


 4. Configuring MariaDB<br />

