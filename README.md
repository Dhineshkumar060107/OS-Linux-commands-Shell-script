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
<img width="436" height="155" alt="cat-1" src="https://github.com/user-attachments/assets/0c425724-b513-4a96-88a5-af6a5f29a896" />



cat < file2
## OUTPUT
<img width="385" height="183" alt="2" src="https://github.com/user-attachments/assets/1646bed6-a0c7-417c-b116-9daa57959320" />


# Comparing Files
cmp file1 file2
## OUTPUT 
<img width="375" height="71" alt="3" src="https://github.com/user-attachments/assets/3a8e3e83-e1b4-42e4-bba2-066856ab510e" />

 
comm file1 file2
 ## OUTPUT
 
<img width="452" height="220" alt="4" src="https://github.com/user-attachments/assets/fc9b339b-9b94-48f9-9689-2ce5ae360ef1" />

 
diff file1 file2
## OUTPUT
<img width="384" height="274" alt="5" src="https://github.com/user-attachments/assets/bbe54325-c2e2-48d0-9771-08c53ef9cb8a" />


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

<img width="383" height="98" alt="7" src="https://github.com/user-attachments/assets/30558e3f-011f-487f-b5a0-4bb356f3d368" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="413" height="127" alt="8" src="https://github.com/user-attachments/assets/bb07c3e3-6f92-4ed8-a64b-e2bc03859e4a" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="413" height="127" alt="8" src="https://github.com/user-attachments/assets/e8987a27-add8-40fa-b13d-93b9888c2f90" />


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

<img width="445" height="73" alt="11" src="https://github.com/user-attachments/assets/253144d7-cec6-4477-aa00-39b1b0fec161" />


grep hello newfile 
## OUTPUT

<img width="445" height="73" alt="11" src="https://github.com/user-attachments/assets/0d374e23-a204-4317-8ea4-5c3d5567cbd9" />



grep -v hello newfile 
## OUTPUT

<img width="376" height="78" alt="12" src="https://github.com/user-attachments/assets/220d0c08-0685-4365-bb34-11684e95659c" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="380" height="107" alt="13" src="https://github.com/user-attachments/assets/ec206c14-ac35-4652-a8a4-37e4ba9baeb7" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="465" height="75" alt="17" src="https://github.com/user-attachments/assets/ac9e5702-9d9d-4680-ab09-6c32a55276c9" />




grep -R ubuntu /etc
## OUTPUT


<img width="884" height="862" alt="18" src="https://github.com/user-attachments/assets/daac427e-01f3-4e94-9a32-966cd49181d2" />


grep -w -n world newfile   
## OUTPUT
<img width="486" height="96" alt="19" src="https://github.com/user-attachments/assets/dbc5c3d8-8547-495d-bc64-18bf15f0ff2c" />


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

<img width="442" height="101" alt="21" src="https://github.com/user-attachments/assets/21a1b2b6-c570-4aa6-a839-561aec92551a" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="463" height="106" alt="22" src="https://github.com/user-attachments/assets/1a2b233e-2b8b-4580-ba06-66c023ec59d6" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="431" height="73" alt="23" src="https://github.com/user-attachments/assets/b4d77b5d-b0b0-4c04-a9f7-bead8923c72a" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="431" height="73" alt="23" src="https://github.com/user-attachments/assets/fc7cced1-3916-46b9-a8f5-8f6446b582f7" />



egrep '(world$)' newfile 
## OUTPUT

<img width="412" height="100" alt="24" src="https://github.com/user-attachments/assets/d1200c85-f708-4729-bcd8-5259161d334f" />


egrep '(World$)' newfile 
## OUTPUT
<img width="360" height="74" alt="25" src="https://github.com/user-attachments/assets/1e404359-68a3-4511-89e6-d84e5a5bb55b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="412" height="90" alt="26" src="https://github.com/user-attachments/assets/a9a16e2a-048f-4367-ab59-e57d6782fb1d" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="391" height="81" alt="27" src="https://github.com/user-attachments/assets/06277339-ad57-4a9b-9e89-e02c831f0728" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="392" height="75" alt="28" src="https://github.com/user-attachments/assets/66468e68-2e4d-4926-be72-fcf6ea97efed" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="410" height="77" alt="29" src="https://github.com/user-attachments/assets/e1d9ade2-6933-4d08-a894-97e1358d4b7e" />


egrep l{2} newfile
## OUTPUT

<img width="393" height="95" alt="30" src="https://github.com/user-attachments/assets/e4b1d3a3-a08b-4968-bfb7-3200b554a478" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="469" height="135" alt="31" src="https://github.com/user-attachments/assets/7a2df19d-6ece-46db-b1cf-5bff2b267c15" />


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

<img width="448" height="75" alt="33" src="https://github.com/user-attachments/assets/e68d1515-0169-4a3f-a0cd-5b2d073ef264" />


sed -n -e '$p' file23
## OUTPUT
<img width="440" height="85" alt="34" src="https://github.com/user-attachments/assets/39154d09-fc7e-43ee-bdc4-9451784e30a9" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="495" height="250" alt="35" src="https://github.com/user-attachments/assets/e66c438e-6d57-4506-aa44-b6740b273fe9" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="430" height="254" alt="36" src="https://github.com/user-attachments/assets/8dfacb30-8773-4e31-be7a-54dc1f354484" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="484" height="245" alt="37" src="https://github.com/user-attachments/assets/c90c7147-58cd-4ac1-a2fa-c51577fe3863" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="448" height="187" alt="38" src="https://github.com/user-attachments/assets/fe36021f-d6db-4020-9cb4-15536ccbf6b1" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="439" height="122" alt="39" src="https://github.com/user-attachments/assets/9dae0c75-4963-4921-97fd-3db851f687b4" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="441" height="100" alt="40" src="https://github.com/user-attachments/assets/632cbb05-aa50-4639-9b47-5faaf8525d75" />


seq 10 
## OUTPUT

<img width="489" height="299" alt="41" src="https://github.com/user-attachments/assets/73c89e2a-c6c2-4cb4-a23f-f26417d40d20" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="405" height="130" alt="42" src="https://github.com/user-attachments/assets/c50a11c4-5708-4651-bf74-c082a32b7750" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="458" height="124" alt="43" src="https://github.com/user-attachments/assets/43f8bdd3-47c7-4a68-91e4-e8aefb4d6bb1" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="424" height="150" alt="44" src="https://github.com/user-attachments/assets/4e8c6079-3a0c-4db0-9590-fc1290a9e672" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="504" height="124" alt="45" src="https://github.com/user-attachments/assets/751fdb0d-9f94-4045-a84c-b8cb9d81bff2" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="414" height="120" alt="46" src="https://github.com/user-attachments/assets/a6cfa133-7fba-4e09-9b60-41cb9b0b49a6" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="426" height="124" alt="47" src="https://github.com/user-attachments/assets/c0cccfe9-a97e-4279-88a9-3d9fcae79cb1" />


sed -n '2,4{s/$/*/;p}' file23

<img width="520" height="133" alt="48" src="https://github.com/user-attachments/assets/aceefd68-09e3-44ce-88f3-9a28d04c9cbf" />

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
<img width="479" height="176" alt="50" src="https://github.com/user-attachments/assets/481a64e8-39e9-4ec7-a93d-076629604aca" />


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

<img width="443" height="150" alt="51" src="https://github.com/user-attachments/assets/e3036bbe-4f44-4b6b-a76c-37be1fa69db3" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="519" height="254" alt="52" src="https://github.com/user-attachments/assets/2b84119f-c75b-4293-aee6-a917467b17bc" />

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

<img width="495" height="120" alt="53" src="https://github.com/user-attachments/assets/36280e49-6b9d-4f5f-bf84-b650a46ce830" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="532" height="115" alt="54" src="https://github.com/user-attachments/assets/04edb863-d80d-4a4a-9695-437743a936de" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="801" height="930" alt="55" src="https://github.com/user-attachments/assets/0cccfda0-f47c-4611-a434-ef95e36111ba" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="700" height="284" alt="56" src="https://github.com/user-attachments/assets/564b61f0-0c82-4e8c-986a-97773e189a8f" />


tar -xvf backup.tar
## OUTPUT
<img width="813" height="780" alt="57" src="https://github.com/user-attachments/assets/32516103-c0dd-49a5-ae11-507971b4d58d" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="606" height="43" alt="58" src="https://github.com/user-attachments/assets/15530e30-0969-4b94-ac5c-08ebae0b2e7a" />

gunzip backup.tar.gz
## OUTPUT
<img width="565" height="69" alt="59" src="https://github.com/user-attachments/assets/9a03edef-5c97-4130-a8a4-33901d5369a8" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="425" height="170" alt="60" src="https://github.com/user-attachments/assets/22ce64d4-b663-4489-9bfc-9b3c34da3417" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="528" height="126" alt="61" src="https://github.com/user-attachments/assets/fc7e200e-3209-4f85-b0a1-956acbab72dd" />


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
<img width="741" height="406" alt="64" src="https://github.com/user-attachments/assets/67ec2a4f-4bc3-4e2e-8579-e261af2b12bd" />

 
ls file1
## OUTPUT
<img width="473" height="80" alt="66" src="https://github.com/user-attachments/assets/5e124983-3d35-49e4-beda-31e883ebf9f7" />

echo $?
## OUTPUT
<img width="431" height="86" alt="67" src="https://github.com/user-attachments/assets/8e0624a5-5529-4e3e-91d7-3e708cf201fc" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="467" height="78" alt="68" src="https://github.com/user-attachments/assets/57ad79d1-d0b2-456c-aaef-798255a488d2" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="464" height="75" alt="69" src="https://github.com/user-attachments/assets/a3c8785e-5499-4a2f-9a1a-ce6263a6ecc3" />

 
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
<img width="538" height="278" alt="70" src="https://github.com/user-attachments/assets/8f14fb58-b2c8-48e7-ba31-feecbd858f04" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="538" height="278" alt="70" src="https://github.com/user-attachments/assets/564496a9-1867-4ddb-9da5-b9742e1f4908" />


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
<img width="645" height="230" alt="71" src="https://github.com/user-attachments/assets/6dd1a740-9603-4a37-ad24-a5b9620cde9b" />
<img width="500" height="102" alt="72" src="https://github.com/user-attachments/assets/64071945-772c-48d0-ab54-362b9f6dad80" />

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

<img width="490" height="570" alt="74" src="https://github.com/user-attachments/assets/27c75cef-ad99-4545-89b0-23cfe2695182" />

<img width="550" height="361" alt="75" src="https://github.com/user-attachments/assets/80725f2c-38d2-4e6b-b5b5-f4ae609daacd" />



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
<img width="716" height="520" alt="77" src="https://github.com/user-attachments/assets/955aa738-c4d8-4c8c-9d70-03bda242219d" />

<img width="526" height="473" alt="76" src="https://github.com/user-attachments/assets/1fb3a0c4-85d9-4733-900b-20650bc6b4d5" />

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
<img width="436" height="155" alt="cat-1" src="https://github.com/user-attachments/assets/00b7d636-193c-4113-8818-ac78f8cdb252" />
<img width="448" height="118" alt="380" src="https://github.com/user-attachments/assets/b00fd7f6-d1ba-4511-ac28-fd13d13bb1c4" />
<img width="576" height="392" alt="93" src="https://github.com/user-attachments/assets/29b410ce-1f82-4d54-b226-76282b49285a" />
<img width="498" height="362" alt="91" src="https://github.com/user-attachments/assets/bd6d05b7-b084-43b3-9f04-8ec6f47c3169" />
<img width="463" height="131" alt="90" src="https://github.com/user-attachments/assets/a4e0c9b1-e53a-46ff-9c5a-2e6e05e2dbe2" />
<img width="763" height="175" alt="87" src="https://github.com/user-attachments/assets/2150bd8f-fd56-430d-a8c2-4d0832e73520" />
<img width="523" height="437" alt="86" src="https://github.com/user-attachments/assets/b751fc7c-e518-44f9-b132-51ff740dc48d" />
<img width="593" height="219" alt="85" src="https://github.com/user-attachments/assets/b2469281-c765-4bd7-8bcc-2de21f084624" />
<img width="619" height="120" alt="80" src="https://github.com/user-attachments/assets/5a9dcaf1-405d-489a-82ce-7248af681538" />
<img width="713" height="189" alt="79" src="https://github.com/user-attachments/assets/452d0184-9550-4adf-b8bc-59fefdd246f9" />
<img width="681" height="200" alt="78" src="https://github.com/user-attachments/assets/febc8233-e45d-4b2f-9cef-ce7742311376" />

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
<img width="713" height="189" alt="79" src="https://github.com/user-attachments/assets/c9d01b1a-6170-4852-a29c-3717960a382c" />


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
<img width="713" height="189" alt="79" src="https://github.com/user-attachments/assets/7a1c12c5-d875-491c-bbc8-8a2ce0cb3d29" />

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
<img width="593" height="219" alt="85" src="https://github.com/user-attachments/assets/e350309d-6972-406f-a82a-4029ae6ee60f" />

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
<img width="523" height="437" alt="86" src="https://github.com/user-attachments/assets/b535ea9c-bb81-4d9f-a369-8799872edafa" />

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

 <img width="763" height="175" alt="87" src="https://github.com/user-attachments/assets/08b69169-5948-47f5-b166-4f72d4036f46" />

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

<img width="523" height="437" alt="86" src="https://github.com/user-attachments/assets/24a46621-2250-47dd-b26e-a549cc7c6485" />

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
 <img width="763" height="175" alt="87" src="https://github.com/user-attachments/assets/87a811c8-2d4a-488a-87b0-5eb7e763a438" />

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
<img width="771" height="339" alt="88" src="https://github.com/user-attachments/assets/024a0518-afa8-4fe5-aa5d-1f79738fffa7" />


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

 <img width="771" height="339" alt="88" src="https://github.com/user-attachments/assets/999006bb-a9f0-4f31-aec7-595fa4abeccd" />

 ./funcex.sh 1 2

 <img width="771" height="339" alt="88" src="https://github.com/user-attachments/assets/8b64b0a9-9073-4b63-8806-5ec799f3cf67" />

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
 <img width="480" height="214" alt="89" src="https://github.com/user-attachments/assets/be10f6ed-820f-45a2-ac69-43bcd55fc01b" />

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
 <img width="463" height="131" alt="90" src="https://github.com/user-attachments/assets/a95b73d4-cc57-4f6e-a85b-1be55ceb2b64" />

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
 
 <img width="498" height="362" alt="91" src="https://github.com/user-attachments/assets/e4660c4a-551d-4c3b-9575-16abb7adb326" />

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
 <img width="588" height="370" alt="94" src="https://github.com/user-attachments/assets/15d94039-731c-439b-9392-f45fa7ffeaec" />

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
<img width="661" height="563" alt="95" src="https://github.com/user-attachments/assets/3a90c3b8-03d8-4089-83d3-7e13b8832f04" />



# RESULT:
The Commands are executed successfully.
