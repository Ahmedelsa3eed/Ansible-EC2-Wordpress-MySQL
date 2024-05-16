# Ansible Playbook
This is a simple Ansible playbook to provision an EC2 instance on AWS, setup a wordpress site, and create a MySQL database.

## Prerequisites
The file ``vars.yml`` should define the following variables:
```yaml
region: <AWS-REGION>
access_key: <AWS-ACCESS-KEY-ID>
secret_key: <AWS-SECRET-ACCESS-KEY>

mysql_root_password: <MYSQL-ROOT-PASSWORD>
mysql_db: <MYSQL-DB-NAME>
mysql_user: <MYSQL-DB-USER>
mysql_password: <MYSQL-DB-PASSWORD>
```

## Usage
```bash
ansible-playbook -i demo.aws_ec2.yml wordpress.yml -e "@vars.yml"
```