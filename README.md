# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# NAME   :GOPIKRISHNAN M
# REG NO :212223043001

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
## OUTPUT
cat < file1

<img width="975" height="210" alt="image" src="https://github.com/user-attachments/assets/be413c40-a8cf-444b-9b02-dce7353ff46e" />

## OUTPUT
cat < file2

<img width="980" height="243" alt="image" src="https://github.com/user-attachments/assets/0e6465b7-d7a2-4aa1-a282-651c44b4f7a1" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="980" height="105" alt="image" src="https://github.com/user-attachments/assets/1f437eb9-67ca-4931-bc51-5bfe2f99130f" />


comm file1 file2
 ## OUTPUT
 
<img width="975" height="308" alt="image" src="https://github.com/user-attachments/assets/442bedd9-f2b6-48b6-b676-84fe32e61d33" />

diff file1 file2
## OUTPUT

Hello world
This is my world
^d

# Filters

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

<img width="970" height="138" alt="image" src="https://github.com/user-attachments/assets/31433eb9-d73e-4d4a-b304-847541128977" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="975" height="173" alt="image" src="https://github.com/user-attachments/assets/b4b42357-9dec-4e4e-b5c1-0aac47600404" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="968" height="166" alt="image" src="https://github.com/user-attachments/assets/4030546d-fb10-48ae-a8bd-ce8e487dbeda" />


cat > newfile 
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

<img width="982" height="107" alt="image" src="https://github.com/user-attachments/assets/1d51095f-0a87-408f-82d5-5582749f7fda" />


grep hello newfile 
## OUTPUT

<img width="976" height="105" alt="image" src="https://github.com/user-attachments/assets/b817490b-0bc1-4c49-af53-fb615582be45" />



grep -v hello newfile 
## OUTPUT
<img width="968" height="101" alt="image" src="https://github.com/user-attachments/assets/bae67abb-e050-4ab2-b55d-9f801c6ed758" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="976" height="136" alt="image" src="https://github.com/user-attachments/assets/899c46be-6ff1-4f27-9dd0-fb2388426823" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="977" height="108" alt="image" src="https://github.com/user-attachments/assets/cd72d22d-3fc0-4be7-aae0-e55f5af8b05e" />



grep -R ubuntu /etc
## OUTPUT
<img width="1887" height="778" alt="image" src="https://github.com/user-attachments/assets/44e50e34-3f48-4531-96a4-231d286e1464" />


grep -w -n world newfile   
## OUTPUT
<img width="1030" height="140" alt="image" src="https://github.com/user-attachments/assets/7e41f000-6851-4966-bc01-0950e1db830a" />

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
<img width="977" height="139" alt="image" src="https://github.com/user-attachments/assets/47872ea2-b686-4a7c-9c65-f2f30b351233" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="977" height="138" alt="image" src="https://github.com/user-attachments/assets/a4ed9eab-d2f8-48d7-9cf7-13b65f445c7f" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="970" height="137" alt="image" src="https://github.com/user-attachments/assets/815f77f4-4a6e-4d6b-9493-2b67976e3e91" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="973" height="103" alt="image" src="https://github.com/user-attachments/assets/63b9bf3c-6f7c-4539-a4c8-2861d9f48c23" />


egrep '(world$)' newfile 
## OUTPUT
<img width="973" height="138" alt="image" src="https://github.com/user-attachments/assets/3376180c-c4f5-4d52-a973-2fcdbab02390" />


egrep '(World$)' newfile 
## OUTPUT
<img width="968" height="99" alt="image" src="https://github.com/user-attachments/assets/32f60645-25e6-43cf-a386-1bcf09de2805" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="977" height="170" alt="image" src="https://github.com/user-attachments/assets/bf889e18-2c89-4e95-a631-39ce9ebb2206" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="985" height="105" alt="image" src="https://github.com/user-attachments/assets/93d7f324-b7e6-4cc7-a5ea-6133a7d31640" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="972" height="100" alt="image" src="https://github.com/user-attachments/assets/9c60e1a0-3830-424b-af0e-d1d5ba41766a" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="972" height="104" alt="image" src="https://github.com/user-attachments/assets/923482be-3a64-4cfd-897a-c7adfd4868ea" />


egrep l{2} newfile
## OUTPUT
<img width="976" height="140" alt="image" src="https://github.com/user-attachments/assets/6893aa32-a9ee-4c05-8f14-dee672349340" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="968" height="164" alt="image" src="https://github.com/user-attachments/assets/4c0ee6a4-174f-4d11-8440-90a3abe48608" />

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
<img width="967" height="104" alt="image" src="https://github.com/user-attachments/assets/8ba1a9e6-03dc-4ea6-b3c4-69dc1d63d22f" />


sed -n -e '$p' file23
## OUTPUT
<img width="982" height="99" alt="image" src="https://github.com/user-attachments/assets/04ee7fd0-b1d6-4c3a-80ea-4060c7b32cc6" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="970" height="339" alt="image" src="https://github.com/user-attachments/assets/ff56c1b3-9009-4d03-a887-1ff82cef86dc" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="975" height="335" alt="image" src="https://github.com/user-attachments/assets/0300898a-2bf9-4003-9095-b775cee1e8cc" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="970" height="345" alt="image" src="https://github.com/user-attachments/assets/458b5480-75b8-429c-a768-8ff5ad39606a" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="977" height="247" alt="image" src="https://github.com/user-attachments/assets/91c87d31-17fe-4443-9eb0-acd9e1705194" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="982" height="170" alt="image" src="https://github.com/user-attachments/assets/4ab9d714-f404-4d93-b192-5bcd3032e5d4" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="976" height="135" alt="image" src="https://github.com/user-attachments/assets/28555876-bf1e-41fe-a0e1-a6bc64c1ad29" />


seq 10 
## OUTPUT
<img width="980" height="410" alt="image" src="https://github.com/user-attachments/assets/133dc72e-0c9b-49f3-be3f-3731afe63ea1" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="971" height="172" alt="image" src="https://github.com/user-attachments/assets/deefe207-6bed-4da0-8e4b-2139f2c77ed6" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="977" height="173" alt="image" src="https://github.com/user-attachments/assets/ff4ee21f-3af8-4dd7-b82b-0ca4cac52e8a" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="991" height="202" alt="image" src="https://github.com/user-attachments/assets/9a952769-1e04-43cb-b46f-6a903e760f91" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="991" height="202" alt="image" src="https://github.com/user-attachments/assets/fb34c901-b80f-4519-a2df-f39d403debfa" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="976" height="165" alt="image" src="https://github.com/user-attachments/assets/d41334e9-91bf-45d7-b692-def83df4e59a" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="977" height="170" alt="image" src="https://github.com/user-attachments/assets/9de0bd00-54b6-49aa-9f70-76239a14f765" />


sed -n '2,4{s/$/*/;p}' file23
<img width="986" height="172" alt="image" src="https://github.com/user-attachments/assets/6b1356f3-d487-4497-9804-89c37fb1102e" />

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
<img width="972" height="238" alt="image" src="https://github.com/user-attachments/assets/9e3533b6-6f4a-4100-8afd-614e6152499f" />

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
<img width="971" height="239" alt="image" src="https://github.com/user-attachments/assets/c729996f-4ed2-4979-b757-119c2980db4e" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="978" height="341" alt="image" src="https://github.com/user-attachments/assets/d4c34022-21c7-452f-8411-8173c1205e7a" />
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
<img width="983" height="179" alt="image" src="https://github.com/user-attachments/assets/3d32303e-7d51-4f98-9cc9-3a281c2cb61a" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="973" height="170" alt="image" src="https://github.com/user-attachments/assets/95a24f22-9e75-4f3d-800e-ab435d10f653" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="973" height="339" alt="image" src="https://github.com/user-attachments/assets/f5ac9690-9849-4e38-9225-8bdf07b592ae" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1112" height="341" alt="image" src="https://github.com/user-attachments/assets/f26b8334-f5a2-4b4a-8472-ba7b8008d40c" />


tar -xvf backup.tar
## OUTPUT
<img width="1115" height="343" alt="image" src="https://github.com/user-attachments/assets/f0503e8d-82be-4f5e-89fa-8eca0b9fb07a" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="1115" height="95" alt="image" src="https://github.com/user-attachments/assets/54d10b17-bd8a-43dc-a57d-5f92f63eb4b5" />

gunzip backup.tar.gz
## OUTPUT

 <img width="1115" height="99" alt="image" src="https://github.com/user-attachments/assets/6bbcf359-84e2-41be-b559-0a202a089870" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="973" height="138" alt="image" src="https://github.com/user-attachments/assets/b3214290-269e-4fb5-b244-8f9dcc4534f0" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="970" height="205" alt="image" src="https://github.com/user-attachments/assets/88880aaf-98b5-45b5-98cc-72d13ec15d3e" />


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
<img width="977" height="542" alt="image" src="https://github.com/user-attachments/assets/5a917166-25f3-4224-adc7-726d83dbae54" />

 
ls file1
## OUTPUT
<img width="966" height="96" alt="image" src="https://github.com/user-attachments/assets/4b56564e-a400-487a-857f-d1322697b420" />


echo $?
## OUTPUT 
<img width="975" height="103" alt="image" src="https://github.com/user-attachments/assets/ccc8d50c-8e17-4ad5-b86e-5420e2b211c9" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="1022" height="105" alt="image" src="https://github.com/user-attachments/assets/f6d2fd80-16e5-450f-bba1-5386fc9ceef1" />

abcd

 
echo $?
 ## OUTPUT
<img width="1022" height="105" alt="image" src="https://github.com/user-attachments/assets/5b27426d-b5f0-4e9d-be99-4b71c4dba5b2" />

 
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
<img width="972" height="369" alt="image" src="https://github.com/user-attachments/assets/7051b948-e3e3-4459-8f1a-1db1c73d413a" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="971" height="91" alt="image" src="https://github.com/user-attachments/assets/85d64e76-b797-4299-ae6d-792f41585194" />

# check file ownership
cat > psswdperm.sh 
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
<img width="975" height="105" alt="image" src="https://github.com/user-attachments/assets/217d7e3e-cf7e-4645-9a66-eb7017743439" />
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

./ifnested.sh 
## OUTPUT
<img width="978" height="176" alt="image" src="https://github.com/user-attachments/assets/a4c0783e-00be-4b2a-bcf1-1e1978e4862c" />


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
<img width="970" height="143" alt="image" src="https://github.com/user-attachments/assets/83b7c2e7-7281-4209-8b15-a762670ff770" />
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
<img width="982" height="174" alt="image" src="https://github.com/user-attachments/assets/1d54071b-5630-40e6-a833-b3bb4ab34d36" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = kabe ]
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
<img width="970" height="138" alt="image" src="https://github.com/user-attachments/assets/b983c0bd-0beb-4d32-9997-735981d9f735" />

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
<img width="973" height="105" alt="image" src="https://github.com/user-attachments/assets/556e92af-d936-40d5-b7d4-29ade67a6fa2" />


# using the case command
cat >casecheck.sh 
```bash
case $USER in
kabe | Kabe)
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
## OUTPUT 
<img width="972" height="135" alt="image" src="https://github.com/user-attachments/assets/76b43220-693a-4acb-8388-320c924fea39" />
cat > whiletest.sh
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
## OUTPUT 
<img width="975" height="413" alt="image" src="https://github.com/user-attachments/assets/7b347912-ed94-4e40-ba14-03b51c0a173f" />

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
 
 ./utiltest.sh
 ## Output
<img width="967" height="210" alt="image" src="https://github.com/user-attachments/assets/c9e8240b-7c82-475e-bba6-418073cc3620" />
 
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
 
./forin1.sh

## Output
<img width="972" height="274" alt="image" src="https://github.com/user-attachments/assets/aca99c88-acbb-4c63-b2e7-20eb2fe47529" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```

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

## Output
<img width="978" height="172" alt="image" src="https://github.com/user-attachments/assets/87bad215-cd1c-4671-b109-92d340417dc6" />

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

## Output
<img width="985" height="276" alt="image" src="https://github.com/user-attachments/assets/0eca1eaf-e20d-4775-b102-72c3ba1122eb" />


cat forinfile.sh 
```bash
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
<img width="986" height="308" alt="image" src="https://github.com/user-attachments/assets/9ffbbce3-4bf0-437b-b281-49a4b290fb3b" />

cat forctype.sh 
```bash
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
<img width="977" height="236" alt="image" src="https://github.com/user-attachments/assets/61ae7eb4-784e-4552-a26b-e967353386c0" />
cat forctype1.sh 
```bash
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
<img width="980" height="240" alt="image" src="https://github.com/user-attachments/assets/9d3421f0-9f85-469a-afbd-c678e8933692" />
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
<img width="977" height="473" alt="image" src="https://github.com/user-attachments/assets/efd7f924-676d-4ed5-b46d-a61cbc7f5ae8" />
 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## Output
<img width="982" height="176" alt="image" src="https://github.com/user-attachments/assets/14cc6101-d4cd-43eb-9d1a-dd0b0a966084" />
 
cat forcontinue.sh 
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
cat exread.sh 
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
<img width="982" height="136" alt="image" src="https://github.com/user-attachments/assets/c127cb33-f361-415a-9bdd-90abbad290d5" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh

## OUTPUT
<img width="982" height="135" alt="image" src="https://github.com/user-attachments/assets/621609b5-7f52-4da5-b3f1-66e8db61d090" />

 
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
 <img width="972" height="104" alt="image" src="https://github.com/user-attachments/assets/4cf7d85d-7e01-4a69-ab8e-7a93323c813e" />

 ./funcex.sh 1 2
 <img width="976" height="99" alt="image" src="https://github.com/user-attachments/assets/d04bf105-6cf8-41d0-9344-f1ecb3ddf784" />

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
$ chmod 777 argshift1.sh
## OUTPUT
$ ./argshift1.sh 1 2 3
<img width="974" height="174" alt="image" src="https://github.com/user-attachments/assets/f9510785-97ab-4319-8f88-de8e2daabbeb" />

cat > argshift.sh
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
<img width="973" height="549" alt="image" src="https://github.com/user-attachments/assets/3ce3384b-acb6-4d6a-9bbb-407f9229d9c1" />
 
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
<img width="972" height="513" alt="image" src="https://github.com/user-attachments/assets/c02989de-a7ce-43f8-8e24-dc3478fc7370" />

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
<img width="988" height="339" alt="image" src="https://github.com/user-attachments/assets/3e4cb11a-9b85-4cd0-87e3-d1ad8f75da80" />

# RESULT:
The Commands are executed successfully.
