# BaseLampStackCreationNotes
My personal notes on base lamp stack creation with auto virtual host creation config

### create sudo user 

    adduser username
    usermod -aG sudo username
    su - username

### Add ssh public key

    mkdir ~/.ssh/
    cd .ssh
    nano authorized_keys       ( add ssh pub key inside)
    sudo reboot

### Follow this tutorial to create swap space to avoid running out of RAM
https://www.digitalocean.com/community/tutorials/how-to-add-swap-space-on-ubuntu-16-04

### Follow this tutorial to install LAMP stack
https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04

### Run the below commands to download and configure automatic virtual host creation command line tool

    cd /usr/local/bin
    sudo wget -O virtualhost https://raw.githubusercontent.com/solancer/virtualhost/master/virtualhost.sh
    sudo chmod +x virtualhost

    sudo virtualhost create rsite.dev my_sutom_dir_full_path
