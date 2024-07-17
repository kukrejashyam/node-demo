# node-demo
To Install &amp; configure nodejs app for Docker

All components are docker-based

### With Docker

#### Steps to Create image, Container & run this simple application

Step 1: clone this git repository on your AWS Linux EC2 instance using below command

    git clone https://github.com/kukrejashyam/node-demo.git

Step 2: Go inside "docker-c3-app-nodb" directory 

    cd node-demo/

Step 3: Build the version-1 app image with the name "node-demo" and tag 1.0 using below command
    
    docker build . -t node-demo:1.0  

Step 4: Create a container from the above created image "node-demo:1.0" and expose it to port 9003 using below command.

    docker run -d -p 9003:80 node-demo:1.0

_NOTE: Don't forget to open this port 9003 in security group of respective EC2 instance in your AWS account_

Step 5: Now access the below URL in the browser using the public ip of your EC2 instance.

    http://ec2-public-ip:9003

    e.g.  http://184.72.185.255:9003

_NOTE: Copy the correct Public IP of this EC2 instance from your AWS account_

