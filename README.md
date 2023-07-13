# ansible-aws-vpc


wait: yes
wait_timeout: 300
instance_tags:
Name: Bastion_host
Project: Vprofile
Owner: Devops Team
count: 1
count_tag:
Name: Bastion_host
Project: Vprofile
Owner: Devops Team
group_id: "{{BastionSG_out.group_id}}"