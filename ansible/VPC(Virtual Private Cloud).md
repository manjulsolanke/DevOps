VPC(Virtual Private Cloud)
    - Virtual environment
    - Similar to having your own datacenter inside the AWS
    - Logically isolated from other VPCs on AWS
    - One can have multiple VPCs in one account.
    - Once can have full control and resources hosted in the VPC.
    - VPC is region-specific, so it can't span across the regions.
    - VPC can extend AZ within the region
Subnets
    - We can have more than one subnet in AZ.
    - Can subnets extend two AZ? NO is the answer.
VPC compounts
    - CIDR and IP address subnets
    - implied router, which facliliated the route within the subnets
    - Connect different subnets
    - Its central VPC routing functions
Router tables
    - Each subnets will have a route table that the router uses to forward traffic within the vpc.
    - You can have up to 200 routing tables per vpc
    - you can have upto 50 route entries per route table.
    - Each subnet MUST be associated with only one route table at any given time.
    - can I attach the subnet with multiple route tables at any given time? Ans is NO.
    - Can I use same route table to be associated with multiple subnets at the same time? ans is Yes.
    - If you didn't specify a subnet-to-route-table association, the subnets (when they are created) will be associated with the main (default ) VPC route table.
    - Main route table is get created by default by AWS when you create a VPC.
    - You can change the subnet association to another route table, but not both. It would be either/or.
    - You can also edit the main (default) route table if you need, but you can't delete the main route table.
    - However, you can make custom route table manually become the main route table, then you can
    delete the former main, as it is no longer a main route table.
    - Every RT in a VPC comes with a default rule that allows all VPC subnets to communicate with one another. (Where will it be? We can see the CIDR value in the RT destination, and the target will be local)
    - You can not modify or delete this rule.
    - VM1 in subnet1 is not able to connect to VM2 in subnet2. What would be the issue? -  dont say route table issue.



VPC IP Addressing
    - Once the VPC is created, you can NOT change its CIDR block range. You can, however, expand your
    VPC CIDR by adding new/extra IP address ranges.
    - The different subnets within a VPC can NOT OVERLAP.
    - First 5 IP address in each subnet and the last one are reserved by AWS
    - Ex. if the subnet is 10.0.0.0/24
    - 10.0.0.0 is the base network
    - 10.0.0.1 VPC route
    - 10.0.0.3 DNS related
    - 10.0.0.4 Reserved for the future use
    - 10.0.0.255
    - Internet gateway - Without IG VPC can't communicate to outside the world.
    - is the gateway through which your VPC communicates with the internet and with ohter
    AWS services
    - is a horizontally scale redundant and highly available system.
    - It performs NAT (static one-to-one) between your private and public (or elastic) IPv4 addresses.


Security groups 
    - Its virtual firewall (defence in depth, SG would be last defence compounts)
The first line of defence is network access control lists (NACLs).

Virtual private gateway (will provide connectivity to own premises alike HQ )




EC2 ENI ( Elastic Network Interface)
    - eth0 is the primary  network interface
        - you can't move/detach the primary (eth0) interface an instance
        - By default, eth0 is the only ENI created with an ec2 instance when lunched 
        - you can add more than one interface to ec2.
        - An ENI is bound to an AZ.
        - Cold attach - When Instance creating
        - Hot attach - attach ENI while running instance
        - Warm attach of ENI - attach ENI when instance is  stop



IAM feature
    - Shared access to your AWS account
    - Granular permission
    - Secure access to your aws account resources for application that run on AWS ec2 instance
    - MFA 
    - Identity federation
    - Identity information assurance (cloudtrail - can identity who access what?)
    - Integrated with many aws services
AWS IAM Elements
- Accessing IAM
    - AWS Console 
    - Promgrammatic access
- Principle
 Principle is an identity that can take an action on an AWS account.
    - user
    - role
    - application
    - Fedrated users

- Request
 - When a principle sends a request via console, cli, sdks, or api including followings
    - action (or operations) that the principle wants to perform
    - resource upon which the action are performed
- Authentication
- Authorization
- Action
- Resource


aditya@araadigit.com
cloudhealth
cloudcheckr





Storage
    - object storage
        - s3 
        storage classes
            - s3 stdrd 
            - Glacier -> retive -> mintues
            - Archive
    - file storage
        - EFS (Elastic File System) --> autoscaling  
    - block storage
        - EBS ( Elastic Block storage) -> 100GB -> extend 
Route53
ELB
Autoscaling

A security flaw in kube-apiserver has been found that enables an aggregated API server to divert client traffic to any URL.

This vulnerability was given a medium rating and the CVE-2022-3172 designation.


Am I at risk?

All Kubernetes clusters with the following versions that are running aggregated API servers are impacted. 

To identify if you have aggregated API servers configured, run the following command:

kubectl get apiservices.apiregistration.k8s.io -o=jsonpath='{range .items[?(@.spec.service)]}{.metadata.name}{"\n"}{end}'

Refer <https://www.hitachivantara.com/en-us/products/x-as-a-service/staas.html>

Affected Versions
kube-apiserver v1.25.0
kube-apiserver v1.24.0 - v1.24.4
kube-apiserver v1.23.0 - v1.23.10
kube-apiserver v1.22.0 - v1.22.13
kube-apiserver <= v1.21.14

Fixed Versions

kube-apiserver v1.25.1
kube-apiserver v1.24.5
kube-apiserver v1.23.11
kube-apiserver v1.22.14
