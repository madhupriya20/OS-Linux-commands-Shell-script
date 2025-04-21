# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

cat < file2

## OUTPUT

![370723899-4d337431-ead4-485f-a27f-62917fb3bc41](https://github.com/user-attachments/assets/8ced7645-e195-4a90-ac89-16ab577cdead)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![370724042-34aa375e-70c5-4e04-a4c5-10e465e69db6](https://github.com/user-attachments/assets/b11a50f0-def9-49e1-a405-9ddbf4e887d4)

comm file1 file2
 ## OUTPUT

![370724135-0a7a334d-925f-4221-abd6-c7d87a1e550d](https://github.com/user-attachments/assets/f0d56b60-9de6-4a61-b03a-f2494992ce9b)

diff file1 file2
## OUTPUT

![370724206-50de76af-9d73-443e-b46a-8714a4e33631](https://github.com/user-attachments/assets/2d807011-6fc1-432f-b31b-5a4b8dec9046)

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

![370724293-4d34bc5d-73ff-4372-b604-feba720c1587](https://github.com/user-attachments/assets/371f29be-61a7-4813-b889-a71342c740ac)

cut -d "|" -f 1 file22
## OUTPUT

![370724350-32711d9b-72f2-4b2a-bc8a-092cb6f4dfc3](https://github.com/user-attachments/assets/029df177-48c4-4e83-b1f7-170069c1bed9)


cut -d "|" -f 2 file22
## OUTPUT
![370724413-fd30bf2d-5250-4d5b-bbbb-d29048f71e44](https://github.com/user-attachments/assets/d54b19ca-0497-4923-bed2-5d3b387ffe66)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![370724473-5d313db7-c6aa-49f8-98c9-920c1d1ec90b](https://github.com/user-attachments/assets/6bcdf442-07f3-463c-94d6-3b12eb1e283a)


grep hello newfile 
## OUTPUT

![370724606-a25efc95-8385-4bed-8b55-5e0755d9b955](https://github.com/user-attachments/assets/5d3c205d-469f-4b50-957d-31eb110a1c42)



grep -v hello newfile 
## OUTPUT

![370724665-347ff4b3-a0fd-4157-aeb8-b5cc783dc3cb](https://github.com/user-attachments/assets/580e4d48-6ce3-4e7e-8afe-e394e8fadd30)


cat newfile | grep -i "hello"
## OUTPUT

![370724712-1f1cc035-d739-4e5a-86d4-a51719032ee3](https://github.com/user-attachments/assets/10badda8-4ef2-4ac5-ae5a-8d2185653c9f)



cat newfile | grep -i -c "hello"
## OUTPUT

![370724792-f2e612b7-0201-4d40-9b7f-927b8594e426](https://github.com/user-attachments/assets/e56a45c2-976c-49aa-87e5-188923f4d62b)



grep -R ubuntu /etc
## OUTPUT

![370725018-cb2cb8a6-a131-4887-89f5-5b732558b27e](https://github.com/user-attachments/assets/eff0766b-0e64-4259-a764-2e209edd680f)


grep -w -n world newfile   
## OUTPUT
![370725081-d8537c07-03d9-4fc3-973d-b13b9e003beb](https://github.com/user-attachments/assets/a968bd23-a7a8-4f5c-990a-16ba878ba695)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![370725679-fd3feeab-7346-4a3e-b147-0e5543393bce](https://github.com/user-attachments/assets/d743ad2c-47c1-48af-b7e3-62ee1ecdb8f1)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![370725729-46beb223-a521-445e-a52e-f05e7763a331](https://github.com/user-attachments/assets/9763c795-f07b-4021-b0d6-526d5052070c)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![370725778-6cd878ed-febf-4774-9e5c-badf0f3fb4f4](https://github.com/user-attachments/assets/2f15f79b-d440-487d-8594-3d18db47a5b2)



egrep '(^hello)' newfile 
## OUTPUT
![370725841-cede1978-a4d8-4ce2-af3e-62be88d99e84](https://github.com/user-attachments/assets/14dd79db-b621-435f-a8a5-31bea71f6d0d)



egrep '(world$)' newfile 
## OUTPUT

![370726073-eb2127ab-0837-4e9f-bc8d-37c061a2c1dd](https://github.com/user-attachments/assets/add53698-193c-4d67-94a5-009e61625529)


egrep '(World$)' newfile 
## OUTPUT
![370726111-68a136a6-e22d-42bb-87d0-7dc350c748ac](https://github.com/user-attachments/assets/20790c6c-9d8d-44e5-8444-ac90a931e095)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![370726192-0125ddc7-be39-49cf-8248-f82ceb1acd54](https://github.com/user-attachments/assets/f0237d1f-0ede-44eb-9aa8-08f6bf6254d8)


egrep '[1-9]' newfile 
## OUTPUT

![370726231-bd05b680-634e-408a-b51a-25bc2db6052e](https://github.com/user-attachments/assets/de4dff89-9678-4ca5-b950-8f8feb92b4c6)


egrep 'Linux.*world' newfile 
## OUTPUT
![370727023-413f445d-052d-4199-a3a5-2ec115e9722b](https://github.com/user-attachments/assets/38560973-a4d9-42ea-9a16-ed468124c16e)


egrep 'Linux.*World' newfile 
## OUTPUT
![370727121-577e6666-8818-486e-be95-a2ce0a100646](https://github.com/user-attachments/assets/f4a43131-912d-4860-8a18-8b581bbfdcc1)


egrep l{2} newfile
## OUTPUT

![370727176-59727b66-cae9-4176-828f-d10d03f9267b](https://github.com/user-attachments/assets/00a06a3c-91eb-474f-a558-e1cda8e378f3)


egrep 's{1,2}' newfile
## OUTPUT 
![370727227-9d6c41cb-bfd1-4749-8558-b399a281fe97](https://github.com/user-attachments/assets/8123f9f0-7ee6-40a1-931c-1787f5f9c44b)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![370727452-9be0dfef-3f3a-441b-9380-9be888946abb](https://github.com/user-attachments/assets/a4c64969-dae4-435d-8540-016556d4ba68)



sed -n -e '$p' file23
## OUTPUT

![370727492-c9177b13-a1e4-4f62-9e92-ac89c2960783](https://github.com/user-attachments/assets/9f2e1b17-f321-4f12-802d-8bcf7b44cd47)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![370727492-c9177b13-a1e4-4f62-9e92-ac89c2960783](https://github.com/user-attachments/assets/3787bf84-c1f7-489d-9d6f-704d76ad1103)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![370727604-cdadd2ea-d2ec-4340-94a5-d2907e046756](https://github.com/user-attachments/assets/7a243289-f540-45f2-b3c3-564d779b6fdd)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![370727742-ea38ae56-f9b0-463e-8835-e91d0b5bc18f](https://github.com/user-attachments/assets/cb1e1579-a345-426c-a52d-c3f470b4916e)


sed -n -e '1,5p' file23
## OUTPUT
![370727778-d8c9441b-f699-4c8c-849b-6db8aa589a3c](https://github.com/user-attachments/assets/7439645c-0c25-4f1e-989e-3d1e7e79785e)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![370727835-da7b56a5-74ca-428a-bcfc-8e10f277c6ec](https://github.com/user-attachments/assets/689d76e9-d1bd-4d86-a7b7-704526a4d8c1)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![370728137-93b3d047-1599-401b-9ad0-cc75b42b4bbd](https://github.com/user-attachments/assets/848782fb-5cc5-4165-a22d-b9a1dbbd22d4)


seq 10 
## OUTPUT

![370728196-8ca6038a-21ec-4165-ab7d-2992f003d272](https://github.com/user-attachments/assets/f2ce9936-f48e-4d6c-a026-d6f8efca938f)


seq 10 | sed -n '4,6p'
## OUTPUT
![370728699-1837d2bc-76d0-4470-9a3b-86aa70311e24](https://github.com/user-attachments/assets/d95ff45d-58bb-4980-b2b5-95c09efd8216)



seq 10 | sed -n '2,~4p'
## OUTPUT

![370728977-f77ba149-fbe8-4343-af0f-d07d19360d08](https://github.com/user-attachments/assets/af33fb4a-fa36-4639-8a7e-75e45e1ef782)


seq 3 | sed '2a hello'
## OUTPUT

![370729045-71340dd4-f359-401a-a8fa-62a7bd50baec](https://github.com/user-attachments/assets/0bf488c0-5198-42f4-934d-e93f0948093b)


seq 2 | sed '2i hello'
## OUTPUT

![370729152-753bbbc1-a04f-495a-b591-be499feb7c3f](https://github.com/user-attachments/assets/7e8bfdba-9e47-4e4f-b5f9-36ff3eb1adf7)

seq 10 | sed '2,9c hello'
## OUTPUT

![370729283-79879d5d-cee4-4432-9aa9-794c0deaf7fb](https://github.com/user-attachments/assets/444aae8b-151c-44d3-9561-8f30cf77884e)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![370729362-6ca66508-e89a-4641-b0d6-65379bd1c8b5](https://github.com/user-attachments/assets/ed1f0a93-cfe2-4166-81a9-2b408975f2e2)


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![370729517-2da2fcd0-0499-48fe-bf16-0bd23e31eca4](https://github.com/user-attachments/assets/30af7f68-368e-44df-9c76-72a4e479f56d)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![370729629-a8f3640c-52d9-4fc2-bc07-9fd6e6923710](https://github.com/user-attachments/assets/b22d747d-20f4-41e0-a10e-6c302ab818fd)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![370729733-00b655fd-a547-405f-ade4-5b5ea89fc564](https://github.com/user-attachments/assets/989aeec5-9248-4fc6-b828-a12919c9408d)


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![370729877-b919f975-53bf-4cac-b755-f09e27c1f50f](https://github.com/user-attachments/assets/650827e6-fc3b-4c96-a98e-e95dd7b099d9)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![370729934-45fd1def-c538-4673-8fd0-78f506447bc3](https://github.com/user-attachments/assets/9bf830bb-855f-4fdd-8555-6b3bb8c800ed)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
bench.py file1 file11 file2 file21 file22 file23 hello.c hello.js newfile readme.txt urllist.txt

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
-rw-r--r-- user/group 0 2024-02-25 14:30:00 file1.txt drwxr-xr-x user/group 0 2024-02-25 14:30:00 directory1/ -rw-r--r-- user/group 1024 2024-02-25 14:30:00 directory1/file2.txt -rw-r--r-- user/group 2048 2024-02-25 14:30:00 directory1/file3.txttar -xvf backup.tar
## OUTPUT

x file1.txt x directory1/ x directory1/file2.txt x directory1/file3.txt gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
backup.tar.gz gunzip backup.tar.gz
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![370731029-468990be-a1b5-486a-99f7-d1466f8267c2](https://github.com/user-attachments/assets/02f11359-238c-4714-b8dc-96de0bed3d11)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![370731102-cf71fe63-4fbb-45f5-b416-8278c7b4514a](https://github.com/user-attachments/assets/651302c5-13bc-4725-88bd-74ac95387106)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
## OUTPUT
![370732669-b35e55ac-0ee7-49cf-8bb5-b39020e5eceb](https://github.com/user-attachments/assets/1ac4f3ec-2574-4a0f-a580-c80246588dd1)

echo $?
## OUTPUT 

![370732875-142905b0-ad86-4c7f-8af5-9b19d9bf2edb](https://github.com/user-attachments/assets/81b916d5-031a-4ecc-b855-117cf0a81a7b)

./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
 1


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT


![370733663-a11a9d91-54b4-4487-9760-b15feb551665](https://github.com/user-attachments/assets/da5c22fd-2018-4acc-a0be-19f836421159)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
baseball is less than hockey
# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
You are the owner of the /etc/passwd file

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

![370734194-2ced2148-e58d-4e9f-b0fb-c02b65aa8f97](https://github.com/user-attachments/assets/ea744987-31e7-420e-ae5a-6a7ba619f4ef)


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![370734339-1e03c2e1-e4b1-4c5c-889c-dccfc86bce82](https://github.com/user-attachments/assets/ba4129e2-c8d1-4ab8-94ee-02ca59a4372d)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

![370734417-481d0481-1bc9-4e94-a03e-cdc91a7cbd6a](https://github.com/user-attachments/assets/9cf844d5-2c01-4081-afbb-6086badf7d37)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
Welcome Ram Please enjoy your visit Welcome Rahim Please enjoy your visit Special testing account gganesh, Do not forget to logout when you're done Sorry, you are not allowed here cat forinfile.sh 
```
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
1 - 5 2 - 4 3 - 3 4 - 2 5 - 1
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
Iteration number: 1 Iteration number: 2 The for loop is completed

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
Iteration number: 1 Iteration number: 2 Iteration number: 4 Iteration number: 5 The for loop is completed cat exread.sh
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
Enter your name: John Hello John, welcome to my program.

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
Enter your name: John Hello John, welcome to my program.

$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
total characters 75 Number of Lines are 10 No of Words count: 10
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
Enter the number 121 Number is palindrome Enter the number 69 Number is NOT palindrome


# RESULT:
The Commands are executed successfully.
