Skills : 

OS          :  Linux/Unix operating system and shell scripting, Networking.
Cloud       : Any cloud
CI-CD       : Jenkins, Github, GitLab
Automation  : Any programming 
Containers  : Docker and K8s 

=============

Amazon’s philosophy on redundancy and uptime. 
100,000 servers per data center.
The Speed of Light Versus the Cloud
Need for a Global Infrastructure


Netflix:

Netflix poster child of DevOps.
This case study explores how Netflix implemented DevOps by drawing inspiration from its principles and focusing on a collaborative culture.
DevOps culture has enabled them to innovate faster.
With nearly 214 million subscribers worldwide and streaming in over 190 countries, Netflix is globally the most used streaming service today

- It all began with the worst outage in Netflix’s history when they faced a major database corruption in 2008. That time it was close to 8.4 million users and 1/3 were facing issue.
- they choice aws for cloud
- Netflix didn’t just forklift into aws instead of they rewrite application to become true cloudnative.

Netflix converted its monolithic, data center-based Java application into cloud-based Java microservices architecture.

Denormalized data model using NoSQL databases
Enabled teams at Netflix to be loosely coupled
Allowed teams to build and push changes at the speed that they were comfortable with
Centralized release coordination.
Multi-week hardware provisioning cycles led to continuous delivery
Engineering teams made independent decisions using self-service tools


















DevOps Domain
    - Cloud
        - AWS/Azure/GCP
    - Automation  
        - ci-cd, infra (IaC) Terraform, bash scripts/Python
    - CI-CD
        - git - build - test - run/deploy
        - Jenkins/GitLab/Github Action/Azure DevOps 
    - Containers and Kubernetes
        - Docker and k8s


Course: 

AWS - AWS Certified Solutions Architect - Associate
Jenkins -> Jenkins, From Zero To Hero: Become a DevOps Jenkins Master
Containers and Kubernetes : https://kodekloud.com/



DevOps Domain
    - Cloud
        - AWS/Azure/GCP (infra, security, networking, best practices, sevices: EC2/VM, RdS/DB and s3/Blob)
    - Automation
        - ci-cd, infra (IaC), bash scripts/Python
    - CI-CD
        - git - build - test - run/deploy
        - Jenkins/GitLab/Github Action/Azure DevOps 
    - Containers and Kubernetes
        - docker and k8s

    - Oberservability: 
      - Opensource    
        Metrics: Prometheus and Grafana
        Logs   : ELK
        Tracing: OPentelemetry/Jeager
     Enterperise:
      - DataDog, Spunk, Dynatrace etc.   

- 

App -> container -> logs -> 

Node  -> flunetD
    Containers (APPS)
        - > /var/logs/containers/Container-name.lgo (FluenttBit/FluentD/Logstash) 
        -> ElastiSearch - > Kibana

        logAggregator(FluenttBit/FluentD/Logstash) -> ES (NoSQL) -> Kibana



Day01
  EC2/VM/RDS/AKS/EKS ->   
Day02 
- ec2 - webserver, ngnix config restart packages 


Terraform
 - Remote 
 - locsjhjjhjhgtgrjhg hgghgbgb gbnn gnhg hnm jhh mn nj hjjhkjhgyjdf fkjhhg hjh nb bbvn al

 ec2- container build once and run anytime anyhwere 












Exam AZ-104: Microsoft Azure Administrator



bash 
Linux Shell Scripting: A Project-Based Approach to Learning