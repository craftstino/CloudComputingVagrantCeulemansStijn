# CloudComputingVagrantCeulemansStijn

This is the lab assingment 2 vagrant and ansible 

Video Timestamps

OO:OO vagrant up

06:50 vagrant ssh ansible

07:10 show ansible version

07:20 ssh from ansible vm to all other vms and showing ip's and apache2 ,php version (not installed)

8:30 doing the ansible ping command to show connection 

8:40 setup some ssh-key on the machine (so i dont need to use the keys with the ansible-playbook comand)

9:30 running the first playbook (install apache and php)

10:10 showing php and apache are installed  (only showed 1 vm )

10:20 running the second playbook (uninstall apache and php)

11:00 running the roles 

12:15 ssh in the database vm to show mysql is installed 

12:38 used some command to create a user for all the machine connecting to the database and allow mysql on the firewall (I am not sure if i needed to make a user this way maby i could have used the default user that is created when installing mysql or i could have maby dont this in the ansible roles but i got errors so i did it this way. This is kinde the same for the firewall i am not sure if it was needed but just did it to be sure. )

14:OO ssh in other machine to show the test.php file in the root

14:20 went to the /var/www/html directory where the php files where located to create a database and connect to it

14:30 used the php files to connect to the database and create the database CloudComputing 

16:00 switched form cmd to browser to show the connection to the database and that is worked (the 2 webservers with addremove could add names of people and there job to the database and could be look at in the list.php )

17:50 showed that the CloudComputing database was created 

18:30 vagrant destroy 
