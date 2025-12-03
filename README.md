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

<img width="492" height="172" alt="image" src="https://github.com/user-attachments/assets/6f80eb8e-4231-4784-95fd-5840103c1b30" />


cat < file2
## OUTPUT
<img width="445" height="202" alt="image" src="https://github.com/user-attachments/assets/e24d9b16-1ee8-4ab8-bef9-8575f5d2509e" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="405" height="90" alt="image" src="https://github.com/user-attachments/assets/7ae7650b-bfe1-42e1-9dc6-d90f976ca8d9" />

comm file1 file2
 ## OUTPUT
<img width="480" height="251" alt="image" src="https://github.com/user-attachments/assets/a7a1bcfa-b04c-47fe-b39c-375d505687bb" />

 
diff file1 file2
## OUTPUT
<img width="421" height="307" alt="image" src="https://github.com/user-attachments/assets/dd157898-6d6e-47c1-ae35-a8c2d5d04a7a" />


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

<img width="421" height="114" alt="image" src="https://github.com/user-attachments/assets/85db25bb-0ce4-4d54-a9f7-74024717d992" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="426" height="137" alt="image" src="https://github.com/user-attachments/assets/07b5e695-8b67-4eb8-9102-7deebb495c6a" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="467" height="135" alt="image" src="https://github.com/user-attachments/assets/43afc03e-a49a-4a27-aece-51a48b909bf1" />


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

<img width="493" height="86" alt="image" src="https://github.com/user-attachments/assets/3503237b-970d-45c8-b4cd-cbe427eb3a29" />


grep hello newfile 
## OUTPUT

<img width="473" height="85" alt="image" src="https://github.com/user-attachments/assets/f16571e4-2cdf-4392-952f-d8b8c3f1f747" />

grep -v hello newfile 
## OUTPUT

<img width="410" height="90" alt="image" src="https://github.com/user-attachments/assets/a1daefd1-b143-46e0-8713-cc86d4e39d14" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="432" height="116" alt="image" src="https://github.com/user-attachments/assets/766512dd-e0f0-482c-9084-d67272a64a23" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="519" height="80" alt="image" src="https://github.com/user-attachments/assets/c5ea3ea2-ab9c-4aba-8c8c-d0f97e7212ff" />

grep -R ubuntu /etc
## OUTPUT

<img width="516" height="505" alt="image" src="https://github.com/user-attachments/assets/d158c0e6-3a9c-41ee-ba36-44a6ac776fc8" />


grep -w -n world newfile   
## OUTPUT

<img width="467" height="109" alt="image" src="https://github.com/user-attachments/assets/db620873-1219-43bf-a23e-0758e9c0402a" />

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

<img width="550" height="108" alt="image" src="https://github.com/user-attachments/assets/828717e5-692a-404f-891b-89c2e48b78e1" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="433" height="121" alt="image" src="https://github.com/user-attachments/assets/0c53e691-10cc-48a8-9ae0-d5e4f8fee006" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="410" height="83" alt="image" src="https://github.com/user-attachments/assets/dfec674b-ddb6-468c-9717-625ed41f5262" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="444" height="78" alt="image" src="https://github.com/user-attachments/assets/d61505c3-4eac-4207-a90a-38e184072cf4" />

egrep '(world$)' newfile 
## OUTPUT

<img width="482" height="113" alt="image" src="https://github.com/user-attachments/assets/53209c2a-66ea-4035-ae0e-2ca62fae2519" />

egrep '(World$)' newfile 
## OUTPUT

<img width="412" height="93" alt="image" src="https://github.com/user-attachments/assets/e38c7c2e-9bdb-4917-9738-8ef1f0986a72" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="438" height="111" alt="image" src="https://github.com/user-attachments/assets/0325ff0b-6f52-4cfd-a28f-4151cd5af523" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="434" height="87" alt="image" src="https://github.com/user-attachments/assets/108e988d-88fc-4ca2-b671-f20f638f70bb" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="427" height="87" alt="image" src="https://github.com/user-attachments/assets/b0fed358-1ace-4f45-b8a2-840a1cb2ca30" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="421" height="86" alt="image" src="https://github.com/user-attachments/assets/eae93f38-a69f-4809-b8da-6bcd2892efcf" />

egrep l{2} newfile
## OUTPUT

<img width="437" height="109" alt="image" src="https://github.com/user-attachments/assets/acaaf219-cace-4ba1-9197-d5b2ca5cd872" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="484" height="143" alt="image" src="https://github.com/user-attachments/assets/4f89068b-d1c3-4c0b-83cc-71899b7f1e9c" />

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

<img width="420" height="83" alt="image" src="https://github.com/user-attachments/assets/37951581-0d15-409f-8f46-efe11a6b1840" />

sed -n -e '$p' file23
## OUTPUT

<img width="441" height="85" alt="image" src="https://github.com/user-attachments/assets/fbc25471-aac7-4693-bfa1-b85e566a9137" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="461" height="262" alt="image" src="https://github.com/user-attachments/assets/b385434b-d967-4d99-a0e8-dcb253948ff9" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="459" height="296" alt="image" src="https://github.com/user-attachments/assets/e59e91c4-eeae-4d08-a5a2-580ccf381e1e" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="437" height="264" alt="image" src="https://github.com/user-attachments/assets/34ba0e26-83eb-412e-ab3a-b9a35212382f" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="458" height="209" alt="image" src="https://github.com/user-attachments/assets/277c400f-a266-498c-a819-c73a82257afd" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="431" height="139" alt="image" src="https://github.com/user-attachments/assets/41689ca1-fa88-40a3-b881-00f56652ba85" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="447" height="108" alt="image" src="https://github.com/user-attachments/assets/2408ee59-6351-4253-bd0c-9fc60e6bf0c6" />

seq 10 
## OUTPUT

<img width="517" height="319" alt="image" src="https://github.com/user-attachments/assets/5bd0feb4-01a6-4b49-b73b-5e5922901183" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="453" height="137" alt="image" src="https://github.com/user-attachments/assets/47c87dff-9e22-4ab4-8676-0da3c55039c4" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="460" height="137" alt="image" src="https://github.com/user-attachments/assets/423eabee-e18c-486f-aa27-04f080e8a988" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="488" height="171" alt="image" src="https://github.com/user-attachments/assets/14a1a5c5-4d3f-44c6-8ecc-56c42abfe36d" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="456" height="130" alt="image" src="https://github.com/user-attachments/assets/9cc06d2f-9c71-47c6-b3e4-3830276eb61a" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="468" height="136" alt="image" src="https://github.com/user-attachments/assets/f6efa9f9-fa03-46f6-95b2-30d950399726" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="482" height="140" alt="image" src="https://github.com/user-attachments/assets/789dd12b-3bfd-4945-875f-2a7dba336f01" />

sed -n '2,4{s/$/*/;p}' file23

<img width="424" height="128" alt="image" src="https://github.com/user-attachments/assets/249e4204-b4c1-45a8-9274-9d7da3161cdf" />

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

<img width="476" height="192" alt="image" src="https://github.com/user-attachments/assets/a98aebae-ed23-457f-ac50-c27b4cdcfe87" />

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

<img width="472" height="172" alt="image" src="https://github.com/user-attachments/assets/933d2f74-0942-4fd3-aae3-84577ac4507a" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="522" height="246" alt="image" src="https://github.com/user-attachments/assets/e82e65f8-72b3-474d-a2a2-ff319b03c5b1" />

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

<img width="432" height="127" alt="image" src="https://github.com/user-attachments/assets/a331fe71-d4b1-4031-9183-f7293b466873" />
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="448" height="115" alt="image" src="https://github.com/user-attachments/assets/797e559b-5564-4056-850f-586569d20ffa" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="497" height="606" alt="image" src="https://github.com/user-attachments/assets/063bd32e-b8fd-409b-a5e9-715f863454f4" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="482" height="203" alt="image" src="https://github.com/user-attachments/assets/77f0e29e-2f32-46eb-9f8b-639acc420bbf" />

tar -xvf backup.tar
## OUTPUT

<img width="515" height="494" alt="image" src="https://github.com/user-attachments/assets/c7271a68-9e55-49bd-ad6a-7306ce8a21e9" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="436" height="43" alt="image" src="https://github.com/user-attachments/assets/e813a284-771a-4eaa-b3d4-aea62db4752b" />

gunzip backup.tar.gz
## OUTPUT

<img width="483" height="68" alt="image" src="https://github.com/user-attachments/assets/a68cf4e7-08bd-474e-9dd5-28ec2c3e4b5f" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="429" height="153" alt="image" src="https://github.com/user-attachments/assets/92708019-7b68-4922-9b60-d943953a8f17" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="478" height="124" alt="image" src="https://github.com/user-attachments/assets/302d4229-bfb6-4a9e-aef3-463b46a40c2b" />

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

<img width="516" height="282" alt="image" src="https://github.com/user-attachments/assets/041ae249-f6b0-44fc-84d9-2828675a855c" />
 
ls file1
## OUTPUT

<img width="455" height="79" alt="image" src="https://github.com/user-attachments/assets/6fa08cc3-4b03-4c74-a7e7-68a71db90498" />

echo $?
## OUTPUT 

<img width="423" height="92" alt="image" src="https://github.com/user-attachments/assets/07a53f61-1071-41dd-8dc7-0da8267d8f82" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="473" height="88" alt="image" src="https://github.com/user-attachments/assets/e3f8634d-04cc-47ba-bc83-33c1119e7114" />

abcd
 
echo $?
 ## OUTPUT

<img width="422" height="84" alt="image" src="https://github.com/user-attachments/assets/2ce13dbf-3299-43f5-811c-b85c206ad200" />
 
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

<img width="451" height="262" alt="image" src="https://github.com/user-attachments/assets/df2d875d-837e-46c8-98f7-6be95ef8aac6" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="484" height="273" alt="image" src="https://github.com/user-attachments/assets/bf3add5f-3d7c-4112-bb76-75f4af31dbb2" />

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

<img width="501" height="304" alt="image" src="https://github.com/user-attachments/assets/0f368ce7-af5c-4636-830f-68100e50ed8a" />

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

<img width="502" height="958" alt="image" src="https://github.com/user-attachments/assets/876e7b95-e1cf-4b83-9332-e6527f387435" />

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

<img width="495" height="380" alt="image" src="https://github.com/user-attachments/assets/b7feb5e7-585c-4752-8190-50436f18cae7" />
<img width="516" height="463" alt="image" src="https://github.com/user-attachments/assets/97022e92-99f0-4b67-a173-850d74af31c4" />

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

<img width="449" height="165" alt="image" src="https://github.com/user-attachments/assets/a451adde-75ce-49bd-be2f-3bd5973441e7" />
<img width="456" height="141" alt="image" src="https://github.com/user-attachments/assets/a3461250-6253-4c4b-b3fb-2a655967d256" />
<img width="478" height="352" alt="image" src="https://github.com/user-attachments/assets/7263d1f2-c3f4-4de3-b862-2e14b9d2cc2b" />
<img width="484" height="384" alt="image" src="https://github.com/user-attachments/assets/8a617ef5-b319-47dd-8708-c5d60be6adf1" />
<img width="504" height="136" alt="image" src="https://github.com/user-attachments/assets/1679dd58-c9c2-46c6-8709-a234dea00cf3" />
<img width="509" height="121" alt="image" src="https://github.com/user-attachments/assets/f237e70f-d01a-436a-b0b1-714b97fcb724" />
<img width="518" height="442" alt="image" src="https://github.com/user-attachments/assets/52cfe91b-1f4c-487a-86fc-0feeef968dfc" />
<img width="514" height="193" alt="image" src="https://github.com/user-attachments/assets/5fd7e310-b6c2-4006-ae66-4a62148caa5b" />
<img width="512" height="101" alt="image" src="https://github.com/user-attachments/assets/f1fc2dca-ce12-431b-b339-12973a31366b" />
<img width="519" height="142" alt="image" src="https://github.com/user-attachments/assets/3cb3fca3-a5c0-49b5-8808-fb6827c1c236" />
<img width="519" height="151" alt="image" src="https://github.com/user-attachments/assets/7a4991a6-28da-4338-b814-54a7ed498a2a" />

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

<img width="513" height="145" alt="image" src="https://github.com/user-attachments/assets/2e5074df-524b-4296-9420-032e0b2e55d5" />

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

<img width="521" height="142" alt="image" src="https://github.com/user-attachments/assets/5187d5a5-2358-4b2c-a868-54e7676ce2e6" />

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

<img width="484" height="196" alt="image" src="https://github.com/user-attachments/assets/783f84e7-48bf-467e-af46-cf9140cbbdb1" />

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

<img width="469" height="436" alt="image" src="https://github.com/user-attachments/assets/5025270f-c5dd-4b9d-8dcb-0e1640b84b61" />

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

<img width="495" height="122" alt="image" src="https://github.com/user-attachments/assets/8840475b-546a-47f2-94ec-40b52d970da0" />
 
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

<img width="479" height="438" alt="image" src="https://github.com/user-attachments/assets/e3d20c5b-1ee2-491a-8821-92a91dae8adf" />

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

<img width="510" height="117" alt="image" src="https://github.com/user-attachments/assets/6fb8fb59-3a55-414a-92ba-5716edf95851" />

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

<img width="527" height="230" alt="image" src="https://github.com/user-attachments/assets/1560daef-a35e-466e-8c1e-36ceb1c2ef39" />
 
 ./funcex.sh 1 2

<img width="526" height="228" alt="image" src="https://github.com/user-attachments/assets/90b4f30f-8a77-46c1-84e9-09751858f941" />
 
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

 <img width="458" height="239" alt="image" src="https://github.com/user-attachments/assets/7a05907e-02eb-45b3-b670-2b5c855be906" />

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

 <img width="480" height="144" alt="image" src="https://github.com/user-attachments/assets/ce00b760-6ec2-491b-b3f1-ebbb5b429314" />

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
 
<img width="482" height="376" alt="image" src="https://github.com/user-attachments/assets/3f353cd6-182f-41b9-bfb1-c4088d2308de" />
 
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

 <img width="461" height="333" alt="image" src="https://github.com/user-attachments/assets/fad5ce3d-ce83-4e11-8ebe-04ca8f597fb2" />

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

<img width="494" height="450" alt="image" src="https://github.com/user-attachments/assets/c6152cff-3386-4ad0-ac1e-e16bd68c1a16" />

# RESULT:
The Commands are executed successfully.
