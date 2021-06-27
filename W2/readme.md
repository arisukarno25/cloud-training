## How to Setup environment nodeJS 

1. install dependencies 
# here using CentOS
[ec2-user@ip-172-31-26-166 W2]$ curl -sL https://rpm.nodesource.com/setup_10.x | sudo bash -
[ec2-user@ip-172-31-26-166 W2]$ sudo yum install nodejs
[ec2-user@ip-172-31-26-166 W2]$ node --version

2. inizialize
# setup npm 
[ec2-user@ip-172-31-26-166 W2]$ npm init
[ec2-user@ip-172-31-26-166 W2]$ npm install express
[ec2-user@ip-172-31-26-166 W2]$ node ./sample-apps.js #just for testing

3. Setup PM2 
# in production we need to make the apps always running, it can use a PM2 
[ec2-user@ip-172-31-26-166 W2]$ sudo npm i -g pm2 
[ec2-user@ip-172-31-26-166 W2]$ sudo pm2 status
[ec2-user@ip-172-31-26-166 W2]$ sudo pm2 start ./sample-apps.js 
[ec2-user@ip-172-31-26-166 W2]$ sudo pm2 stop ./sample-apps.js  #if you would like to stop the apps