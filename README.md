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

# The value, 6 indicates the starting point from where the substring will start and 5 indicates the length of the substring. 


Str="Learn Greek in 30 minutes"
subStr=${Str:6:5}
echo $subStr

```
----------------------------------------



