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
<img width="661" height="175" alt="image" src="https://github.com/user-attachments/assets/bbbaeff7-1c82-4dd1-9cca-8998eba63e31" />

cat < file2
## OUTPUT
<img width="653" height="179" alt="image" src="https://github.com/user-attachments/assets/468a3895-f88b-4b7c-bcda-f4a001e82a98" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="644" height="74" alt="image" src="https://github.com/user-attachments/assets/807718a9-d096-45cf-9ec1-229539c467f6" />

comm file1 file2
 ## OUTPUT
<img width="622" height="222" alt="image" src="https://github.com/user-attachments/assets/0c8c33f1-79b1-4e74-be32-b816eca8367c" />

 
diff file1 file2
## OUTPUT
<img width="633" height="291" alt="image" src="https://github.com/user-attachments/assets/a0e17440-7d2f-456e-ae97-754c79a4004c" />


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
<img width="707" height="95" alt="image" src="https://github.com/user-attachments/assets/24e67f4e-f4bb-4d1c-a70c-a3fad56bf509" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="568" height="125" alt="image" src="https://github.com/user-attachments/assets/f695eb60-ae38-4b3a-93ac-634d3a13faeb" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="629" height="118" alt="image" src="https://github.com/user-attachments/assets/7a837432-e8db-4e99-905c-faca3e8a7b18" />


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
<img width="566" height="73" alt="image" src="https://github.com/user-attachments/assets/a204e1ab-eb78-4073-be51-d6ce1dddb666" />



grep hello newfile 
## OUTPUT
<img width="668" height="79" alt="image" src="https://github.com/user-attachments/assets/e77dd7ce-f533-4462-8f2f-a86e8d7442e7" />




grep -v hello newfile 
## OUTPUT
<img width="610" height="70" alt="image" src="https://github.com/user-attachments/assets/21509237-b453-4555-8dc5-35fae91daf87" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="583" height="100" alt="image" src="https://github.com/user-attachments/assets/71fa0b77-db2c-4c14-b4f7-de5cdbd612d6" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="588" height="71" alt="image" src="https://github.com/user-attachments/assets/bafc9a3c-814c-4762-8199-c63ecbaace13" />




grep -w -n world newfile   
## OUTPUT
<img width="658" height="99" alt="image" src="https://github.com/user-attachments/assets/4ca25f1a-0ebe-4f0c-bafd-a9ebe54536d3" />


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
<img width="641" height="98" alt="image" src="https://github.com/user-attachments/assets/944cad22-e776-424a-af5d-5c0ede051d2f" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="633" height="90" alt="image" src="https://github.com/user-attachments/assets/b8afdb91-19d0-4eff-806e-1c44b4c07589" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="563" height="97" alt="image" src="https://github.com/user-attachments/assets/125f5472-ae56-4b44-9d13-bfc6314212fb" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="658" height="66" alt="image" src="https://github.com/user-attachments/assets/23cabb3b-5c74-42a9-8ca5-fe91b9bbdf9d" />



egrep '(world$)' newfile 
## OUTPUT
<img width="637" height="99" alt="image" src="https://github.com/user-attachments/assets/f5e82d68-f71d-4d12-b7cc-68dda4e336ce" />



egrep '(World$)' newfile 
## OUTPUT
<img width="637" height="99" alt="image" src="https://github.com/user-attachments/assets/f5e82d68-f71d-4d12-b7cc-68dda4e336ce" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="484" height="101" alt="image" src="https://github.com/user-attachments/assets/612ea19b-b6e7-49c0-8329-2a6d6e521f23" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="637" height="99" alt="image" src="https://github.com/user-attachments/assets/f5e82d68-f71d-4d12-b7cc-68dda4e336ce" />

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
<img width="521" height="75" alt="image" src="https://github.com/user-attachments/assets/bd03a688-84b5-435c-8ef7-46e62ca34a63" />

sed -n -e '$p' file23
## OUTPUT
<img width="642" height="72" alt="image" src="https://github.com/user-attachments/assets/83d6adc4-1d04-426a-80a7-5bc280679c2c" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="572" height="237" alt="image" src="https://github.com/user-attachments/assets/dc9eb8b7-249a-4e95-a1e4-6a0fa57d4dcf" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="553" height="250" alt="image" src="https://github.com/user-attachments/assets/af63fdfa-8af8-48c9-8990-9f88e3533706" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="646" height="247" alt="image" src="https://github.com/user-attachments/assets/9cf424ff-0fe3-43d7-9d13-0eb6c1022056" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="594" height="169" alt="image" src="https://github.com/user-attachments/assets/26eaeba4-015a-430f-b5ee-78f3e96beff1" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="466" height="123" alt="image" src="https://github.com/user-attachments/assets/2c0b15b7-cb72-4591-be23-9507dc7c23f1" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="524" height="97" alt="image" src="https://github.com/user-attachments/assets/56848918-0072-4726-b50b-216a1d8f71e9" />

seq 10 
## OUTPUT
<img width="529" height="298" alt="image" src="https://github.com/user-attachments/assets/95da86fb-bc84-48f8-92de-e772d412405d" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="424" height="122" alt="image" src="https://github.com/user-attachments/assets/bebbcad5-23cb-4f6f-9e7d-044f918dd2e9" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="548" height="116" alt="image" src="https://github.com/user-attachments/assets/5ae093af-f9c9-4d80-905f-332a2353cbb9" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="468" height="150" alt="image" src="https://github.com/user-attachments/assets/de2c597d-b65a-4a3b-8bfb-98c7cbedf73e" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="409" height="122" alt="image" src="https://github.com/user-attachments/assets/2e6eac86-7b0b-408f-9d22-472586697e91" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="550" height="122" alt="image" src="https://github.com/user-attachments/assets/35813e2c-c886-481b-acdf-850de1c50bce" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="549" height="127" alt="image" src="https://github.com/user-attachments/assets/265e4b0a-b095-4935-8593-3fa49824d55c" />

sed -n '2,4{s/$/*/;p}' file23
<img width="492" height="122" alt="image" src="https://github.com/user-attachments/assets/a6cdb4cc-008b-4e03-ae65-8e96a1659490" />

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
<img width="574" height="153" alt="image" src="https://github.com/user-attachments/assets/2f0017a4-c3ee-43a7-aed6-cbbded8596d2" />


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

<img width="540" height="148" alt="image" src="https://github.com/user-attachments/assets/407cffe2-3bad-45f6-b811-71399a4da8c2" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="624" height="246" alt="image" src="https://github.com/user-attachments/assets/8cd1c402-a125-4ce9-8d60-055df504c93f" />

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
<img width="568" height="125" alt="image" src="https://github.com/user-attachments/assets/79710612-4677-4548-974a-3adc0859b849" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="567" height="120" alt="image" src="https://github.com/user-attachments/assets/b0dde669-97a5-4d2b-a285-1c36541946ee" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="624" height="546" alt="image" src="https://github.com/user-attachments/assets/ab5066ce-84e9-4f4f-8d4a-9d86e2510305" />
<img width="797" height="596" alt="image" src="https://github.com/user-attachments/assets/fde1c234-f800-4d52-9548-e74d82a4da40" />

<img width="779" height="468" alt="image" src="https://github.com/user-attachments/assets/afb661cf-a7c0-42c4-9a2b-8e26782a04f9" />
<img width="790" height="598" alt="image" src="https://github.com/user-attachments/assets/ae8068c5-5eaa-4fe4-a252-b8371e0c60cc" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="867" height="526" alt="image" src="https://github.com/user-attachments/assets/09b4caba-659b-4bfd-9d35-9b2767001913" />
<img width="634" height="546" alt="image" src="https://github.com/user-attachments/assets/e6179442-60be-4c92-b896-ca1ae42dbd6e" />


tar -xvf backup.tar
## OUTPUT
<img width="566" height="118" alt="image" src="https://github.com/user-attachments/assets/6a33d618-1239-4dd9-a25e-0fd892f6dd20" />
<img width="500" height="73" alt="image" src="https://github.com/user-attachments/assets/db2cda6b-b2aa-4cec-a43d-98325ce82092" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="604" height="70" alt="image" src="https://github.com/user-attachments/assets/4cd0f997-73b8-4c07-95f2-81bb5cd7481e" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="460" height="71" alt="image" src="https://github.com/user-attachments/assets/53070301-7ea4-42c1-b69c-a7f2d9cfd4a7" />


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
<img width="693" height="74" alt="image" src="https://github.com/user-attachments/assets/58400ccc-13d9-40fa-a405-aac0290105aa" />

 
ls file1
## OUTPUT
<img width="461" height="75" alt="image" src="https://github.com/user-attachments/assets/09cc6ca9-7839-4fc6-999c-d210ca9277c8" />

echo $?
## OUTPUT 
<img width="682" height="298" alt="image" src="https://github.com/user-attachments/assets/d3619ba9-e04a-4f63-8153-c1acaef58606" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="800" height="246" alt="image" src="https://github.com/user-attachments/assets/3b2f982f-f015-40d9-8f6b-482ef6c85256" />

abcd
 
echo $?
 ## OUTPUT
<img width="682" height="298" alt="image" src="https://github.com/user-attachments/assets/d3619ba9-e04a-4f63-8153-c1acaef58606" />


 
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
<img width="569" height="269" alt="image" src="https://github.com/user-attachments/assets/370863e3-ff1c-4bbc-b273-1e0cccd0530d" />
chmod 755 strcomp.sh
 
./strcomp.sh
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
<img width="703" height="248" alt="image" src="https://github.com/user-attachments/assets/e98c36e9-b500-4425-a1ab-8c0aad0fef43" />



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
./ifnested.sh




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
 
$  cat < elifcheck.sh 
## OUTPUT



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
$ cat < ifcompound.sh 
## OUTPUT


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
<img width="611" height="200" alt="image" src="https://github.com/user-attachments/assets/36d75d7b-3b4d-4bcb-bf81-711f3fe961e4" />

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
<img width="720" height="299" alt="image" src="https://github.com/user-attachments/assets/60c95dae-72e4-4433-b2e1-80c08bf2d0b4" />

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
<img width="598" height="321" alt="image" src="https://github.com/user-attachments/assets/d17f195e-7505-4151-8d7d-fb85f07d91f9" />


 
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
<img width="684" height="319" alt="image" src="https://github.com/user-attachments/assets/ee13df99-704d-423f-9206-c7bac957b042" />


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
echo "The for loop is completed“cat 
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

![Uploading image.png…]()


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![Uploading image.png…]()



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
 ![Uploading image.png…]()

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
![Uploading image.png…]()


# RESULT:
The Commands are executed successfully.
