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

<img width="258" height="147" alt="Screenshot 2025-08-30 141709" src="https://github.com/user-attachments/assets/b1601af9-fefc-4394-85b1-4c3aadf22c49" />


cat < file2
## OUTPUT

<img width="255" height="176" alt="Screenshot 2025-08-30 142311" src="https://github.com/user-attachments/assets/2c3547d1-a22b-4f9d-a78d-755c9c90f044" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="322" height="223" alt="Screenshot 2025-08-30 142620" src="https://github.com/user-attachments/assets/890892af-645e-42ca-97c0-d2d046f72925" />

comm file1 file2
 ## OUTPUT

 <img width="367" height="77" alt="Screenshot 2025-08-30 142759" src="https://github.com/user-attachments/assets/611b7a77-4d0a-4427-838b-e9652b958b64" />

diff file1 file2
## OUTPUT

<img width="306" height="230" alt="Screenshot 2025-08-30 142820" src="https://github.com/user-attachments/assets/6ca6dafd-6396-4cff-a685-f3cad9c9e450" />

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

<img width="291" height="270" alt="Screenshot 2025-08-30 142941" src="https://github.com/user-attachments/assets/b3e9634b-f6c0-4ae7-8380-6be73824bf99" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="303" height="107" alt="Screenshot 2025-08-30 143354" src="https://github.com/user-attachments/assets/d685b20b-8e95-4bbc-812a-2b2cdddb0ef1" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="312" height="130" alt="Screenshot 2025-08-30 143455" src="https://github.com/user-attachments/assets/434bd74f-096b-42f9-9539-10156fad747d" />

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

<img width="298" height="118" alt="Screenshot 2025-08-30 143559" src="https://github.com/user-attachments/assets/a9aa6047-c7fb-4186-b0ae-b488d26be802" />


grep hello newfile 
## OUTPUT

<img width="169" height="56" alt="Screenshot 2025-08-30 144255" src="https://github.com/user-attachments/assets/048be923-9579-4967-a670-1fa37ffa4e1a" />



grep -v hello newfile 
## OUTPUT

<img width="312" height="99" alt="Screenshot 2025-08-30 144310" src="https://github.com/user-attachments/assets/28f61b23-839d-42b6-878c-943fcb146cfc" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="255" height="80" alt="Screenshot 2025-08-30 144400" src="https://github.com/user-attachments/assets/ffe792fc-0066-4b32-8f35-49c68ab1d0de" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="290" height="110" alt="Screenshot 2025-08-30 144456" src="https://github.com/user-attachments/assets/36b39766-501f-43f8-995c-b77ef93dc943" />


grep -R ubuntu /etc
## OUTPUT

<img width="362" height="127" alt="Screenshot 2025-08-30 144531" src="https://github.com/user-attachments/assets/04914ac8-c203-4824-8ef3-8f09ca84d5f9" />


grep -w -n world newfile   
## OUTPUT

<img width="408" height="78" alt="Screenshot 2025-08-30 144601" src="https://github.com/user-attachments/assets/36cc3cad-9fd9-4522-bbb3-7e1507c8c311" />

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

<img width="942" height="651" alt="Screenshot 2025-08-30 144729" src="https://github.com/user-attachments/assets/39ea4734-27bc-4352-b4ee-ae0e2d2291e6" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="327" height="103" alt="Screenshot 2025-08-30 144800" src="https://github.com/user-attachments/assets/4fb56ab5-f59c-4493-bebf-fdd420e98217" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="380" height="101" alt="Screenshot 2025-08-30 145119" src="https://github.com/user-attachments/assets/7f8bb794-373b-41c5-9b04-bdfec6358c38" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="325" height="72" alt="Screenshot 2025-09-11 143154" src="https://github.com/user-attachments/assets/68ea56d9-1e3e-4b12-a9ee-ce11dce8c357" />


egrep '(world$)' newfile 
## OUTPUT

<img width="314" height="100" alt="Screenshot 2025-09-11 143220" src="https://github.com/user-attachments/assets/1f5adbfe-35b1-44e3-b8ee-ec18f8189137" />


egrep '(World$)' newfile 
## OUTPUT

<img width="330" height="74" alt="Screenshot 2025-09-11 143249" src="https://github.com/user-attachments/assets/41d3634c-5fa7-475e-8783-abee6b5fc7aa" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="360" height="125" alt="Screenshot 2025-09-11 143312" src="https://github.com/user-attachments/assets/79e964ca-577c-4478-bee3-0c4fe4d90137" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="297" height="83" alt="Screenshot 2025-09-11 143339" src="https://github.com/user-attachments/assets/7697ab40-c79e-4f50-bdde-b67421af698a" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="357" height="74" alt="Screenshot 2025-09-11 143415" src="https://github.com/user-attachments/assets/222d8469-c43d-40ac-9c9c-2efbda89bb5e" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="351" height="81" alt="Screenshot 2025-09-11 143451" src="https://github.com/user-attachments/assets/721bae64-6363-430f-8f7f-c479691d078c" />

egrep l{2} newfile
## OUTPUT

<img width="266" height="96" alt="Screenshot 2025-09-11 143526" src="https://github.com/user-attachments/assets/856792d8-ae86-4c60-931a-167e5c2a4e6b" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="299" height="131" alt="Screenshot 2025-09-11 143603" src="https://github.com/user-attachments/assets/bdbdad68-d2b5-4962-86a4-0fc9dd4b0182" />

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

<img width="328" height="64" alt="Screenshot 2025-09-11 144128" src="https://github.com/user-attachments/assets/890e0d1d-cffc-4f82-8a4a-179a86e2571d" />


sed -n -e '$p' file23
## OUTPUT

<img width="328" height="64" alt="Screenshot 2025-09-11 144128" src="https://github.com/user-attachments/assets/174b2c75-4539-4536-9a37-5b22c1f80a28" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="354" height="268" alt="image" src="https://github.com/user-attachments/assets/cc0db8c1-a78b-49f8-86d4-59149f31c64c" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="372" height="263" alt="image" src="https://github.com/user-attachments/assets/ef01b229-1877-470b-a465-165e09d12ce2" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="416" height="272" alt="image" src="https://github.com/user-attachments/assets/e874e759-85eb-4090-bac6-4226f712f61c" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="327" height="190" alt="image" src="https://github.com/user-attachments/assets/c6eab766-7c28-4667-8908-6502d2b4d403" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="396" height="133" alt="image" src="https://github.com/user-attachments/assets/8ca64789-69d6-4abf-a29d-5b0fc788313f" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="385" height="105" alt="image" src="https://github.com/user-attachments/assets/2ddd54d5-2e89-49bb-bceb-3bb624a782e7" />


seq 10 
## OUTPUT

<img width="337" height="303" alt="image" src="https://github.com/user-attachments/assets/d6169b3a-9f28-41a1-840d-d911fc6397fa" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="294" height="131" alt="image" src="https://github.com/user-attachments/assets/7639c8b3-eee7-458b-9f14-cb6ef6e003bf" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="317" height="138" alt="image" src="https://github.com/user-attachments/assets/b189a62f-e982-42c2-a512-494dcad61852" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="376" height="155" alt="image" src="https://github.com/user-attachments/assets/778193a2-0399-4d11-affa-5ccce9b21435" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="304" height="134" alt="image" src="https://github.com/user-attachments/assets/fcf79793-b9fe-4146-9971-5014d645255e" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="320" height="126" alt="image" src="https://github.com/user-attachments/assets/8d5011fb-4800-4d40-adba-42b2c2bdd285" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="390" height="123" alt="image" src="https://github.com/user-attachments/assets/07a8808b-ee10-4dff-834c-c2bb34ee6f58" />


sed -n '2,4{s/$/*/;p}' file23

<img width="372" height="135" alt="image" src="https://github.com/user-attachments/assets/287ef9c8-97ee-42da-8899-9fcb4fa59152" />

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

<img width="367" height="207" alt="image" src="https://github.com/user-attachments/assets/4b5850a6-4121-44a5-b7cc-20957751562d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="452" height="279" alt="image" src="https://github.com/user-attachments/assets/14652a54-8f4d-4487-a31e-5f9f5a08c63e" />


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
