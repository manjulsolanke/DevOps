## Jenkins Installation on Ubuntu

1) Update the package index:

`sudo apt update`

2) Add the Jenkins package repository to the system's package manager:

```bash

wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo add-apt-repository "deb https://pkg.jenkins.io/debian-stable binary/"

```

3) Install Jenkins:

`sudo apt install jenkins`

4) Start the Jenkins service:

`sudo systemctl start jenkins`

5) Enable the Jenkins service to start automatically at boot time:

`sudo systemctl enable jenkins`

6) Check the status of the Jenkins service:

`sudo systemctl status jenkins`

7) Open your web browser and navigate to `http://your-server-ip:8080`

8) After the initial installation, you will be prompted to enter the initial admin password which can be found in the following location:

`sudo cat /var/lib/jenkins/secrets/initialAdminPassword`

9) Follow the prompts to complete the setup process, including installing any necessary plugins.

10) Once the initial setup is completed you can customize your Jenkins as per your requirement.

Keep in mind that these steps are for a basic installation of Jenkins on Ubuntu 22. You can also check the official Jenkins website for more detailed instructions, as well as for other platforms.
