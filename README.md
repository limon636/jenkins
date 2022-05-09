> #### Installing Jenkins!
>
> - `wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -`
> - `sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`
> - `sudo apt update`
> - `sudo apt install jenkins`
>
>  *Everything* is going according to **plan**.

> #### Start Jenkins
> - `sudo systemctl start jenkins`
> - `sudo systemctl status jenkins`



> #### Opening the Firewall
> - `sudo ufw allow 8080`
> - `sudo ufw status`
*[If the firewall is inactive, the following commands will allow OpenSSH and enable the firewall]*
> - `sudo ufw allow OpenSSH`
> - `sudo ufw enable`


> #### Install plugins
> - Gitlab
> - Maven
> - NodeJS
> - OpenJDK
> - Publish over SSH


> #### Global configuration
> - Add JDK   
>  `– name: open-jdk8`    
>  `– JAVA_HOME: /usr/lib/jvm/java-8-openjdk-amd64`   
>   
> - Add Maven   
>  `name: M2_HOME`    
> `– MAVEN_HOME: /opt/maven`    
>    
> - Add Node    
> `– name: node`    
> `– install automatically` (version: 10.16.0)


> #### Configure System    
> Copy id_rsa and all of .ssh/ files into another directory (ex: home/limon/keygen/id_rsa)    
> - `ssh-keygen`
> -- Location of id_rsa  home/limon/keygen/id_rsa    
> ![jenkins-add-ssh-key](https://user-images.githubusercontent.com/45899698/167341122-648e7b35-0d2e-4785-b290-23ae1e34e014.png)

