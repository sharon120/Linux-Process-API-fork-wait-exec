# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

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

![Screenshot 2024-09-19 082329](https://github.com/user-attachments/assets/5fb58ed7-8b27-4209-8d91-964fec6b693b)


cat < file2
## OUTPUT
![Screenshot 2024-09-22 180349](https://github.com/user-attachments/assets/07e46f59-90b2-48a6-b7b4-fef37731515f)

# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2024-09-22 180357](https://github.com/user-attachments/assets/23ae9ba2-c4ed-45f8-9f1f-3ee1017b099f)
 
comm file1 file2
 ## OUTPUT
![Screenshot 2024-09-22 180405](https://github.com/user-attachments/assets/55461898-28e3-473f-a67a-c4a1844479f3)

 
diff file1 file2
## OUTPUT
![Screenshot 2024-09-22 180417](https://github.com/user-attachments/assets/c6117101-fd29-40e3-9bf4-6b0ce2d6deb3)


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

![Screenshot 2024-09-22 180608](https://github.com/user-attachments/assets/c30fffc6-3f81-4dac-8786-2650bacef6d7)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/460afefc-ff7d-4c95-8671-af98c1523eb2)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/573dd7de-070a-42e0-810d-d89cc894ed32)
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

![image](https://github.com/user-attachments/assets/347b0a9c-e9ed-4db3-bb26-81e4fc6c7c2a)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/e40693e2-5ac4-4dee-9e4a-4f38cd888192)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/6df4f059-bba7-4b3f-aad0-93b28e5112cc)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/cbc169c1-c6b7-42a7-abcf-6ca74d559a98)
cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/b805a818-3ac8-4bbd-bdf7-2deeb10859dc)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/577acb49-e483-4eaf-8cdd-2c33623f4dbd)


grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/c664a815-fab5-4ad9-9e87-e837a04ff297)


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

![image](https://github.com/user-attachments/assets/b9b64153-a7db-4859-ab14-35fe39776568)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/cb889fd6-400d-41f6-b8a1-696c814863c9)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/2c31fa0d-57f1-4488-827f-730fb5de1f9c)



egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4e3e2260-80ed-4494-8244-e577fa8b86c2)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/4e8b1875-ebbb-40cc-ad5e-d0a4841dd7a2)



egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/643566af-be83-4d83-a1b0-b8269040a9f0)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d77d7602-c874-4367-ab32-c2c306cdcc5a)



egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/cd57fb1b-c93c-4ddd-bf9a-89d7cad71ca4)



egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/bed797bf-22cf-4d92-900a-8027044a6ac0)

egrep 'Linux.*World' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/c5ec778e-cc73-41e6-94cc-ed93d4274cab)

egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/03ef8a4f-b573-48a0-9316-a6ed349b743b)


egrep 's{1,2}' newfile
## OUTPUT 

![image](https://github.com/user-attachments/assets/d080802c-00b3-4b1d-8017-9dacc20fd97e)

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

![image](https://github.com/user-attachments/assets/ebdf1546-08b8-44ec-8e8b-2a6cd8806be8)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/d4f959a1-29f7-4495-b8c8-6c47f108bef5)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/aefa6510-7a0c-4c23-bfdb-c77a5e25f347)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/13cfe44d-8061-485f-9764-bbd7ec6f619e)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/2ec052e7-7aa7-465b-9f01-4db6e6ddcb26)


sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/374d45b3-bc6c-4c9e-8b4d-9ac14895859b)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/a18745e6-a379-4fad-887f-d11020f1a2d2)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/9862ffdd-97ca-403c-a3b7-66001c0f671f)


seq 10 
## OUTPUT

![image](https://github.com/user-attachments/assets/c90d2f02-b346-48e7-a50d-a3be24a6a8c7)


seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/d53ac535-6b9d-4af1-b076-3e3bfd804d12)

seq 10 | sed -n '2,~4p'
## OUTPUT


![image](https://github.com/user-attachments/assets/227d9fd3-c08b-4094-a271-dab1786efa2d)

seq 3 | sed '2a hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/814d5fc7-3b0b-4594-b44a-ea5689137b89)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/93b881d6-0be7-4f6e-ae44-a2c7d418e8b1)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/9a34ba1d-6099-4efb-a799-eea6ce347a3c)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/17981bb1-8abd-4e4d-a4de-c4cbe7686f58)



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
![image](https://github.com/user-attachments/assets/6a5a74da-5a7b-4f01-b8db-816a1abd9739)


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

![image](https://github.com/user-attachments/assets/9d56c49a-7b11-4edd-b656-5f8841375880)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/7164b017-68f1-44c3-975e-9754509e3aa4)

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

![image](https://github.com/user-attachments/assets/9b20e061-68ca-4e3b-be64-0bcb208f9c63)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/ea79fff9-d4b7-42ca-99c9-b2d02afb633e)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

  
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
![image](https://github.com/user-attachments/assets/d7eb0372-2b07-481c-a71d-d5e07588d89b)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/f7eaf7e1-adf6-4d73-a9b6-4c561c869ea0)


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
![image](https://github.com/user-attachments/assets/097b4fb1-5045-4dfe-accc-8327c40c20e6)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/d70c42ab-11f0-4002-8852-bbb3f8cce5c7)

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

![image](https://github.com/user-attachments/assets/48eccb3b-d5cb-44c5-8ed0-811f949a4909)


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

![image](https://github.com/user-attachments/assets/d23d1db8-e4e7-4adc-9bfc-db3c699085e2)


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
![image](https://github.com/user-attachments/assets/fc215d87-3568-4e1b-9afd-290b212dddc8)

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
![image](https://github.com/user-attachments/assets/1c27affe-682b-4f82-8cb1-7e16c5f974f7)

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
![image](https://github.com/user-attachments/assets/90b3017a-0194-4cc4-801b-6184581a26d8)

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

	

# RESULT:
The Commands are executed successfully.

 
