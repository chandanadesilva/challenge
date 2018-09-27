# Challenge
This repo and example Ansible Playbook which sets up an Ngnix Container on an AWS EC2 instance.

The playbook;

	installs an EC2 instance inside an AWS VPC using an AWS Cloudformation stack (defined in cfn/challenge-cfn.yml)
	
	starts an Ngnix Docker container on the EC2 instance
	
	connects to the Ngnix container's http port using curl, and find the word which occurs the most number of times in the initial web page ( the work **nginx** occurs 8 times)
	
	monitors and logs Docker performance and resourse usage (every 10 seconds) using [Performance Co-Pilot](http://pcp.io)

To run the playbook, clone the repository to your workspace,

```bash
cd /path/to/workspace
AWS_PROFILE=<your aws profile in .aws/credentials> ansible-playbook ansible/challenge.yaml
```	
	