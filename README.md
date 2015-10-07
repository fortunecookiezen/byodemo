# byodemo
Bring Your Own Development environment demo

Vagrant Configuration
---------------------
>mkdir c:\users\jamesp\Vagrant_Photon
>cd Vagrant_Photon; vagrant init vmware/photon; vagrant up --provider virtualbox

install java, ruby, git, 

Modify Vagrantfile:

add port mapping localhost:8080 to guest:8080

add filesystem mapping of /Users/James/byodemo to /data

Putty Configuration
--------------------
run vagrant ssh to get location of private key: .vagrant/machines/default/virtualbox/private_key

use puttygen to convert key to format usuable by putty, store in putty profile for Vagrant_Photon

Docker Configuration
--------------------
Enable docker: 

  systemctl docker enable

to run docker image:

  docker run -p 8080:8080 -t fortunecookiezen/gs-spring-boot-docker

Useful Commands
----------------
dos2unix (removes DOS formatting, needed when running gradlew):

  tr -d '\015' \<DOS-file \>UNIX-file
