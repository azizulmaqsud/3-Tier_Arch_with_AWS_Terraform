
![alt text](https://miro.medium.com/max/900/1*rJ_YbOr71X1iKrrW3do4nQ.png)

Required Components of AWS
- 1 VPC
- 2 Public subnets
- 2 Private subnets 
- 2 Autoscaling groups
- 5 Security Groups
- 2 Load Balancers, (one private, one public)
- 2 Private EC2 instances (representing our application tier)
- 2 Public EC2 instances (representing our presentation tier)
- 2 Nat Gateways (so private instances can connect to the internet) 
- 2 Elastic IP addresses, one for each Nat gateway
- 1 rds instance

Steps
- 1) Clone the code -
- https://github.com/azizulmaqsud/3-Tier_Arch_with_AWS_Terraform/terrform threetierarch.git
- 2) Create the AWS account - https://aws.amazon.com/console/ 
- 3) Execute the linux command to give permission
- chmod +x setup-ecrs.sh
- 4) Run this on terminal to create the ECR repo and to create images in local and send those to ECR- /setup-ecrs.sh
- 5) Go to terraform folder -
- terraform init
- terraform plan terraform apply

Testing the Application via LB
- 1) Hit the Front end load balancer-
- front-end-lb-**********.us-east-1.elb.amazonaws.com/
- 2) Request to the presentation layer, which forwards the requests to the application layer (via the internal Load Balancer) that finally creates a table called users, and adds 2 users in the table front-end-lb-**********.us-east-1.elb.amazonaws.com/init
- 3) To view the users table you can call
    front-end-1b-**********.us-east-1.elb.amazonaws.com/users

## Thank You!
# Stay Connected !!

https://www.youtube.com/channel/UCNwP7KEElaJ7cdDTLP-KbBg

https://www.linkedin.com/in/azizul-maqsud/

https://azizulmaqsud-1684501031000.hashnode.dev/

https://medium.com/@azizulmaqsud

https://twitter.com/Sohail2me

https://github.com/azizulmaqsud


<a href="https://www.buymeacoffee.com/azizulmaqsud"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=scaleupsaas&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff" /></a> 

# 3-Tier_Arch_with_AWS_Terraform
