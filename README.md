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


cat < file2
## OUTPUT
<img width="635" height="288" alt="Screenshot 2025-08-22 144639" src="https://github.com/user-attachments/assets/5620b870-1ecf-477f-9d9d-cecf7635b704" />






# Comparing Files
cmp file1 file2
## OUTPUT
<img width="653" height="87" alt="1" src="https://github.com/user-attachments/assets/8464e597-85a1-407c-b73b-080953e0aec7" />

 
comm file1 file2
 ## OUTPUT
<img width="676" height="331" alt="Screenshot 2025-08-22 144639 2" src="https://github.com/user-attachments/assets/35b8d847-fc4a-4e6b-bae3-4d5f7cba4718" />

 
diff file1 file2
## OUTPUT
<img width="637" height="229" alt="Screenshot 2025-08-22 144639" src="https://github.com/user-attachments/assets/86f37763-2530-47e1-be9d-7908c436d5e4" />


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


cut -c1-2 file11
## OUTPUT

<img width="676" height="90" alt="Screenshot 2025-08-22 144842" src="https://github.com/user-attachments/assets/6681b126-f949-400c-834a-4e9c7cce5108" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="736" height="112" alt="Screenshot 2025-08-22 144842 2" src="https://github.com/user-attachments/assets/b2942c8f-cdaf-4784-8395-e7a297d2eef4" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="700" height="124" alt="Screenshot 2025-08-22 144842 3" src="https://github.com/user-attachments/assets/fdd29d48-1e51-4fa7-ba6d-8ef90d821604" />


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

<img width="651" height="92" alt="Screenshot 2025-08-22 145016" src="https://github.com/user-attachments/assets/75008668-e378-45dc-87cc-99e5ba33aa89" />

grep hello newfile 
## OUTPUT

<img width="650" height="88" alt="Screenshot 2025-08-22 145016 2" src="https://github.com/user-attachments/assets/07c1db33-f98a-45a6-82b6-a228bd64d66a" />



grep -v hello newfile 
## OUTPUT
<img width="685" height="91" alt="Screenshot 2025-08-22 145016 3" src="https://github.com/user-attachments/assets/23e3caf3-ee52-46a8-802a-547e0260c43c" />



cat newfile | grep -i "hello"
## OUTPUT



<img width="797" height="106" alt="Screenshot 2025-08-22 145016 4" src="https://github.com/user-attachments/assets/bc162673-35cc-4142-88b3-db2acfc9b2d3" />

cat newfile | grep -i -c "hello"
## OUTPUT


<img width="819" height="111" alt="Screenshot 2025-08-22 145016 5" src="https://github.com/user-attachments/assets/8582b808-581b-4ceb-a1bd-f08c76771ec1" />


grep -R ubuntu /etc
## OUTPUT
<img width="1533" height="702" alt="Screenshot 2025-08-22 145016" src="https://github.com/user-attachments/assets/86072045-58ca-4075-9543-c0598d64cb89" />



grep -w -n world newfile   
## OUTPUT

<img width="739" height="100" alt="Screenshot 2025-08-22 145024" src="https://github.com/user-attachments/assets/00cc13cc-fd4c-45fd-91de-b8749670bf63" />


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
<img width="808" height="109" alt="Screenshot 2025-08-22 145220" src="https://github.com/user-attachments/assets/94ecd097-7284-4e69-bffa-9f8b7772a043" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="770" height="104" alt="Screenshot 2025-08-22 145220 2" src="https://github.com/user-attachments/assets/74038ba8-229a-44b8-aea0-58923b79ec1d" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="806" height="109" alt="3" src="https://github.com/user-attachments/assets/150d261e-d2e5-4bbc-bdd0-626a266e8880" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="806" height="109" alt="3" src="https://github.com/user-attachments/assets/09f3775f-2486-4c5c-80c1-652be311217c" />



egrep '(world$)' newfile 
## OUTPUT
<img width="725" height="98" alt="Screenshot 2025-08-22 145220 4" src="https://github.com/user-attachments/assets/8f8eeb8d-b726-4c52-89ca-a6d90fe5919b" />



egrep '(World$)' newfile 
## OUTPUT
<img width="725" height="98" alt="Screenshot 2025-08-22 145220 5" src="https://github.com/user-attachments/assets/7ef9be86-70c5-46ac-8a68-3b1b6ce6a400" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="772" height="104" alt="Screenshot 2025-08-22 145220 6" src="https://github.com/user-attachments/assets/e016801d-f042-44e5-8288-1b63a43b1195" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="672" height="91" alt="Screenshot 2025-08-22 145220 7" src="https://github.com/user-attachments/assets/8ad7856f-4015-4ab2-912a-87e247e917e3" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="796" height="108" alt="Screenshot 2025-08-22 145220 8" src="https://github.com/user-attachments/assets/2d470068-668a-456d-bd04-1f2d17e0e41a" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="796" height="108" alt="Screenshot 2025-08-22 145220 8" src="https://github.com/user-attachments/assets/e60aae8c-23b1-4a74-a254-df389af28c94" />


egrep l{2} newfile
## OUTPUT
<img width="659" height="89" alt="Screenshot 2025-08-22 145220 9" src="https://github.com/user-attachments/assets/444ae648-2a67-4814-8253-cb1bf8b142c2" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="705" height="95" alt="Screenshot 2025-08-22 145220" src="https://github.com/user-attachments/assets/555f5ee0-e502-4577-8cea-69e41c2fd892" />


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

<img width="673" height="91" alt="Screenshot 2025-08-22 145544" src="https://github.com/user-attachments/assets/31bbe892-e1e9-45eb-b940-6eb00eecab54" />


sed -n -e '$p' file23
## OUTPUT
<img width="689" height="93" alt="Screenshot 2025-08-22 145544 2" src="https://github.com/user-attachments/assets/dd019ab5-f0b3-440f-a0ed-a4bb5b219514" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="764" height="218" alt="Screenshot 2025-08-22 145544 3" src="https://github.com/user-attachments/assets/9845e9b4-1873-4c0b-a85e-1600ff73adc2" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="782" height="211" alt="Screenshot 2025-08-22 145544 4" src="https://github.com/user-attachments/assets/2f9cc4b6-07df-4ac4-8c32-31d2fb74ec6f" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="799" height="211" alt="Screenshot 2025-08-22 145544 5" src="https://github.com/user-attachments/assets/1f483237-5d81-45ec-be7e-bdccd5255789" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="739" height="143" alt="Screenshot 2025-08-22 145544 6" src="https://github.com/user-attachments/assets/fd8ca7f4-a943-441f-87bb-7c5c48752451" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="769" height="122" alt="Screenshot 2025-08-22 145544" src="https://github.com/user-attachments/assets/3b87fb09-c315-47e4-9e82-600f1d62dea7" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="815" height="110" alt="Screenshot 2025-08-22 145556" src="https://github.com/user-attachments/assets/d0164798-16a5-45a1-9e36-778b222a8138" />



seq 10 
## OUTPUT

<img width="515" height="260" alt="Screenshot 2025-08-22 145556 2" src="https://github.com/user-attachments/assets/c6c5b0fc-3218-4b3f-98d3-f4d0c4fe99d6" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="700" height="101" alt="Screenshot 2025-08-22 145556 3" src="https://github.com/user-attachments/assets/0bc1adc8-4a42-4164-b340-edd29b433ca1" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="707" height="112" alt="Screenshot 2025-08-22 145602" src="https://github.com/user-attachments/assets/4959cff1-2223-4620-95c5-8203580abf56" />




seq 3 | sed '2a hello'
## OUTPUT

<img width="724" height="122" alt="Screenshot 2025-08-22 145602 2" src="https://github.com/user-attachments/assets/106796b5-d71a-4c92-a15b-8929882ff278" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="703" height="95" alt="Screenshot 2025-08-22 145602 3" src="https://github.com/user-attachments/assets/0085ff69-b5ec-4fa0-ab04-069fbcc6b8a8" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="728" height="100" alt="Screenshot 2025-08-22 145602 4" src="https://github.com/user-attachments/assets/b42ef8c7-fb9b-4b51-b41d-c89ab1126748" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="777" height="105" alt="Screenshot 2025-08-22 145602 5" src="https://github.com/user-attachments/assets/dd369359-e71d-43ce-8545-4908d1a147ec" />



sed -n '2,4{s/$/*/;p}' file23
# OUTPUT
<img width="794" height="107" alt="Screenshot 2025-08-22 145602" src="https://github.com/user-attachments/assets/70328de9-9cb4-4e3a-a4fa-ff162a33553a" />


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

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

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
