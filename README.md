# ec2-setup
Setup Ubuntu Operating System on ec2 With NodeJS, SailsJS and MongoDB

# For Ubuntu Essential
``
sudo apt-get update
sudo apt-get install build-essential libssl-dev
``

# Install Git
``
sudo apt-get update
sudo apt-get install git
``

# Istall NodeJS
Using nvm
``
curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh -o install_nvm.sh
nano install_nvm.sh
bash install_nvm.sh
source ~/.profile
``
Get All Node Version
``
nvm ls-remote
``
Choose a version
``
nvm install 5.11.1
node -v
nvm ls
``
Set As default
``
nvm alias default 5.11.1
``

# Install MongoDB
``
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927
touch /etc/apt/sources.list.d/mongodb-org-3.2.list
# for Ubuntu 12.04
echo "deb http://repo.mongodb.org/apt/ubuntu precise/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list

# for Ubuntu 14.04
echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list

# for Ubuntu 16.04
echo "deb http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list

sudo apt-get update
sudo apt-get install -y mongodb-org
sudo apt-get install -y mongodb-org=3.2.10 mongodb-org-server=3.2.10 mongodb-org-shell=3.2.10 mongodb-org-mongos=3.2.10 mongodb-org-tools=3.2.10

# Start MongoDB
sudo service mongod start
# Stop MongoDB
sudo service mongod stop
# Restart MongoDB
sudo service mongod restart

``



