# WORKING WITH TEXT
## Module Review

### END OF MODULE LAB - Working with Text

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

![image](https://user-images.githubusercontent.com/36435980/144498336-a8167036-c939-4374-860c-2a720abf1ffd.png)

*****
### TASK 3:  Perform the following operations on SERVER2

1. Put the first 15 lines of the file */usr/share/dict/words* into the file *~/myfile*.
2. Remove any lines that end in numbers from *~/myfile*.
3. Change all lower case letters in *~/myfile* to capital letters and change the only capital letter to lower case.
4. Find all of the **pdf** files in the file system and list the locations in a text file named *~/pdf.lst*.
5. Find all of the **jpg** files in the file system and list the locations in a text file named *~/jpg.lst*
6. Add the following host names and IP addresses to the file */etc/hosts* :
```
192.168.4.3        server1
192.168.4.4        server2
192.168.4.254      workstation
```
7. Create a file that reads "Welcome to Server 2" named *welcome.txt* in */etc/skel/* 

*****
### SOLUTION


1. Put the first 15 lines of the file */usr/share/dict/words* into the file *~/myfile*.

![image](https://user-images.githubusercontent.com/36435980/144685150-24368165-a03e-459a-80c2-29be7ece9cc8.png)

2. Remove any lines that end in numbers from *~/myfile*.
3. Change all lower case letters in *~/myfile* to capital letters and change the only capital letter to lower case.

![image](https://user-images.githubusercontent.com/36435980/144685214-7de9a856-0ccb-4846-ba7d-0a31267f06b5.png)

4. Find all of the **pdf** files in the file system and list the locations in a text file named *~/pdf.lst*.

![image](https://user-images.githubusercontent.com/36435980/144685249-30c2f6ec-5520-4c00-914e-6f4bb50b0154.png)

5. Find all of the **jpg** files in the file system and list the locations in a text file named *~/jpg.lst*

![image](https://user-images.githubusercontent.com/36435980/144685280-89183029-60ac-4fb5-bc29-dc10f75104e4.png)

6. Add the following host names and IP addresses to the file */etc/hosts* :
```
192.168.4.3        server1
192.168.4.4        server2
192.168.4.254      workstation
```

![image](https://user-images.githubusercontent.com/36435980/144685318-7465d93f-306c-4138-a5ba-1400b56fb1ab.png)

7. Create a file that reads "Welcome to Server 2" named *welcome.txt* in */etc/skel/* 

![image](https://user-images.githubusercontent.com/36435980/144685340-a0ad88d1-a856-4ddb-b481-23ae412fe0eb.png)

******
