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



vpcid: vpc-0ef9092105ba5c6ca
pubsub1id: subnet-0b8cd8050c89a4e70
pubsub2id: subnet-02140e8a98d9ff705
pubsub3id: subnet-0787e2344bb4f5e68
privsub1id: subnet-0fd266e012403206f
privsub2id: subnet-020f823ded3a26328
privsub3id: subnet-023e507b53720318e
igwid: igw-06265233ab7046d8c
pubRTid: rtb-0f297b66a333a1107
NATGWid: nat-0ab47f0a106b9ead4
privRTid: rtb-0ec7f868d2184dc05
BastionSGid:

# BEGIN ANSIBLE MANAGED BLOCK
BastionSGid: sg-08afc98e00d925de7
# END ANSIBLE MANAGED BLOCK














