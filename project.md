Explain Script:
This is a script that helps install a master ans slave Ubuntu Vagrant Machines.
Must Have
-vagrant
-virtual box
Slave And Master:
Memory: 1024
CPUs: 2
slave machine:
    Spec:
        name = slave
        image = ubunta/focal64
        Network:
            private_network:
            constant ip: 192.168.22.12
Slave Configuration:
    update and update machine
    Install:
        sshpass: allows you to enter the password while logging in
        switching the password aunthenticator on for access using password
        restart the sshd service
        install avahi-daemon libnss-mdns
Master Machine:
    Spec:
        name = master
        image = ubunta/focal64
        Network:
            private_network:
            constant ip: 192.168.22.11
Master Configuration:
    update and update machine
    Install:
        sshpass: allows you to enter the password while logging in
        switching the password aunthenticator on for access using password
        restart the sshd service
        install avahi-daemon libnss-mdns
Script Configuration for Master:
 - creating a sudo user named "alsthool"
 - creating an ssh key for the user "Altschool"
 - copy the user "Altschool" ssh to the slave machine (only the user altschool should be able to ssh into the slave machine without a password)
 - copy a file named "/mnt" from the altschool user to the slave machine.
LAMP stack (Master & Slave installation):
    LAMP: (linux, apache, mysql, and php)
        - Installing apache2 web server
        - Installing PHP and requirements
        - Installing MySQL
        - Enabling modules
        - Restarting Apache
Lastly, a LAMP stack will be istalled on both master and slave on the script runs. Apche is goint to restarted after installation and configuration.
Also mySQL server and client are goint to be installed on both master and slave
Different versions of php is going to be installed and permissions for /var/www is goint to be set to an owner and group of "www.data:www.data"