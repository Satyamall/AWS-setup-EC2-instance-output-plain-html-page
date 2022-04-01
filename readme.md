
Problem
 - setup an ec2 instance
 - install apache server
 - output a plain html page

View the Html Page: <a href="http://3.110.118.211/">Click here</a>

Setup EC2 instance:
 - click on services
 - click on compute
 - click on instances
 - click on launch instances
 - Choose an Amazon Machine Image (AMI)
 - select the ubuntu server
 - choose Free tier eligible
 - click Next: Configure Instance Details
 - left default and click on Next: Add Storage
 - left default and click on Next: Add Tags
 - click on Add tag
 - fill the tags credential
   - Name  My application 2
   - dev   developers
   - data  01-04-2022
 - click on Next: Configure Security Group
 - click on Add Rule
   - choose SSH  custom IP address  satya
   - choose HTTP custom IP address  satya
 - click on Review and Launch
 - click on launch
 - choose a new key pair
 - choose pair name
 - Download Key Pair
 - click on Launch Instances

Use local Machine for handle
 - make a folder on Desktop => mkdir aws-setup-ec2
 - mv developer.pem aws-setup-ec2
 - cd aws-setup-ec2
 -  ssh -i "key pair file name" ubuntu@"paste the Public IPv4 DNS here"
 - Press Enter
 - sudo apt-get update
 - sudo apt-get install apache2
 - cd /var/www/html
 - pico index.html
 - sudo rm index.html
 - sudo touch index.html
 - sudo pico index.html
 ```js
  <html>
<body>
<h1> Hi Everyone I am Satya Prakash Mall, This is AWS-setup EC2 intances. </h1>
</body>
</html>
```
- Ctrl+S
- ctrl + O
- ctrl + L
- ctrl + X
- refresh the Public IPv4 address in browser.

