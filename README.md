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
vpc_subnet_id: "{{pubsub1id}}"

- name: Creating Bastion Host
  ec2:
  key_name: vprofile-key
  region: "{{region}}"
  instance_type: t2.micro
  image: "{{ bastion_ami }}"
  register: bastionHost_out