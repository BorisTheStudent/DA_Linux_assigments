# Documentation of assignment 3
## points 1-4
I can't really comment much about 1-4 steps since those were instructed and didin't caused any issues, while following the instructions
## point 5
In order to do point five, I had seperate it to different task as:
1. Create /opt/projekti directory:

   borisuser@ubuntu-robotics-DA:~$ cd
   
   borisuser@ubuntu-robotics-DA:~$ mkdir projekti
   
   borisuser@ubuntu-robotics-DA:~$ sudo mv projekti /opt/
   
2. Create group and add tupu and lupu in it:
   
   borisuser@ubuntu-robotics-DA:~$ sudo addgroup tupujalupu
   
   Adding group `tupujalupu' (GID 1006) ...
   
   Done.
   
   borisuser@ubuntu-robotics-DA:~$ sudo adduser tupu tupujalupu
   
   Adding user `tupu' to group `tupujalupu' ...
   
   Adding user tupu to group tupujalupu
   
   Done.
   
   borisuser@ubuntu-robotics-DA:~$ sudo adduser lupu tupujalupu
   
   Adding user `lupu' to group `tupujalupu' ...
   
   Adding user lupu to group tupujalupu
   
   Done.

   NOTE: Instead of "Projekti" I named it as "tupujalupu"
3. Give group access to folder:
   
   borisuser@ubuntu-robotics-DA:~$ sudo chgrp -R tupujalupu /opt/projekti
   
4. Set permissions on folder:
   borisuser@ubuntu-robotics-DA:~$ sudo chmod -R 775 /opt/projekti

5. Make all folders subsequently created inside /opt/projekti to be owned by group tupujalupu:

   borisuser@ubuntu-robotics-DA:~$ sudo setfacl -dR -m g:tupujalupu:rwx /opt/projekti
   
   NOTE: in order to do need to install acl:
   
   borisuser@ubuntu-robotics-DA:~$ sudo apt-get install acl

6. Give ownership of this directory to the group by ID:

    sudo chown -R :1006 /opt/projekti
