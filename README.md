## Notes
- Add multiple tasks in one
- Specify present/absent to add/delete S3 Buckets
- Check naming convention before 

> Remove become & become_method
> This still gives the boto3 error.

# Ansible-S3-Bucket
Creating S3 Buckets using Ansible

Notes: [S3 Bucket Naming Convention](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html)
- Bucket names must be between 3 and 63 characters long.
- Bucket names can consist only of lowercase letters, numbers, dots (.), and hyphens (-).
- Bucket names must begin and end with a letter or number.
- Bucket names must not be formatted as an IP address (for example, 192.168.5.4).
- Bucket names must be unique within a partition. A partition is a grouping of Regions. AWS currently has three partitions: aws (Standard Regions), aws-cn (China Regions), and aws-us-gov (AWS GovCloud [US] Regions).
- Buckets used with Amazon S3 Transfer Acceleration can't have dots (.) in their names. For more information about Transfer Acceleration, see Configuring fast, secure file transfers using Amazon S3 Transfer Acceleration.



|                          |  s3Bucket.yml|
:------------------------- |:-------------------------
|---                       |---
|- name: Install prometheus|- name: Install prometheus|
|  hosts: webservers       |   hosts: webservers|
|  become: true            |<strike>become: true<strike>|
|  become_method: sudo     |<strike>become_method: sudo<strike>|
|                          | connection: local|
  
  


