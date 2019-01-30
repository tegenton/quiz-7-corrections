# quiz-7-corrections

## Question 8
*I need to populate an ArrayList of Integers that will represent each of the perfect squares between 1 and 10. Which of the following code segments below accomplishes that task? Select all that apply.*

```java
ArrayList<Integer> perfectSquares = new ArrayList<Integer>();

int i = 1;
while (i <= 10) {
    perfectSquares.add(i, i * i);
    i++;
}
```
This answer uses the arraylist add method, which I thought used indexes starting at 0. This iterator starts at 1, which made me think it would be incorrect.

```java
ArrayList<Integer> perfectSquares = new ArrayList<Integer>();

for (int i = 1; i <= 10; i++) {
    perfectSquares.set(i, (i * i));
}
```

This answer uses the arraylist set method, which I thought used indexes starting at 0. This iterator starts at 1, which made me think it would be incorrect.

## Question 9

*Consider the following code segment, which is intended to swap two values in an ArrayList. You can assume the ArrayList and the variables x and y are correctly declared and initialized.*

```java
list.set(y, list.set(x, list.get(y));
```
This answer uses both get and set to return the current value. This would allow the values to be swapped in one line, instead of setting all the values to `list.get(y)`

```java
String temp = list.set(x, list.get(y);
list.set(y, temp);
```
This answer would not compile, as it is missing a parenthesis. Ignoring that, it again uses the set method to return the current value.

## Question 10

*Which method(s) of the ArrayList class is being called in the code segment below?*
```java
ArrayList<String> names = new ArrayList<String>();

names.add("Paul");
names.remove(0);

System.out.println("There are " + names.size() + " elements in the ArrayList.");
```
*Select all that apply.*

Incorrect: *The `ArrayList` default constructor.*
In my opinion, constructors are methods, but (they are different in some respects)[https://stackoverflow.com/questions/3646461/can-i-say-a-constructor-is-a-method]

## Question 13
*Consider the following code segment, which is designed to print only those values in an array that are multiples of 5.*
```java
for (int i = 0; i < numbers.size(); i++) {
    if (numbers.get(i) % 5 == 0) {
        System.out.println(numbers.get(i));
    }
}
```
*Which of the following code snippets represents the equivalent behavior? You may assume (in both the question and answer options) that numbers is properly declared and initialized. Select all that apply.*

```java
numbers.forEach((number) -> System.out.println(number));
```
This answer is incorrect.

## Question 15
*Both usages of the remove method (i.e., by index and by value) automatically manage the shifting of elements to preserve order.*

Incorrect: *This statement is partially true. Removals by index automatically preserve order, but removals by value do not.*

Correct: *This statement is true.*

The remove by value method does not change the order of the arrayList. Removal by index also maintains the order of the list.
