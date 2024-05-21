# Jenkins_installation_Amazon_Linux

## Step 1: SSH Into Your Instance

``` ssh -i <your_key>.pem ec2-user@<your_amazon_linux_instance_ip> ```

## Step 2: Update the System

``` sudo dnf update ```

## Step 3: Install Java

``` sudo dnf install java-17-amazon-corretto -y ```
### Verify the installation with:

``` java -version ```
## Step 4: Add the Jenkins Repository 

``` sudo wget -O /etc/yum.repos.d/jenkins.repo \https://pkg.jenkins.io/redhat-stable/jenkins.repo ```

### Import a key file from Jenkins-CI to enable installation from the package:

``` sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key ```

## Step 5: Install Jenkins

``` sudo dnf install jenkins -y ```

## Step 6: Start and Enable Jenkins
```sudo systemctl enable jenkins
   sudo systemctl start jenkins 
```
## Step 7: Access Jenkins
``` http://your_amazon_linux_instance_ip:8080 ```

