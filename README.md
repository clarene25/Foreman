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
Steps to install and configure an apache server
<br />
<br />
   <p align="left">
1. Set up the repository for Maria DB Project<br />
  
  - vi /etc/yum.repos.d/MariaDB.repo (and copy below contents in file)<br />
    <br />
[mariadb] <br />
name=MariaDB-10.7.8<br />
baseurl=http://archive.mariadb.org/mariadb-10.7.8/yum/centos/$releasever/$basearch<br />
gpgkey=https://archive.mariadb.org/PublicKey<br />
gpgcheck=1<br />

2. Install mariadb Server and msql client<br />

- yum install MariaDB-server MariaDB-client<br />

3. Start and enable mariadb server<br />
- systemctl enable mariadb -y<br />
- systemctl start mariadb<br />
- systemctl status mariadb<br />

 4. Configuring MariaDB<br />
- run the mysql_secure_installation script which will perform several security related tasks:<br />
mariadb-secure-installation<br />
- test by connecting mysql client with mariadb server<br />
- mysql -u root -p
