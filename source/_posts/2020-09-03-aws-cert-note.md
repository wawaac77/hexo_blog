---
title: AWS Cert Note
date: 2020-09-03 20:52:09
tags: aws
---

Aws fundamentals

AWS Regions
naming convension: us-east-1
a region is a cluster of data center

most aws are region-scoped

AZ: availability Zones

- Each region has many AZ
    - usually 3, min 2, max 6

- AZ are location isolated, but connected through bandwith

## IAM - Identity and Access Management

Users
Groups
Roles

Root account should never be used and shared, except for initial setup.

IAM is ath teh center of AWS

Policies => JSON document

Users => usually a physical person
Groups => functions (admins, devOps
    Teams
Roles => internal usage

IAM has a global view, across all the locations

least privilege principles

IAM Federation
SAML standard

- One IAM Role per Application
- IAM credentials never shared

## EC2
- renting virtual machines EC2
- sotring data on virtual drives EBS
- distributing load across machines ELB
- scaling the services using an auto-scaling group ASG

*common exam question*: Permissions 0666 for 'EC2Tutorial.pem' are too open.
*solution*: chmod 0400 EC2Tutorial.pem

logout: control + D /exit

## Security groups
- can atteched to multiple instances
- locked down to a region / VPC combination
- security groups are like firewall

## Private vs. Public IP IPv4
- IPv6 => common for IoT
- Public IP: machine can be identified on the internet
- Private IP: machine can only be identified on a private network only
- Elastic IPs - try to avoid using Elastic IP
- ifconfig -a

## Apache Server


## questions: 

    All of these are IAM components except... => organisation
    
    An IAM user can belong to multiple groups => true

## EC2 Instance launch types
- on demand instances: short workload, predicatable pricing
- reserved: min 1 year
    - long workloads
        - up to 75% discount
        - reserve 1 or 3 years
    - convertible reserved instances: long workloads with flexible instance
        - up to 54% discont
    - scheduled reserved instances: every Thursday between 3-6pm (exam)

- spot instance: short workload, cheeap, might lose instances
    - up to 90% compared to on-demand
    - workloads that are resilient to failure
        - pssible to retry
        - data analysis
        - image processing
        - batch jobs
        - not for critical jobs or databases
        - reserved instances for baseline + on-demand & spot for peaks
- dedicated instances
    - physical
    - full control
    - visibility into underlying socket/hardware
    - for 3 year
    - strong regulatory or compliance 
    - dedicated host (exam)
- dedicated hosts: book an entire physical server
- exam: discount based on type

### on demond

## instance type
- exam: will choose which type
