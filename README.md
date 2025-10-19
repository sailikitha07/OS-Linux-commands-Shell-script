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

![Alt text](img/1.png)



cat < file2
## OUTPUT

![Alt text](img/2.png)

# Comparing Files
cmp file1 file2
## OUTPUT
![Alt text](img/3.png)
 
comm file1 file2
 ## OUTPUT
![Alt text](img/4.png)

 
diff file1 file2
## OUTPUT
![Alt text](img/5.png)


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
![Alt text](img/6.png)




cut -d "|" -f 1 file22
## OUTPUT
![Alt text](img/7.png)



cut -d "|" -f 2 file22
## OUTPUT
![Alt text](img/8.png)


cat > newfile 
```
Hello world
hello world
^d
````
cat <> newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![Alt text](img/9.png)



grep hello newfile 
## OUTPUT
![Alt text](img/10.png)




grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="356" height="57" alt="image" src="https://github.com/user-attachments/assets/e8838c99-70ba-4a74-9cce-a79e30ae7839" />





grep -R ubuntu /etc
## OUTPUT
<img width="815" height="287" alt="image" src="https://github.com/user-attachments/assets/b0f4dd6a-bf7a-42e5-afe4-d743d2fb51fd" />




grep -w -n world newfile   
## OUTPUT
<img width="315" height="86" alt="image" src="https://github.com/user-attachments/assets/3a0d1365-2878-406f-8b23-9f978d863d66" />



cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

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
<img width="423" height="93" alt="image" src="https://github.com/user-attachments/assets/807f34c3-e9ef-4ef7-b8bc-de165c8132fe" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="361" height="117" alt="image" src="https://github.com/user-attachments/assets/81a1a613-11a1-4e93-abd3-bbb6e332f891" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="447" height="116" alt="image" src="https://github.com/user-attachments/assets/b2118ec3-ce06-4ccb-bbb5-900e05a80994" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="350" height="105" alt="image" src="https://github.com/user-attachments/assets/f744205c-dcd8-4155-a1c6-0582bdcd2ffd" />




egrep '(world$)' newfile 
## OUTPUT
<img width="307" height="115" alt="image" src="https://github.com/user-attachments/assets/564332b3-2507-4c7f-9bc8-9d1c9e4b0f8d" />




egrep '(World$)' newfile 
## OUTPUT
<img width="342" height="107" alt="image" src="https://github.com/user-attachments/assets/7a9abbad-bedd-4ec7-bf73-9db3b8f5a6de" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="362" height="118" alt="image" src="https://github.com/user-attachments/assets/3474012c-eede-4798-9853-71e12fabec9a" />




egrep '[1-9]' newfile 
## OUTPUT
<img width="318" height="63" alt="image" src="https://github.com/user-attachments/assets/6f79576f-7ed6-4656-8e75-f2fa30fdd55e" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="408" height="47" alt="image" src="https://github.com/user-attachments/assets/12179a24-93a7-4765-b5f6-1473537b4fae" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="371" height="88" alt="image" src="https://github.com/user-attachments/assets/0001564b-aa71-44ec-9b73-758594b2a575" />



egrep l{2} newfile
## OUTPUT
<img width="331" height="107" alt="image" src="https://github.com/user-attachments/assets/7e3b505d-1327-4b2a-98b5-540c1f286dde" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="426" height="127" alt="image" src="https://github.com/user-attachments/assets/a4656b13-6ed5-4bc3-ba35-e02620106242" />



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
<img width="312" height="88" alt="image" src="https://github.com/user-attachments/assets/dd848b0a-4940-4da9-9ca9-6e1954b5df95" />




sed -n -e '$p' file23
## OUTPUT
<img width="327" height="93" alt="image" src="https://github.com/user-attachments/assets/8d85c6c8-8f13-4607-8073-2f69cb6b8995" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="460" height="242" alt="image" src="https://github.com/user-attachments/assets/d405679e-511c-4e23-96d1-c101c58727a8" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="441" height="243" alt="image" src="https://github.com/user-attachments/assets/b46f34ee-03de-4bd1-a845-c19da96a9c67" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="457" height="246" alt="image" src="https://github.com/user-attachments/assets/7f1b7da2-484d-45b2-928a-b652ec9f67f2" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="432" height="177" alt="image" src="https://github.com/user-attachments/assets/47558330-1044-40a6-8a72-5385140d663b" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="413" height="102" alt="image" src="https://github.com/user-attachments/assets/ad154da8-4700-49fb-95fe-f2e6d47023d6" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="395" height="127" alt="image" src="https://github.com/user-attachments/assets/8795f376-db27-449c-90b7-8997c5d2ccdd" />




seq 10 
## OUTPUT
<img width="427" height="287" alt="image" src="https://github.com/user-attachments/assets/1aaff8d5-3b47-4b00-98c4-17c4464146d5" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="417" height="143" alt="image" src="https://github.com/user-attachments/assets/2e1ff077-4784-434a-bbc5-f48f425b7110" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="397" height="135" alt="image" src="https://github.com/user-attachments/assets/eda21db0-0826-4731-95cb-360c72a418c4" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="445" height="167" alt="image" src="https://github.com/user-attachments/assets/4b316181-a857-4a90-9227-d2c47719d0ff" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="340" height="145" alt="image" src="https://github.com/user-attachments/assets/374c88ce-b822-4c84-aa7b-9eebee0aae99" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="370" height="126" alt="image" src="https://github.com/user-attachments/assets/cb35e80b-cacf-405a-85aa-710ecfab0cab" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="423" height="153" alt="image" src="https://github.com/user-attachments/assets/5f665200-d093-4035-822b-1a2afaf7235a" />




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
<img width="362" height="176" alt="image" src="https://github.com/user-attachments/assets/013e5265-b3c0-45b6-a531-9ac4e9b09482" />



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
<img width="338" height="162" alt="image" src="https://github.com/user-attachments/assets/65e0588d-e5f9-4aec-807c-a925ded70467" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="423" height="237" alt="image" src="https://github.com/user-attachments/assets/a7c23b5e-915c-400b-8c70-31e8b152a52d" />


cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat <> urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
 <img width="436" height="127" alt="image" src="https://github.com/user-attachments/assets/0219b240-b672-4522-b190-7f5428e7462a" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="442" height="141" alt="image" src="https://github.com/user-attachments/assets/28999831-d3a1-47e2-a70d-2ac916fe3b52" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="332" height="283" alt="image" src="https://github.com/user-attachments/assets/91e3bc3a-9208-409e-8da1-e97c0780c982" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="717" height="285" alt="image" src="https://github.com/user-attachments/assets/e0d31e57-11c4-4093-a1cb-490f7e600479" />



tar -xvf backup.tar
## OUTPUT
<img width="283" height="275" alt="image" src="https://github.com/user-attachments/assets/b79e05da-61e2-4d58-b2c7-95bbfb5ffad4" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="166" height="87" alt="image" src="https://github.com/user-attachments/assets/b62ed80e-f44f-4832-8803-67695569886e" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="181" height="105" alt="image" src="https://github.com/user-attachments/assets/695f084a-d620-41da-89ac-fbb04de6f47c" />

cd ..
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World; exit 0' >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="517" height="176" alt="image" src="https://github.com/user-attachments/assets/acbd6ccf-5210-461d-ab8e-47ef57abb63b" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="373" height="141" alt="image" src="https://github.com/user-attachments/assets/57660ed0-3955-42f4-a068-e3a96ccaaf8e" />



cat > scriptest.sh 
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
<img width="655" height="487" alt="image" src="https://github.com/user-attachments/assets/24900552-c0c4-4830-ab68-313fc839256c" />


 
ls file1
## OUTPUT
<img width="197" height="90" alt="image" src="https://github.com/user-attachments/assets/9edd6e2e-4e95-44c6-91ce-57199d75725e" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
 <img width="237" height="112" alt="image" src="https://github.com/user-attachments/assets/ff0e827e-2e39-43a8-9353-845fb35bfddf" />



 
# mis-using string comparisons

cat > strcomp.sh 
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
<img width="337" height="257" alt="image" src="https://github.com/user-attachments/assets/b095d571-46aa-477e-bd4a-0daba35a31c1" />



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

 chmod 755 psswdperm.sh
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

chmod 755 ifnested.sh

./ifnested.sh 
## OUTPUT
<img width="671" height="182" alt="image" src="https://github.com/user-attachments/assets/e1abfb77-bb91-4330-95f1-9a1c379a2802" />




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

chmod 755 iftest.sh

 
 ./iftest.sh 

 
##OUTPUT

<img width="602" height="147" alt="image" src="https://github.com/user-attachments/assets/23c4f747-07ec-4b2d-bda1-aa7a686f964f" />


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
```

 chmod 755 ifnested.sh

 
 ./ifnested.sh 
##OUTPUT

<img width="570" height="162" alt="image" src="https://github.com/user-attachments/assets/b23634d5-e14e-42a6-bc3b-b44c8e5676a9" />


# looking for a possible value using elif
cat > elifcheck.sh 
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

chmod 755 elifcheck.sh
 
 ./elifcheck.sh 
## OUTPUT
<img width="667" height="138" alt="image" src="https://github.com/user-attachments/assets/b2a91ee7-afe7-49d1-8957-4ab162f91bcd" />



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

chmod 755 ifcompound.sh

 ./ifcompound.sh 
## OUTPUT
<img width="597" height="140" alt="image" src="https://github.com/user-attachments/assets/90d451ed-f2cd-4ee6-b835-003a9f043d11" />


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
 chmod 755 casecheck.sh 
<img width="431" height="101" alt="image" src="https://github.com/user-attachments/assets/10e3500e-ae71-43ec-98c9-0707f0142633" />

 
 ./casecheck.sh 
 
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
 chmod 755 whiletest.sh
 
 ./whiletest.sh
<img width="337" height="300" alt="image" src="https://github.com/user-attachments/assets/bce3d36a-9de6-43dd-abd7-fdba3409feb5" />

 
 
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
chmod 755 untiltest.sh

./untiltest.sh
<img width="351" height="163" alt="image" src="https://github.com/user-attachments/assets/cbde6664-d464-478e-9c65-c18f0cc3d9c6" />

 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
 chmod 755 forin1.sh
<img width="293" height="202" alt="image" src="https://github.com/user-attachments/assets/8c01b599-ee33-4eaa-9b48-039092ec330c" />

./forin1.sh 
 
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
 chmod 755 forin2.sh
 
 ./forin2.sh 
 
cat > forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

chmod 755 forin3.sh
 ./forin3.sh 
## Output
<img width="371" height="220" alt="image" src="https://github.com/user-attachments/assets/c523032a-6f70-4cd2-8bda-f23a91bf1b11" />

 
cat > forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
 chmod 755 forin1.sh

./forin1.sh
## OUTPUT
cat > forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
 chmod 777 forinfile.sh
 cat > cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam


cat cities
## OUTPUT
<img width="446" height="370" alt="image" src="https://github.com/user-attachments/assets/00f82773-6fe0-4bba-a674-cfc24a2455e9" />



cat > forctype.sh 
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
<img width="343" height="198" alt="image" src="https://github.com/user-attachments/assets/2b049db1-5069-4aef-8a98-61e99f62ec70" />


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
 chmod 755 forctype.sh
./forctype1.sh 
## OUTPUT
<img width="337" height="181" alt="image" src="https://github.com/user-attachments/assets/62a893b6-bb52-4a64-bd45-07a4d881a94d" />


cat > fornested1.sh 
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
chmod 755 fornested1.sh
 
 ./fornested1.sh 
 ## OUTPUT
 <img width="377" height="326" alt="image" src="https://github.com/user-attachments/assets/63d163e7-3931-495c-a107-4db6dd53528a" />


 
cat > forbreak.sh 
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


 chmod 755 forbreak.sh
 
 ./forbreak.sh 


## OUTPUT
<img width="502" height="172" alt="image" src="https://github.com/user-attachments/assets/8773591b-d8c3-4f40-b0ec-1cb8543071d8" />


 
cat > forbreak.sh 
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

 
 chmod 755 forcontinue.sh
 
 ./forcontinue.sh 
## OUTPUT
<img width="471" height="200" alt="image" src="https://github.com/user-attachments/assets/7ca6e6cd-9ffe-4d7a-a8d1-3ee1fc2271b5" />

 
cat > exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
 chmod 755 exread.sh 
 
 ./exread.sh 
## OUTPUT
<img width="455" height="137" alt="image" src="https://github.com/user-attachments/assets/3e4b50d2-15b0-4021-93c9-64f65f51b592" />



 cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
 chmod 755 exread1.sh 



 ./exread1.sh 

 ## OUTPUT
<img width="275" height="148" alt="image" src="https://github.com/user-attachments/assets/149bf4c4-4d74-4d2c-8175-f92ec033f950" />


 
cat > funcex.sh
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
chmod 755 funcex.sh

 ./funcex.sh


./funcex.sh 1 2
## OUTPUT
 
 <img width="300" height="156" alt="image" src="https://github.com/user-attachments/assets/9a95c929-8b98-4af9-97bb-1cca28d0499d" />


 
 

 
cat > argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
 chmod 777 argshift.sh

./argshift.sh 1 2 3

## OUTPUT
<img width="372" height="186" alt="image" src="https://github.com/user-attachments/assets/d4414d6f-f13e-4355-a603-532c67e12969" />

 
 
 cat > argshift1.sh
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
 chmod 777 argshift.sh

./argshift.sh 1 2 3

## OUTPUT
<img width="300" height="146" alt="image" src="https://github.com/user-attachments/assets/8afbc132-016c-4769-ba24-1271228cc0bb" />

 
 
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

chmod 755 argshift.sh
./argshift.sh 1 2 3
## OUTPUT
<img width="382" height="388" alt="image" src="https://github.com/user-attachments/assets/b311b300-fb90-43e9-bd6a-56873049a0e4" />

 
 
 
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
 <img width="380" height="330" alt="image" src="https://github.com/user-attachments/assets/e482fa2c-68ed-484e-82ec-2cf963c98cef" />

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

chmod 777 palindrome.sh

./palindrome.sh
## OUTPUT 
<img width="367" height="148" alt="image" src="https://github.com/user-attachments/assets/d441f209-8c5a-48be-8480-4e6a05fce048" />



# RESULT:
The Commands are executed successfully.
