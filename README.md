AWS-EC2
=========

This Role will launch two AWS EC2 instances with basic configuration.

Requirements
------------
Install following package on ansible controller:
1. pip or pip3
2. boto or boto3

```
Create one file at  '~/'    with name ".boto"

// add following data in file

[Credentials]
aws_access_key_id = <your_access_key_here>
aws_secret_access_key = <your_secret_key_here>

Note: it will set your AWS credentails for API calls.
```

Role Variables
--------------
Description of variables used by this Role.

| Variable | File | Comment |
|--------|----|-------|
|`key` | vars/main.yml | Give your Key |
|`region` | vars/main.yml | Give region name(Ex. ap-south-1) |

Description of variables for master.

| Variable | File | Comment |
|--------|----|-------|
|`instance_type_Master` | vars/main.yml | Give instance type(Ex. t2.micro) |
|`image_Master` | vars/main.yml | Give image name (Ex. ami-0bcf5425cdc1d8a85) |
|`security_group_Master` | vars/main.yml | Give security group(Ex. Kubernetes-Master)|
|`count_Master` | vars/main.yml | Give count of instance (Ex. 1)|
|`subnet_id_Master` | vars/main.yml | Give subnet (Ex. subnet-070fdbef63646c886) |
|`instance_tag_Master` | vars/main.yml | Give tag name (Ex. k8s_Master) |

Description of variables for slave.

| Variable | File | Comment |
|--------|----|-------|
|`instance_type_Slave` | vars/main.yml | Give instance type(Ex. t2.micro) |
|`image_Slave` | vars/main.yml | Give image name (Ex. ami-0bcf5425cdc1d8a85) |
|`security_group_Slave` | vars/main.yml | Give security group(Ex. Kubernetes-Slave)|
|`count_Slave` | vars/main.yml | Give count of instance (Ex. 1)|
|`subnet_id_Slave` | vars/main.yml | Give subnet (Ex. subnet-070fdbef63646c886) |
|`instance_tag_Slave` | vars/main.yml | Give tag name (Ex. k8s_Slave) |

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      roles:
         - "your role name"

License
-------

BSD

Author Information
------------------
venkateshpensalwar@gmail.com

<a href="https://www.linkedin.com/in/venkatesh-pensalwar"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"
/></a>