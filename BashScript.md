Bash (Bourne Again SHell) is a command language interpreter for Unix/Linux.

Scripts are just text files with commands.

To create:

#!/bin/bash
echo "Hello, World!"


Make executable:

chmod +x script.sh


🟢 2️⃣ Variables

Declare variable

name="John"

age=25


Access variable

echo "Name: $name"

echo "Age: $age"

Command substitution

today=$(date)

echo "Today is $today"

🟢 3️⃣ Conditionals (if, else, elif)

#!/bin/bash
num=10

if [ $num -gt 5 ]; then
  echo "Number is greater than 5"
elif [ $num -eq 5 ]; then
  echo "Number is equal to 5"
else
  echo "Number is less than 5"
fi


Operators

| Type             | Example |
| ---------------- | ------- |
| Equal            | `-eq`   |
| Not equal        | `-ne`   |
| Greater          | `-gt`   |
| Less             | `-lt`   |
| String equal     | `=`     |
| String not equal | `!=`    |
| File exists      | `-e`    |


🟢 4️⃣ Loops

For loop

for i in 1 2 3 4 5
do
  echo "Number $i"
done


For loop with C-style

for ((i=1; i<=5; i++))
do
  echo "Number $i"
done


While loop

count=1
while [ $count -le 5 ]
do
  echo "Count $count"
  ((count++))
done

Until loop

num=1
until [ $num -gt 5 ]
do
  echo "Until $num"
  ((num++))
done


🟢 5️⃣ Case statement

read -p "Enter a character: " char

case $char in
  [a-z])
    echo "Lowercase letter";;
  [A-Z])
    echo "Uppercase letter";;
  [0-9])
    echo "Digit";;
  *)
    echo "Other character";;
esac


🟢 6️⃣ Arrays


fruits=("apple" "banana" "cherry")
echo "${fruits[0]}"      # apple
echo "${fruits[@]}"      # all elements

# Iterate
for fruit in "${fruits[@]}"
do
  echo "$fruit"
done



🟢 7️⃣ Functions (like methods)

greet() {
  echo "Hello, $1!"
}

greet "Alice"

outside source filename.sh...ect
 then greet Ebin

🟢 8️⃣ Command line arguments


#!/bin/bash
echo "Script name: $0"
echo "First arg: $1"
echo "Second arg: $2"
echo "Total args: $#"
echo "All args: $@"



🟢 9️⃣ Reading user input

read -p "Enter your name: " username
echo "Hello $username"

