# bash-scripting

### 1. `if...else`
**Explanation:** The `if...else` construct is used for conditional execution of commands based on whether a specified condition evaluates to true or false. This is fundamental for decision-making in scripts.

**Example:**
```bash
#!/bin/bash

read -p "Enter a number: " number

if [ "$number" -gt 0 ]; then
    echo "The number is positive."
elif [ "$number" -lt 0 ]; then
    echo "The number is negative."
else
    echo "The number is zero."
fi
```
*In this example, the user is prompted to enter a number, and the script checks if the number is positive, negative, or zero.*

### 2. `switch...case`
**Explanation:** The `case` statement allows you to execute different commands based on the value of a variable. It’s similar to the `switch` statement in other programming languages and is useful for handling multiple conditions cleanly.

**Example:**
```bash
#!/bin/bash

read -p "Enter a fruit (apple, banana, cherry): " fruit

case $fruit in
    apple)
        echo "You chose an apple."
        ;;
    banana)
        echo "You chose a banana."
        ;;
    cherry)
        echo "You chose a cherry."
        ;;
    *)
        echo "Unknown fruit."
        ;;
esac
```
*This script prompts the user to enter a fruit and responds based on the input, defaulting to "Unknown fruit" for any other input.*

### 3. `for` Loops
**Explanation:** A `for` loop allows you to iterate over a list of items or a range of numbers. It’s useful for executing a block of code multiple times.

**Example:**
```bash
#!/bin/bash

for i in {1..5}; do
    echo "Number: $i"
done
```
*This loop iterates from 1 to 5 and prints each number. It’s a straightforward way to repeat actions.*

### 4. `while` Loops
**Explanation:** A `while` loop continues to execute a block of commands as long as a specified condition is true. It’s useful for situations where the number of iterations isn’t known beforehand.

**Example:**
```bash
#!/bin/bash

count=1
while [ $count -le 5 ]; do
    echo "Count: $count"
    ((count++))
done
```
*In this script, the loop continues until `count` exceeds 5, incrementing `count` each time.*

### 5. `until` Loops
**Explanation:** An `until` loop is the opposite of a `while` loop; it continues until a specified condition becomes true. It’s helpful for situations where you want to repeat until something changes.

**Example:**
```bash
#!/bin/bash

count=1
until [ $count -gt 5 ]; do
    echo "Count: $count"
    ((count++))
done
```
*Here, the loop runs until `count` is greater than 5, similar to the `while` loop but structured differently.*

### 6. Functions
**Explanation:** Functions in Bash are used to group commands into reusable blocks. This helps in organizing code and avoiding repetition.

**Example:**
```bash
#!/bin/bash

function greet {
    echo "Hello, $1!"
}

greet "Alice"
greet "Bob"
```
*In this example, a function named `greet` takes a name as an argument and prints a greeting. It’s called twice with different names, demonstrating reusability.*

### Usage
You can save each example in separate `.sh` files, make them executable with `chmod +x filename.sh`, and run them using `./filename.sh`. These explanations provide context for the concepts and demonstrate how they are used in practical scenarios.
