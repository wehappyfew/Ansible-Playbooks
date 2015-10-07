# Ansible-Playbooks
Ansible playbooks to automate various deployment routines [not only] on AWS 

Prerequisites:

Case 1:
Create a boto.cfg file in /etc folder, [sudo nano /etc/boto.cfg] , 
and copy-paste your AWS creds in it.

The boto.cfg file will be like this:
[Credentials]
AWS_ACCESS_KEY_ID = 'blablabla223%$%$%$%4%545'
AWS_SECRET_ACCESS_KEY = 'blublublu223%$%$%$%4%545'

This setup concerns you if you want all the users in the machine to access the creds. 
Like a QA or Staging server.

Case 2:
Create a file in the home folder [~/.boto] of a specific user that you want only him to have access to the creds.
Copy-paste the AWS creds as stated above.

Official AWS docs here: http://boto.readthedocs.org/en/latest/boto_config_tut.html


Run each playbook from the command line (Linux) like this:

ansible-playbook "-e 'VAR1=[value1] VAR2=[value2]'" [playbook-name].yml
