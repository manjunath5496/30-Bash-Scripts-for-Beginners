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
# Multiply two numeric value
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
