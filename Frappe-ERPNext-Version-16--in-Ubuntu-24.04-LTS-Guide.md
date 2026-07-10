# Frappe-16 / ERPNext-16 Installation Steps Ubuntu 24.04 LTS

## Prerequisites

1. Ubuntu 24.04 LTS
2. python3.14
3. pip 25.3+
4. node 24
5. yarn 1.22+
6. redis 6+
7. mariadb 11.8


## Step 1
```bash
sudo apt-get update && sudo apt-get upgrade -y
```
Updates package list and upgrades all installed system packages

## Step 2
```bash
sudo add-apt-repository ppa:deadsnakes/ppa
```
Adds the Deadsnakes PPA to install newer Python versions

## Step 3
```bash
sudo apt update
```
Refreshes the package list after adding a new repository

## Step 4
```bash
sudo apt install python3.14 python3.14-venv
```
Installs Python 3.14 and its virtual environment module

## Step 5
```bash
python3.14 --version
pip3.14 --version
```
Verifies Python and pip installation versions
 
For any issue Follow these one

## Step 5.1
```bash
python3.14 -m ensurepip --upgrade
```
Installs pip for Python 3.14 using the built-in ensurepip module

## Step 5.2
```bash
curl -sS https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3.14 get-pip.py
```
Downloads and runs the official pip installation script (Use this if Step 5.1 fails)


## Step 5.3
```bash
sudo rm /usr/lib/python3/dist-packages/distutils-precedence.pth
```
Verifies pip is successfully installed. Always use `python3.14 -m pip install <package_name>` to install packages going forward.


## Step 5.4
```bash
sudo rm /usr/lib/python3/dist-packages/distutils-precedence.pth
```
Verifies pip is successfully installed. Always use `python3.14 -m pip install <package_name>` to install packages going forward.


## Step 5.5
```bash
python3.14 -m pip --version
```
Verifies pip is successfully installed. Always use `python3.14 -m pip install <package_name>` to install packages going forward.




## Step 6
```bash
sudo apt-get install python3-setuptools python3-pip -y
```
Installs setuptools and pip for Python package management

## Step 7
```bash
sudo apt install pkg-config -y
```
Installs pkg-config required for compiling native dependencies

## Step 8
```bash
sudo apt install python3.14-dev -y
```
Installs Python development headers for building extensions

## Step 9
```bash
sudo apt install mariadb-server -y
```
Installs MariaDB database server

## Step 10
```bash
sudo mysql_secure_installation
```
Secures MariaDB by setting root password and removing defaults

## Step 11
```bash
sudo apt-get install libmysqlclient-dev -y
```
Installs MySQL/MariaDB client libraries for Python connectors

## Step 12
```bash
sudo service mysql restart
```
Restarts the MySQL/MariaDB service to apply changes

## Step 13
```bash
sudo apt-get install redis-server -y
```
Installs Redis used by Frappe for caching and queues

## Step 14
```bash
sudo apt install curl
```
Installs curl for downloading scripts and files

## Step 15
```bash
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
```
Installs NVM (Node Version Manager)

## Step 16
```bash
source ~/.profile
```
Reloads shell profile to enable NVM

## Step 17
```bash
nvm install 24
```
Installs Node.js version 24 using NVM

## Step 18
```bash
sudo apt-get install npm -y
```
Installs npm package manager

## Step 19
```bash
sudo npm install -g yarn
```
Installs Yarn globally for frontend asset builds

## Step 20
```bash
sudo apt-get install xvfb libfontconfig -y
```
Installs dependencies required for PDF generation

## Step 21
```bash
sudo apt-get install xfonts-75dpi
```
Installs fonts required by wkhtmltopdf

## Step 22
```
https://wkhtmltopdf.org/downloads.html
```
Reference link to download wkhtmltopdf package Download the .deb file for your system based on amd64 or arm64 architecture. Here using arm64 architecture

## Step 23
```bash
sudo dpkg -i wkhtmltox_file.deb
```
Installs wkhtmltopdf package manually

## Step other 22.
```
sudo apt update
sudo apt install wkhtmltopdf -y
```
This will automatically download the correct version for Ubuntu 24.04 and handle all dependencies for you, so you don't need to run --fix-broken install

## Verify Step 22
```bash
wkhtmltopdf --version
```
Verify the installation


## Step 24
```bash
sudo -H pip3 install frappe-bench --break-system-packages
```
Installs Frappe Bench CLI tool

## Step 25
```bash
bench init frappe-bench --frappe-branch version-16 --python python3.14
```
Initializes a new Frappe bench with version 16

## Step 26
```bash
cd frappe-bench/
```
Moves into the Frappe bench directory

## Step 27
```bash
bench start
```
Starts Frappe development server

## Step 28
```bash
bench new-site local.com
```
Creates a new Frappe site

## Step 29
```bash
bench use local.com
```
Sets the active site for bench commands

## Step 30
```bash
bench get-app erpnext --branch version-16
```
Downloads ERPNext app from GitHub

## Step 31
```bash
bench install-app erpnext
```
Installs ERPNext app on the site

--
```
```
## Connect with Me

[![Website](https://img.shields.io/badge/Website-000000?style=for-the-badge&logo=googlechrome&logoColor=white)](https://yourwebsite.com)&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ali-raza-643520217?utm_source=share_via&utm_content=profile&utm_medium=member_android)&nbsp;
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/yourusername)