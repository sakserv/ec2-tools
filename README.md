ec2-tools
=========

Tools for working with ec2 nodes

Prerequisites
-------------
1. passphraseless ssh-key, default ~/.ssh/id_rsa (because if a user knows nothing of ssh, this is the default)
2. git needs to be installed
3. the "Name" tag on the EC2 instance should be set to the hostname you want the node to have

Bootstrap the node
------------------
The bootstrap and initial configuration tool makes use of ec2-host (and you get [ec2-ssh](https://github.com/Instagram/ec2-ssh) for free). 

Set the env vars below:

*export AWS_ACCESS_KEY_ID=""
*export AWS_SECRET_ACCESS_KEY=""
*export AWS_EC2_REGION=""

Run the following to bootstrap the node
`wget --delete-after -q -O - https://raw.githubusercontent.com/sakserv/ec2-tools/master/init_node | bash`
