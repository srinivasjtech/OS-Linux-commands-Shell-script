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
<img width="664" height="152" alt="image" src="https://github.com/user-attachments/assets/c3584357-6304-435c-80e5-7d67ade36de7" />


cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
<img width="647" height="174" alt="image" src="https://github.com/user-attachments/assets/10471781-8110-455e-a522-ae03eb32ee3c" />


### Display the content of the files
cat < file1
## OUTPUT

<img width="887" height="153" alt="image" src="https://github.com/user-attachments/assets/06042f3f-1c6e-4e60-8a1b-8117f6dbbf61" />


cat < file2
## OUTPUT

<img width="655" height="178" alt="image" src="https://github.com/user-attachments/assets/85dace45-3ae3-44c7-b06f-88ef4b1f9d12" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="671" height="89" alt="image" src="https://github.com/user-attachments/assets/c48810e1-e349-45fb-965e-bfff304e9a00" />

comm file1 file2
 ## OUTPUT
<img width="753" height="230" alt="image" src="https://github.com/user-attachments/assets/d0757167-bb1b-4585-b9ad-e90fcb211a40" />

 
diff file1 file2
## OUTPUT

<img width="704" height="270" alt="image" src="https://github.com/user-attachments/assets/47f1af51-3f71-4afb-9e67-4a93a558208a" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
<img width="683" height="108" alt="image" src="https://github.com/user-attachments/assets/6f0962a7-ee1e-4099-be89-04f38f02b7fd" />


cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```

<img width="646" height="138" alt="image" src="https://github.com/user-attachments/assets/52b1160e-fccf-4c60-b61c-dcc1b6d8a101" />


cut -c1-3 file11
## OUTPUT


<img width="679" height="101" alt="image" src="https://github.com/user-attachments/assets/a0a99cf3-ba52-493e-9efc-6eb76cf5a610" />



cut -d "|" -f 1 file22
## OUTPUT


<img width="666" height="123" alt="image" src="https://github.com/user-attachments/assets/74a73f75-20f1-479e-86d9-febd71139309" />


cut -d "|" -f 2 file22
## OUTPUT


<img width="668" height="130" alt="image" src="https://github.com/user-attachments/assets/151d2be7-8a7e-460a-aa1c-1e2070c00e59" />


cat > newfile 
```
Hello world
hello world
^d
````

<img width="673" height="100" alt="image" src="https://github.com/user-attachments/assets/d7fc367c-7adc-4ac2-95da-598f2cd00974" />


cat < newfile 
Hello world
hello world


<img width="639" height="98" alt="image" src="https://github.com/user-attachments/assets/483a3143-b181-45ef-8549-0270c4cef223" />

 
grep Hello newfile 
## OUTPUT


<img width="639" height="85" alt="image" src="https://github.com/user-attachments/assets/09b8450f-3720-4bbc-85c5-61d4a4d2b70d" />


grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT


<img width="639" height="85" alt="image" src="https://github.com/user-attachments/assets/f15e0e36-8dad-4f3c-a618-ac152f764111" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="679" height="104" alt="image" src="https://github.com/user-attachments/assets/ae6cc61b-6f18-4bf8-8a92-95fecd92d5cc" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="635" height="90" alt="image" src="https://github.com/user-attachments/assets/05635216-ea67-46c6-954e-d5032fcc698c" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT


<img width="725" height="104" alt="image" src="https://github.com/user-attachments/assets/47b2e885-3a95-4a0e-83ce-2a933e4f8ed3" />


cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```


<img width="660" height="174" alt="image" src="https://github.com/user-attachments/assets/9c5da880-5ac2-4545-b64e-e2874a557e8c" />


cat < newfile
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


<img width="660" height="107" alt="image" src="https://github.com/user-attachments/assets/50e0777f-a1b8-4212-bd7a-09971eb3263f" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="660" height="130" alt="image" src="https://github.com/user-attachments/assets/6038efcd-65f3-4c18-8e1d-8a68d0ed13d6" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="660" height="129" alt="image" src="https://github.com/user-attachments/assets/131906a4-069e-44d7-93a8-418e153f6eec" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="660" height="99" alt="image" src="https://github.com/user-attachments/assets/5e51ea2f-0a75-4d04-9360-dac013ec2ae6" />


egrep '(world$)' newfile 
## OUTPUT


<img width="660" height="128" alt="image" src="https://github.com/user-attachments/assets/b9233b6d-966f-4ba8-8508-7b92f2d1f474" />


egrep '(World$)' newfile 
## OUTPUT


<img width="646" height="106" alt="image" src="https://github.com/user-attachments/assets/7b07d5a3-6f72-4426-aabd-64eeabf78d4c" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="646" height="149" alt="image" src="https://github.com/user-attachments/assets/823cc1f0-7aaf-4d1c-beeb-aadcd25de13d" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="646" height="107" alt="image" src="https://github.com/user-attachments/assets/4231efe5-7b5e-42b8-a692-e011f903c240" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="646" height="104" alt="image" src="https://github.com/user-attachments/assets/6c277792-62bd-412d-abc3-879e0aa18208" />


egrep 'Linux.*World' newfile 
## OUTPUT


<img width="646" height="95" alt="image" src="https://github.com/user-attachments/assets/4306e7f5-5bfe-4999-8508-4df962c30b51" />


egrep l{2} newfile
## OUTPUT


<img width="685" height="122" alt="image" src="https://github.com/user-attachments/assets/007dfba2-ccd7-4783-890d-5bb4292a9fdf" />


egrep 's{1,2}' newfile
## OUTPUT 


<img width="685" height="147" alt="image" src="https://github.com/user-attachments/assets/ad242e63-6d7e-46b5-a173-46f54be71134" />


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


<img width="685" height="278" alt="image" src="https://github.com/user-attachments/assets/beb97f27-772b-43dd-9ebe-2d3aacb13fa2" />


sed -n -e '3p' file23
## OUTPUT


<img width="685" height="101" alt="image" src="https://github.com/user-attachments/assets/d67dee19-2d04-47a9-a880-3dc5fef52414" />


sed -n -e '$p' file23
## OUTPUT


<img width="685" height="101" alt="image" src="https://github.com/user-attachments/assets/d1d5ac1d-2d0c-47af-8cfe-4f8181326169" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="717" height="282" alt="image" src="https://github.com/user-attachments/assets/71c27fcb-aabe-4e64-b144-c53800e575b7" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="717" height="276" alt="image" src="https://github.com/user-attachments/assets/faceab16-2755-4096-bc3c-5655e9ffc431" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="717" height="273" alt="image" src="https://github.com/user-attachments/assets/b6d76b00-4a03-451b-ab17-2b2968f9e3e0" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="733" height="201" alt="image" src="https://github.com/user-attachments/assets/37284c76-6d5c-40d2-8e2b-6f23ed5aa803" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="733" height="153" alt="image" src="https://github.com/user-attachments/assets/fdd7ac49-6a02-4a0c-aa4d-c56ae652cec1" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="733" height="121" alt="image" src="https://github.com/user-attachments/assets/46b3e31e-b710-4624-b09e-a8449d310947" />


seq 10 
## OUTPUT


<img width="733" height="328" alt="image" src="https://github.com/user-attachments/assets/24f3fc3b-1cfc-4a9d-af70-92def495b088" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="750" height="156" alt="image" src="https://github.com/user-attachments/assets/237b22af-e0ca-4960-a758-7fa15ae0d680" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="750" height="155" alt="image" src="https://github.com/user-attachments/assets/aed62ba2-fdd1-4464-a22b-922f3fe0bfae" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="750" height="171" alt="image" src="https://github.com/user-attachments/assets/7a0f0ec8-0050-4d5a-93c9-ffe7bf6c3efd" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="750" height="159" alt="image" src="https://github.com/user-attachments/assets/51430489-cb23-4125-9f1b-a5e62a192174" />


seq 10 | sed '2,9c hello'
## OUTPUT


<img width="750" height="146" alt="image" src="https://github.com/user-attachments/assets/75bc733a-c6e5-4f4f-b755-d878fddb1556" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="826" height="144" alt="image" src="https://github.com/user-attachments/assets/668be81d-df4d-4946-9d7e-f015b8533cd7" />


sed -n '2,4{s/$/*/;p}' file23


<img width="826" height="147" alt="image" src="https://github.com/user-attachments/assets/2bc1040d-9f28-4a43-a90c-2334f97a033e" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```


<img width="473" height="181" alt="image" src="https://github.com/user-attachments/assets/992f59db-02fc-42ef-b612-d6e12731dd24" />


sort file21
## OUTPUT


<img width="473" height="147" alt="image" src="https://github.com/user-attachments/assets/dd4445ef-0342-4fff-ad16-53863c22a466" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```


<img width="855" height="219" alt="image" src="https://github.com/user-attachments/assets/7f019cf2-9fe9-49df-afab-35e7b5734004" />


uniq file22
## OUTPUT


<img width="855" height="205" alt="image" src="https://github.com/user-attachments/assets/aeddb07e-3f8b-4335-9fde-212585c6a4e1" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT


<img width="855" height="279" alt="image" src="https://github.com/user-attachments/assets/01362079-cd4e-4752-884d-cf96dc416a98" />


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```

<img width="829" height="177" alt="image" src="https://github.com/user-attachments/assets/789ce019-dafc-4fd3-99c1-434c0e6adddd" />


cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT


<img width="829" height="174" alt="image" src="https://github.com/user-attachments/assets/6ff05ffb-92ca-439e-903c-e5047ab0a97b" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="829" height="167" alt="image" src="https://github.com/user-attachments/assets/566def17-8324-45ee-8722-36755b1aa22c" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="922" height="296" alt="image" src="https://github.com/user-attachments/assets/53d80124-d692-4961-bc6d-9c69b525a72f" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="922" height="337" alt="image" src="https://github.com/user-attachments/assets/f31127c7-a617-4f30-b49b-2c3eba78438b" />


tar -xvf backup.tar
## OUTPUT


<img width="892" height="324" alt="image" src="https://github.com/user-attachments/assets/f00d8f64-baee-4ed6-8a78-d8c9f2e54ff8" />


gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```


<img width="833" height="169" alt="image" src="https://github.com/user-attachments/assets/55c8de3f-daf4-497a-be2a-ef4f84eaa31c" />


cat herecheck.txt
## OUTPUT





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


<img width="799" height="350" alt="image" src="https://github.com/user-attachments/assets/3abdb3ab-8391-4e35-ad00-c79d32219165" />


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


<img width="799" height="352" alt="image" src="https://github.com/user-attachments/assets/0cf31856-721a-45d6-8376-fab93d11a884" />

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT


<img width="861" height="415" alt="image" src="https://github.com/user-attachments/assets/0ec460a3-dba2-43b2-82da-1093240dd8fe" />

 
ls file1
## OUTPUT


<img width="861" height="115" alt="image" src="https://github.com/user-attachments/assets/7a7d4f9a-5478-4154-948c-ecd17fdb1a3b" />


echo $?
## OUTPUT 


<img width="861" height="116" alt="image" src="https://github.com/user-attachments/assets/fa4485db-67c8-40e3-81c5-1cdb3229361f" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 


<img width="797" height="106" alt="image" src="https://github.com/user-attachments/assets/36eff5de-098e-4dfa-bd02-84d85371bc01" />

 
abcd
 
echo $?
 ## OUTPUT


<img width="797" height="106" alt="image" src="https://github.com/user-attachments/assets/b9f38ffc-812f-43b5-a1e4-50d57b59c8fb" />

 
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


<img width="797" height="270" alt="image" src="https://github.com/user-attachments/assets/549b36ce-d0e0-4809-949e-78a24798207a" />


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


<img width="797" height="303" alt="image" src="https://github.com/user-attachments/assets/9b2dbd0d-7d44-4dff-84cd-b323d5315056" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


<img width="819" height="127" alt="image" src="https://github.com/user-attachments/assets/76b6c1f6-e3e0-4464-93f6-4c9504c0d976" />


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


<img width="819" height="221" alt="image" src="https://github.com/user-attachments/assets/e40d15f7-d047-47dd-a7cf-f0cfabf5fd11" />


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


<img width="819" height="245" alt="image" src="https://github.com/user-attachments/assets/47ab33f3-7d4b-4c87-a4eb-3f767f0f0197" />


./psswdperm.sh
## OUTPUT



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

<img width="937" height="506" alt="Screenshot 2026-04-25 141824" src="https://github.com/user-attachments/assets/beb15034-fc7a-4596-96d4-efde90c8ddb9" />


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


<img width="891" height="500" alt="image" src="https://github.com/user-attachments/assets/c0608a3d-b9d2-44cf-b7ae-a13e5572d23e" />


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

<img width="805" height="405" alt="image" src="https://github.com/user-attachments/assets/c6a1875c-c86f-4a50-94db-4fc31b641da5" />

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

<img width="805" height="395" alt="image" src="https://github.com/user-attachments/assets/82f410af-a042-4ea6-bc82-86ffec63a490" />


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

<img width="846" height="497" alt="image" src="https://github.com/user-attachments/assets/9b8bce28-5031-4bf1-8dbf-03306b4c35bc" />


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

<img width="774" height="506" alt="image" src="https://github.com/user-attachments/assets/474c9a54-07ef-496d-9d07-139fde7479f2" />


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

<img width="843" height="112" alt="image" src="https://github.com/user-attachments/assets/9ba9494a-b7eb-4a28-961e-a488633286d1" />


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

<img width="843" height="256" alt="image" src="https://github.com/user-attachments/assets/3dba22bf-6060-4e53-a9b5-26eb0ec73099" />


$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

<img width="889" height="118" alt="image" src="https://github.com/user-attachments/assets/15d4232e-6850-4c38-a2e2-a3d5dde81707" />


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

<img width="889" height="351" alt="image" src="https://github.com/user-attachments/assets/4c29dfb8-93bb-43f7-89cd-479a857d5642" />


$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 

<img width="889" height="128" alt="image" src="https://github.com/user-attachments/assets/d05ba062-6cca-4b71-a568-dede6f840c9f" />

 
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

<img width="793" height="271" alt="image" src="https://github.com/user-attachments/assets/f910777f-b39b-4bfb-81fc-63a5b18a47c7" />


$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

 <img width="758" height="342" alt="image" src="https://github.com/user-attachments/assets/9395c5b1-aebd-44fa-89db-57d50ce6d51b" />

 
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

<img width="837" height="231" alt="image" src="https://github.com/user-attachments/assets/cd34255a-bfb6-4c0f-84de-f8178009a06b" />

 
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

<img width="713" height="96" alt="image" src="https://github.com/user-attachments/assets/195d079b-5b59-4637-925c-25f436c01bf9" />


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

<img width="713" height="225" alt="image" src="https://github.com/user-attachments/assets/adf17eea-c1eb-4396-9be7-1d0575e7a0f2" />


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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.
