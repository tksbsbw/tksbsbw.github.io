generate ssh key:
ssh-keygen -o -t rsa -C "tksbsbw@gmail.com"

copy pub ssh key to github acccount setting ssh key

git clone using following command:
git clone git@provider.com:userName/projectName.git --config core.sshCommand="ssh -i ~/location/to/private_ssh_key/id_rsa"
