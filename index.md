# lab1 report
1. part 1: The first step is to install Visual Studio Code. For this, I went to the website [vscode](https://code.visualstudio.com/download) and downloaded the mac version. Here is the starting page.
* <img src="https://github.com/josephjo7star/labreport1/blob/main/image1.png" />
---
2. part 2: The second step is to remotely log into the computer. The first thing I did is open a terminal window and type out *ssh username@ieng6.ucsd.edu (username to be replaced by yours)*. Then I enter the password and logged in.
* ![my result](https://github.com/josephjo7star/labreport1/blob/main/image4.png)
* The account names that appeared in these screenshots might be different because I was using different accounts due to the problem with ssh login.
---
3. part 3: Now run some commands. ls allows you to see all the directories; cd follows by a directory name allows you to move into such a directory; mkdir followed by a name allows you to create a new directory with the name that you entered.
* ![my result](https://github.com/josephjo7star/labreport1/blob/main/image2.png)
---
4. part 4: For this step, the first thing you need to do is make a file on your computer. After that, type in the following on your local terminal window: scp WhereAmI.java username@ieng6.ucsd.edu:~/
* After that, you should see the file on your remote computer
* ![my result](https://github.com/josephjo7star/labreport1/blob/main/image3.png)
---
5. part 5: for setting up ssh key, the first thing you need to do is type *ssh-keygen* on your computer's terminal window. Then follow the step and enter the file name of where you want your key to be stored. when it asks you to enter the passphrase, press "enter" twice because it means "no passphrase".
* when it's finished, follow the following steps:
  1. on your computer terminal window, log in to your ssh 
  2. on your remote computer, type "mkdir .ssh"
  3. log out
  4. type "scp /Users/joe/.ssh/id_rsa.pub cs15lfa22@ieng6.ucsd.edu:~/.ssh/authorized_keys" but replace the path and user name with your own
  5. after that, you should be able to use scp or log into ssh without entering your password
* ![my result](https://github.com/josephjo7star/labreport1/blob/main/image6.png)
* here is my result, but there is something wrong. you can see that even after I finished the above step, it still requires entering the password. I do not know the reason for this, but I suspect that it's because I was not logging into the cse15l lab account, but rather my school account. Some of the settings may be different between the two accounts. Also when I tried to type "mkdir .ssh", it tells me that a directory called .ssh had already existed so you can see me trying to delete everything in the directory and create a new one
---
6. The last part is optimizing. About this one, the best thing I could think of was just that we can use semicolon to separate multiple commands so we can write them all at once without having to, say, wait for the computer to login to ssh and then type out the rest of the commands.
* ![my result](https://github.com/josephjo7star/labreport1/blob/main/image5.png)
* this was my attempt. Unfortunately, it was not successful and I couldn't try again because after I took this screenshot, I was no longer able to login to my ssh account and this is the same problem that many people was having in the lab session and has something to do with passwords. For my failed attempt above, I was not using the command for scp correctly, so I wouldn't be able to transfer the file let alone complie and run it. If I'd type the command correctly, it would have worked.
