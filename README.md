# Installing Docker on AWS Ubuntu
This guide will walk you through the steps required to install Docker on an AWS Ubuntu instance.

## Prerequisites
Before you begin, make sure you have the following:

- An AWS Ubuntu instance
- A user account with sudo privileges
- Internet connectivity
## Step 1: Update the package manager
First, update the package manager to ensure that all the latest packages are installed on your instance.
```bash
sudo apt-get update
```
## Step 2: Install Docker
Install Docker by running the following command:
```bash
sudo apt-get install docker.io -y
```
This will download and install Docker on your AWS Ubuntu instance.

## Step 3: Verify the installation
Verify that Docker is installed correctly by running the following command:
```bash
docker --version
```
This will display the version of Docker that is installed on your instance.

## Step 4: Add user to the docker group
To avoid running Docker commands with sudo, add your user to the docker group:

```bash
sudo usermod -aG docker ${USER}
```
Note that you need to log out and back in again for the changes to take effect.

## Step 5: Test Docker
Test your Docker installation by running the following command:
```bash
docker run hello-world
```
This will download a Docker image and run it in a container. If everything is installed correctly, you should see a message confirming that Docker is working correctly.

## Conclusion
Congratulations, you have successfully installed Docker on your AWS Ubuntu instance! You can now use Docker to create and manage containers on your instance.