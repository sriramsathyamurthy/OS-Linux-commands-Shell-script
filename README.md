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
<img width="332" height="135" alt="image" src="https://github.com/user-attachments/assets/19e07796-1324-4ea9-826d-dc7fe9cccb91" />

cat < file2
## OUTPUT
<img width="357" height="162" alt="image" src="https://github.com/user-attachments/assets/9423ad42-0a39-4da5-96e2-a1c75aafa5a3" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="441" height="50" alt="image" src="https://github.com/user-attachments/assets/63c64e93-c638-4e49-b100-98d6a5a58545" />

comm file1 file2
 ## OUTPUT
<img width="465" height="317" alt="image" src="https://github.com/user-attachments/assets/5dc95f16-0a00-40b5-9487-ee8177763b1c" />

 
diff file1 file2
## OUTPUT
<img width="406" height="232" alt="image" src="https://github.com/user-attachments/assets/7b2edd65-8f6a-4002-bd8c-735271fbc846" />


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

<img width="390" height="70" alt="image" src="https://github.com/user-attachments/assets/2aa7b1af-429d-42bf-a3f5-ae294de753d8" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="461" height="85" alt="image" src="https://github.com/user-attachments/assets/2c508acd-fae4-4212-986c-f94576e022b8" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="476" height="95" alt="image" src="https://github.com/user-attachments/assets/28812c5a-e10a-4a60-9200-167bca98d97e" />

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
<img width="427" height="47" alt="image" src="https://github.com/user-attachments/assets/3bc66dd6-7f11-4e73-9aaf-26767411da51" />


grep hello newfile 
## OUTPUT
<img width="412" height="41" alt="image" src="https://github.com/user-attachments/assets/38bba335-b06b-423a-aad2-a89e5273450d" />


grep -v hello newfile 
## OUTPUT
<img width="457" height="43" alt="image" src="https://github.com/user-attachments/assets/cfad07c1-b6cd-4259-bb1a-ed7431a99979" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="628" height="63" alt="image" src="https://github.com/user-attachments/assets/4f4f4f35-b7da-4442-a507-00aa2363ebb2" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="567" height="41" alt="image" src="https://github.com/user-attachments/assets/57e729aa-39ee-4607-b55c-b499bde4ea24" />

grep -w -n world newfile   
## OUTPUT
<img width="493" height="66" alt="image" src="https://github.com/user-attachments/assets/14e5987e-49d5-4cb0-bcd1-f4750920c791" />


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
<img width="567" height="66" alt="image" src="https://github.com/user-attachments/assets/30b1d723-caf0-404b-b99f-0b0762473b5f" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="561" height="67" alt="image" src="https://github.com/user-attachments/assets/18555610-a451-44d4-a1ee-903b251286dc" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="613" height="67" alt="image" src="https://github.com/user-attachments/assets/6cb83cce-ea24-4b6d-b9fc-77a2e9c7ae7e" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="497" height="43" alt="image" src="https://github.com/user-attachments/assets/b2dd3aa4-68f6-41be-9653-913fe1233c4c" />


egrep '(world$)' newfile 
## OUTPUT

<img width="492" height="70" alt="image" src="https://github.com/user-attachments/assets/f6e4ab7a-6329-43b3-8029-ca62e5bcf87f" />


egrep '(World$)' newfile 
## OUTPUT
<img width="532" height="42" alt="image" src="https://github.com/user-attachments/assets/c47ffd62-b1bd-4c22-b0e0-ac8ca7214139" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="535" height="88" alt="image" src="https://github.com/user-attachments/assets/2254571e-b391-48ca-96e2-71ceba073503" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="521" height="48" alt="image" src="https://github.com/user-attachments/assets/5eb43ea8-9659-4e49-869d-7b1f4f9df7c4" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="537" height="40" alt="image" src="https://github.com/user-attachments/assets/9c2fd534-ee64-48b7-8f63-38deba9e295e" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="536" height="37" alt="image" src="https://github.com/user-attachments/assets/9228a7cc-8a06-4e5c-a613-831f7cb5a0c2" />


egrep l{2} newfile
## OUTPUT

<img width="430" height="61" alt="image" src="https://github.com/user-attachments/assets/529595de-c3e5-4ed8-a041-2c3ce7e734fc" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="460" height="87" alt="image" src="https://github.com/user-attachments/assets/3dad8e01-f5a7-43f0-8d79-9735e7a7c578" />


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
<img width="465" height="43" alt="image" src="https://github.com/user-attachments/assets/b5e43133-4e45-4853-a92b-90752cf51d99" />


sed -n -e '$p' file23
## OUTPUT
<img width="442" height="47" alt="image" src="https://github.com/user-attachments/assets/95b03d88-4b71-4bd6-bce3-1e507f7790a9" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="518" height="202" alt="image" src="https://github.com/user-attachments/assets/4fe18e31-906a-412c-8ff2-cecae68833bc" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="575" height="207" alt="image" src="https://github.com/user-attachments/assets/cb5a5c06-ceab-4ecd-bb1a-b29bc0908d08" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="555" height="210" alt="image" src="https://github.com/user-attachments/assets/ee1415d4-d436-461a-8ffe-a8125d7f0f27" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="510" height="160" alt="image" src="https://github.com/user-attachments/assets/d034f7fc-80f9-4e9e-827c-b25297b63b47" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="602" height="87" alt="image" src="https://github.com/user-attachments/assets/904d834a-9448-4f5d-9b8b-57e940c4e8ef" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="632" height="70" alt="image" src="https://github.com/user-attachments/assets/3978ae3f-369f-4308-975f-3a185242e67e" />


seq 10 
## OUTPUT

<img width="293" height="250" alt="image" src="https://github.com/user-attachments/assets/7db8a9f0-1e6d-408d-b786-42aac1800472" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="477" height="100" alt="image" src="https://github.com/user-attachments/assets/8386c2fd-ffcd-4f4c-81ea-98e28834d28f" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="487" height="100" alt="image" src="https://github.com/user-attachments/assets/26645d83-02d7-416a-a123-034cfcfed921" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="470" height="117" alt="image" src="https://github.com/user-attachments/assets/fa8fb5b2-cec0-48dc-9dba-60db3cf17c7f" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="540" height="93" alt="image" src="https://github.com/user-attachments/assets/32bbb5b3-6383-44ab-b444-3d4ca2faf2f3" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="505" height="92" alt="image" src="https://github.com/user-attachments/assets/a3f34870-e596-45ff-a0d8-13476e23a109" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="542" height="95" alt="image" src="https://github.com/user-attachments/assets/198da8a1-2856-4d27-9d72-119258ec2d9e" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="381" height="90" alt="image" src="https://github.com/user-attachments/assets/98f4a6ed-6994-424e-9005-da9153a47ba0" />


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
<img width="377" height="113" alt="image" src="https://github.com/user-attachments/assets/5b7830b5-b566-4be2-b1b8-7e8c1b9f5ee6" />


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
<img width="410" height="117" alt="image" src="https://github.com/user-attachments/assets/00e42d08-416b-4b17-824f-2dfd41943aec" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="641" height="203" alt="image" src="https://github.com/user-attachments/assets/626f48bb-4c4f-4f7e-82e6-3f29bbe63864" />

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

<img width="535" height="92" alt="image" src="https://github.com/user-attachments/assets/641281a7-b7f2-47f3-a312-09735b4b1f05" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="652" height="83" alt="image" src="https://github.com/user-attachments/assets/43107a8e-cc05-4fef-af99-164478d0e8a4" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="473" height="271" alt="image" src="https://github.com/user-attachments/assets/0252e989-69d1-4f10-859c-c41837388f27" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="742" height="280" alt="image" src="https://github.com/user-attachments/assets/466704e5-8f86-423a-b2dc-2d641260742d" />


tar -xvf backup.tar
## OUTPUT
<img width="635" height="272" alt="image" src="https://github.com/user-attachments/assets/45518d98-790c-4035-85df-ce4329adda7b" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="631" height="37" alt="image" src="https://github.com/user-attachments/assets/6abc996a-7694-4c9e-9687-353836bf53e5" />

gunzip backup.tar.gz
## OUTPUT
<img width="588" height="28" alt="image" src="https://github.com/user-attachments/assets/5dcce7c9-69f4-4fbd-ab53-dbd611c0e510" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="875" height="85" alt="image" src="https://github.com/user-attachments/assets/94126cc4-b0ec-43cd-ad75-7cdf98bba65d" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="530" height="87" alt="image" src="https://github.com/user-attachments/assets/40600881-d016-49b1-af56-0a8c58bb9134" />


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
<img width="562" height="45" alt="image" src="https://github.com/user-attachments/assets/b4e2d59a-f9e8-44f6-8b50-9c991d4d3e16" />

 
ls file1
## OUTPUT
<img width="416" height="46" alt="image" src="https://github.com/user-attachments/assets/1c059662-62f1-436c-8916-8d2ca91ed83f" />

echo $?
## OUTPUT 
<img width="410" height="40" alt="image" src="https://github.com/user-attachments/assets/b42d7e2a-fe9f-4764-8fc0-09eee70b38ca" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="401" height="50" alt="image" src="https://github.com/user-attachments/assets/82b23fe3-26db-45c2-acd5-1ec0c614dbec" />

abcd
 
echo $?
 ## OUTPUT

<img width="417" height="45" alt="image" src="https://github.com/user-attachments/assets/a802c81f-0ab1-47b2-a4c8-d5a029a2e68a" />

 
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




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="557" height="71" alt="image" src="https://github.com/user-attachments/assets/b80ac2e0-c33c-4cfd-838f-ef948f93a494" />


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
<img width="502" height="53" alt="image" src="https://github.com/user-attachments/assets/4f85cbb2-3637-40c1-85c7-12cc8415d66b" />

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

<img width="528" height="47" alt="image" src="https://github.com/user-attachments/assets/14e1cec0-9c36-4834-a17b-21e27b1fdca0" />


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
<img width="470" height="50" alt="image" src="https://github.com/user-attachments/assets/222baec8-21d0-46fc-86eb-c781df1ffb44" />

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
<img width="477" height="52" alt="image" src="https://github.com/user-attachments/assets/1fd7f810-6624-43c1-aeec-54f481c15bd2" />

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
<img width="566" height="47" alt="image" src="https://github.com/user-attachments/assets/643a83fc-b1e0-4631-99a8-cc025148c78e" />


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
<img width="525" height="50" alt="image" src="https://github.com/user-attachments/assets/53508187-751c-47ef-afa3-0039b10c1910" />

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
 <img width="737" height="138" alt="image" src="https://github.com/user-attachments/assets/94c2fbaf-acb2-4785-8f61-df88f2163563" />

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
<img width="828" height="458" alt="image" src="https://github.com/user-attachments/assets/05df6fbd-5d83-4177-b188-dc64a4a488a5" />

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
<img width="1015" height="226" alt="image" src="https://github.com/user-attachments/assets/c8522807-f51d-41e1-9658-36202a04547f" />


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
<img width="468" height="137" alt="image" src="https://github.com/user-attachments/assets/a6cf584e-b4b0-41ec-9b3c-6f33db8f7abe" />

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
<img width="502" height="51" alt="image" src="https://github.com/user-attachments/assets/d82c63e2-1741-49ab-921e-25d6802ff53b" />

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
<img width="580" height="300" alt="image" src="https://github.com/user-attachments/assets/c67148ee-f20f-442e-a233-518a8b0a167f" />

 
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
<img width="455" height="278" alt="image" src="https://github.com/user-attachments/assets/2fdb7ae3-936e-4634-b2d4-df5e08208e93" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 <img width="847" height="87" alt="image" src="https://github.com/user-attachments/assets/1c2c398b-db03-41fa-91e0-d1565db0ffa4" />

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
 <img width="477" height="71" alt="image" src="https://github.com/user-attachments/assets/ae5e69d4-147e-46a4-84d4-ba053c2f5a87" />

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
<img width="816" height="78" alt="image" src="https://github.com/user-attachments/assets/614b3a0d-1c7f-4dfd-8f8d-44ac22803909" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="530" height="102" alt="image" src="https://github.com/user-attachments/assets/7367225a-b9ba-476d-be14-2c62d36d1287" />


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
<img width="626" height="96" alt="image" src="https://github.com/user-attachments/assets/b89e8737-5498-414a-b1e0-5d0e7bf3c423" />

 


 
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
 <img width="761" height="335" alt="image" src="https://github.com/user-attachments/assets/be666302-1208-4b00-bbc2-3d6e3d85832d" />

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
 <img width="585" height="322" alt="image" src="https://github.com/user-attachments/assets/144aabd3-c3c1-46c5-9dad-ab4531b08263" />

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
 <img width="585" height="322" alt="image" src="https://github.com/user-attachments/assets/8bc3f9b8-9d8b-48e6-8ac9-bfe78c268882" />

 
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
 <img width="556" height="526" alt="image" src="https://github.com/user-attachments/assets/ab2f0134-e847-44d0-814c-772ad0e0019b" />

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
<img width="556" height="526" alt="image" src="https://github.com/user-attachments/assets/93a28742-47b0-4a99-a753-7783dba2da4e" />


# RESULT:
The Commands are executed successfully.
