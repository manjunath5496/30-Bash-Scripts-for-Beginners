# 30 Bash Scripts for Beginners

### **01. Hello World:**

---------------------------------------


```bash
# The following Bash script will print the text "Hello World!" as output.

echo "Hello World"
```
----------------------------------------
### **02. Echo Command:**

---------------------------------------


```bash
echo "Printing text with newline"
echo -n "Printing text without newline"
echo -e "\nRemoving \t backslash \t characters\n"
```
----------------------------------------
### **03. Comments:**

---------------------------------------


```bash
# Multiply two numeric values
((product=5*3))

#Print the result
echo $product
```
----------------------------------------
### **04. Multi-line comment:**

---------------------------------------


```bash
: '
The following script calculates
the cube value of the number, 2.
'
((x=2*2*2))
echo $x

```
----------------------------------------
### **05. While Loop:**

---------------------------------------


```bash
x=true
count=1
while [ $x ]
do
echo $count
if [ $count -eq 6 ];
then
break
fi
((count++))
done

```
----------------------------------------
### **06. For Loop:**

---------------------------------------


```bash
# for loop will iterate for 10 times and print all values of the variable, x in single line.
for (( x=10; x>0; x-- ))
do
echo -n "$x "
done
printf "\n"

```
----------------------------------------
### **07. Get User Input:**

---------------------------------------


```bash
echo "Enter Your Name"
read name
echo "Welcome $name to Myw3schools.com"


```
----------------------------------------
### **08. If statement:**

---------------------------------------


```bash
x=9
if [ $x -lt 10 ];
then
echo "It is a one digit number"
else
echo "It is a two digit number"
fi

```
----------------------------------------


### **09. And Condition if statement:**

---------------------------------------


```bash
echo "Enter username"
read username
echo "Enter password"
read password

if [[ ( $username == "manju" && $password == "123" ) ]]; then
echo "valid user"
else
echo "invalid user"
fi


```
----------------------------------------

### **10. Or Condition if statement:**

---------------------------------------


```bash

echo "Enter any number"
read x

if [[ ( $x -eq 12 || $x  -eq 56 ) ]]
then
echo "your guess is correct"
else
echo "your guess is wrong"
fi


```
----------------------------------------


### **11. Else if and else condition:**

---------------------------------------


```bash

echo "Enter any number"
read x

if [ $x -eq 4 ];
then
echo "You won the first place"
elif [ $x -eq 20 ];
then
echo "You won the second place"
elif [ $x -eq 840 ];
then
echo "You won the third place"

else
echo "Sorry, try again next time"
fi

```
----------------------------------------
### **12. Case Condition:**

---------------------------------------


```bash
echo "Enter any number"
read x
case $x in
4)
echo echo "You won the first place" ;;
20)
echo "You won the second place" ;;
840)
echo "You won the third place" ;;
*)
echo "Sorry, try again next time" ;;
esac

```
----------------------------------------


### **13. Get Arguments from Command Line:**

---------------------------------------


```bash
echo "Total arguments : $#"
echo "First Argument = $1"
echo "Second argument = $2"


```
----------------------------------------

### **14. Get arguments from command line with names:**

---------------------------------------


```bash

for arg in "$@"
do
index=$(echo $arg | cut -f1 -d=)
val=$(echo $arg | cut -f2 -d=)
case $index in
X) x=$val;;

Y) y=$val;;

*)
esac
done
((result=x+y))
echo "X+Y=$result"



```
----------------------------------------


### **15. Combine two strings in a variable:**

---------------------------------------


```bash

x="Red Hat"
y="Linux"
echo "$x$y"
z=$x+$y
z+=" was a widely used Linux distribution until its discontinuation in 2004."
echo $z

```
----------------------------------------

### **16. Get Substring of Strings:**

---------------------------------------


```bash

# The value, 6 indicates the starting point from where the substring will start 
# and 5 indicates the length of the substring. 


Str="Learn Greek in 30 minutes"
subStr=${Str:6:5}
echo $subStr

```
----------------------------------------

### **17. Muliply 2 numbers into a variable:**

---------------------------------------


```bash

echo "Enter any number"
read a
echo "Enter any number"
read b
(( product=a*b ))
echo "The result of multiplication=$product"

```
----------------------------------------

### **18. Create a Function:**

---------------------------------------


```bash

function G2()
{
echo 'Bash is a Unix shell and command language.'
}

G2

```
----------------------------------------

### **19. Use Function Parameters:**

---------------------------------------


```bash

Rectangle_Volume() {
volume=$(($1 * $2 * $3))
echo "Volume is : $volume"
}

Rectangle_Volume 20 40 30

```
----------------------------------------


### **20. Pass Return Value from Script:**

---------------------------------------


```bash

function welcome() {

str="Hi, $name"
echo $str

}

echo "Enter your name"
read name

val=$(welcome)
echo "Return value of the function is $val"
```
----------------------------------------

### **21. Make directory:**

---------------------------------------


```bash

echo "Enter directory name"
read newdir
`mkdir $newdir`

```
----------------------------------------

### **22. Make directory by checking existence:**

---------------------------------------


```bash

echo "Enter directory name"
read ndir
if [ -d "$ndir" ]
then
echo "Directory exist"
else
`mkdir $ndir`
echo "Directory created"
fi

```
----------------------------------------

### **23. Read a file:**

---------------------------------------


```bash

file='1.txt'
while read line; do
echo $line
done < $file

```
----------------------------------------

### **24. Delete a File:**

---------------------------------------


```bash

echo "Enter filename to remove"
read fn
rm -i $fn

```
----------------------------------------


### **25. Append to file:**

---------------------------------------


```bash

echo "Before appending the file"
cat 1.txt

echo "Learning Red Hat Linux">> 1.txt
echo "After appending the file"
cat 1.txt

```
----------------------------------------

### **26. Test if File Exists:**

---------------------------------------


```bash

filename=$1
if [ -f "$filename" ]; then
echo "File exists"
else
echo "File does not exist"
fi

```
----------------------------------------

### **27. Send Email Example:**

---------------------------------------


```bash

Recipient="admin@example.com"
Subject="Greeting"
Message="Welcome to our Website"
`mail -s $Subject $Recipient <<< $Message`

```
----------------------------------------


### **28. Get Parse Current Date:**

---------------------------------------


```bash

Year=`date +%Y`
Month=`date +%m`
Day=`date +%d`
Hour=`date +%H`
Minute=`date +%M`
Second=`date +%S`
echo `date`
echo "Current Date is: $Day-$Month-$Year"
echo "Current Time is: $Hour:$Minute:$Second"

```
----------------------------------------

### **29. Wait Command:**

---------------------------------------


```bash

echo "Wait command" &
process_id=$!
wait $process_id
echo "Exited with status $?"

```
----------------------------------------

### **30. Sleep Command:**

---------------------------------------


```bash

echo "Wait for 5 seconds"
sleep 5
echo "Completed"

```
----------------------------------------



