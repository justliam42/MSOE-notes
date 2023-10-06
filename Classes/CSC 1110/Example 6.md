## 1. 
Write a method countToTen that will use a for loop to count from 1 to 10, incrementing a local variable ten inside the loop, then return ten. Here is a buggy version of the method:
```java
public int countToTen() {
    int ten = 0;
    for(int i = 0; i < 10; i +=2) {
        ++ten;
    }
    return ten;
}```
First Impressions:
The result will not be ten because the incrementor adds two, so by the time i becomes 10, the loop will have only executed 5  times.

ChatGPT says: 
The Java code you provided appears to be correct and should work as expected. It defines a method `countToTen` that initializes an integer variable `ten` to 0 and then uses a `for` loop to iterate from 0 to 8 (since `i` starts at 0 and increments by 2 in each iteration). Inside the loop, it increments the `ten` variable by 1 for each iteration. Finally, it returns the value of `ten`, which should be 5 after the loop has executed.

So, the code counts from 0 to 10 by increments of 2 and returns the count, which should be 5.

There is nothing syntactically or logically wrong with the code you've provided.

Comments:
while technically correct with the given context, ChatGPT doesn't know exactly what the problem is asking, and therefore the "ten" variable is supposed to be 10

## 2. 
Write a method called `middleChar` that will get a `String` passed in as a parameter, get the number of characters in the `String`, and return the middle character of the `String`. If the `String` has an even number of letters, it should return the first of the two middle characters (i.e. for the word fluffy, the method will return ‘u’.

```java
public char middleChar(String s) {
    int length = s.length();
    int middle = length / 2;
    return s.substring(0, middle);
}
```
first impressions:
It begins okay, but the programmer forgot that they were just outputting a character, not a string to the character. This wont compile as the substring method returns a string. A more appropriate method would be s.charAt(middle).

ChatGPT says: 