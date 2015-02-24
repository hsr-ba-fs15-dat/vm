# project-dat-HSR
Main Repository

## Setup Instructions
1. Clone Repo into Folder
2. Install Vagrant Tools
   On Linux and Mac OS it is recommended to install the vagrant bind plugins.
  
  ```sh
   $ vagrant plugin install vagrant-bindfs
   ```
3. Fire Vagrant VM up 

   ```shell
   $ vagrant up
   ```
4. Connect to VM via SSH
   
   ```shell
   $ vagrant ssh
   ```
5. Initial Setup dat
  
   ```shell
   $ dat init
   $ dat listen
   ```
6. Nodejs Server files are located in ./nodejs in the repository and link to /var/www in the vm.
7. Update the host file on your computer to use the reverse proxy in the vm.
  ```shell
  $ sudo vi \etc\hosts
  ```
  add these lines
  ```
  192.168.56.101 dat.dev www.dat.dev
  192.168.56.101 node.dev www.node.dev
  ```
8. On changes on the VM either destroy the vm (`$ vagrant destroy`) or try to update (`$ vagrant update`)
