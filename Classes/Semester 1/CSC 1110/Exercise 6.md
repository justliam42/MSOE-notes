Course:  CSC 1110
Fall 2023
Exercise 6 - Using Chat-GPT To Debug Code
Name: Liam Otten
Date: 10/6/2023

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

ChatGPT says: The provided Java method `middleChar` aims to return the middle character of a given string `s`. However, there is an issue with the code. The `substring` method is used to extract a portion of the string, but it returns a string, not a single character. To get a single character, you should use the `charAt` method.

Here's the corrected version of the `middleChar` method:

```java
public char middleChar(String s) {
	int length = s.length();     
	int middle = length / 2;     
	return s.charAt(middle);
}
```


In this corrected code, we use the `charAt` method to get the character at the middle index of the string, which is what you want when you're trying to find the middle character.

Comments:
This seems to be spot on.


## 3. 
Write the equals method for the `String` class. Below is a buggy implementation.
```java
@Override
public boolean equals(String s) {
    if(this == s) { return true; }
    if(!(s instanceof String)) { return false; }
    for(int i = 0; i < s.length(); ++i) {
        if(this.charAt(i) != s.charAt(i)) { return false; }
    }
    return true;
```
First Impressions:
I can say I know a whole lot about Overrides and such, but from what I know it seems good to me.


ChatGPT says: 
The Java code attempts to override the `equals` method for a class. However, there are a few issues:

1. **Method Signature**: The `equals` method in Java should have the following signature to override the method from the `Object` class:

```java
@Override public boolean equals(Object obj) {     // ... }
```


2. **Parameter Type**: The `equals` method should take an `Object` as a parameter, not a `String`. This allows for proper polymorphic behavior and adheres to the standard `equals` method.
    
3. **Comparison with `this`**: The line `if(this == s)` should not be comparing `this` (which is the current instance) with `s` (which is of type `String`). Instead, it should be comparing with the other object passed as an argument.
    
4. **Instanceof Check**: The `instanceof` check should be performed on the argument `obj` (of type `Object`) to determine if it's an instance of the class.
    

Here's the corrected code:



```java
@Override public boolean equals(Object obj) {     
	if (this == obj) {         
		return true;     
	}     
	if (!(obj instanceof String)) {         
		return false;     
	}          
	String otherString = (String) obj;          
	if (this.length() != otherString.length()) {         
		return false;     
	}          
	for (int i = 0; i < this.length(); i++) {         
		if (this.charAt(i) != otherString.charAt(i)) {
			return false;         
		}     
	}          
	return true; 
}
```


In this corrected code:

- We use `Object` as the parameter type for the `equals` method to adhere to the method signature for overriding.
- We perform the `instanceof` check on the `obj` (which is of type `Object`).
- We cast `obj` to `String` before performing any operations specific to the `String` class.
- We properly compare the characters of the two strings using the `charAt` method.

Comments: 
Once again it didn't understand the scope of the problem, which only asked to write the code for the string class, as opposed to rewriting the default Object.equals

ChatGPT once again after some back and forth:
  
I understand your desire to override the `equals` method for the `String` class, but it's important to clarify that in Java, you cannot directly override methods in classes from the `java.lang` package, including the `String` class. The `equals` method of the `String` class is final and cannot be modified or overridden in your code.

If you have a specific use case that requires custom behavior for comparing or working with `String` objects, you'll need to create your own custom class and implement your own `equals` method within that class to define the desired behavior for comparisons involving instances of your custom class and `String` objects.

