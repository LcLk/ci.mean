##Setup on Ubuntu 14.04


###Install Node
...
sudo apt-get install npm

#Make sure the legacy node package isn't installed:
sudo apt-get remove node

#Instead of installing the legacy 'nodejs-legacy' app, create a sym link:
sudo -s /usr/bin/nodejs /usr/bin/node
...

###Install SASS
...
sudo apt-get install rbenv ruby-build
rbenv install 2.0.0-dev
sudo gem install sass --no-rdoc
...

###Install MongoDB
...
sudo apt-get install mongo
sudo mkdir /data
sudo mkdir /data/db
mongod

#If there are permission errors:
sudo chmod 0755 /data/db
sudo chown mongodb:mongodb /data/db
...

###Install requirements for angular-fullstack (Not needed when using this repo, only when generating from scratch)
...
sudo npm install -g yo bower grunt-cli gulp generator-angular-fullstack
yo angular-fullstack
...

