# How to install Python 3.6.4 on CentOS

1. Open a Terminal and add the repositoryto your Yum install 

   ```bash
   sudo yum install -y https://centos7.iuscommunity.org/ius-release.rpm
   ```

2. Update Yum to finish adding the repository

   ```bash
   sudo yum update
   ```

3. Download and install Python

   ```bash
   sudo yum update
   ```

4. Check if the correct version of Python

   ```bash
   python3.6 -V
   ```

# Configure Python3.6 virtual environment

1. Install pip, a Python Package Manager

   ```bash
   wget https://bootstrap.pypa.io/get-pip.py
   sudo python3 get-pip.py
   ```

2. Make use of virtual environments for Python development

   ```bash
   sudo pip install virtualenv virtualenvwrapper
   sudo rm -rf ~/get-pip.py ~/.cache/pip
   ```

3. Append the following lines to your `~/.bashrc`

   ```bash
   # virtualenv and virtualenvwrapper
   export WORKON_HOME=$HOME/.virtualenvs
   export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3.6
   source /usr/bin/virtualenvwrapper.sh
   ```

4. Update your `~/.bashrc`

   ```bash
   source ~/.bashrc
   ```

5. Create a virtual environment

   ```bash
   mkvirtualenv <your virtual environment name> -p <your python version>
   ```

6. Use your virtual environment

   ```bash
   workon <your virtual environment name>
   ```