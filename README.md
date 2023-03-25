setup multiple github account on one machine:
cd to path: C:\Users\jiaxu\.ssh
delete everything
open git bash, initialize ssh-agent:
ssh-agent -s
eval $(ssh-agent -s)

generate ssh for your machine (id_rsa) and add to ssh-agent:
ssh-keygen -t rsa
ssh-add /c/Users/jiaxu/.ssh/id_rsa

generate ssh for each github account
ssh-keygen -t rsa -C "tksbsb@gmail.com" -f "tksbsb"
ssh-add tksbsb
ssh-keygen -t rsa -C "tksbsbw@gmail.com" -f "tksbsbw"
ssh-add tksbsbw

go to your github repo website -> user settings -> add ssh key
create 2 keys, one for tksbsb.pub another one for id_rsa.pub
do the same for tksbsbw

git clone using ssh options
