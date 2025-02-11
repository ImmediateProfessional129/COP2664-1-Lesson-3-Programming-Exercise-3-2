# COP2664-1-Lesson-3-Programming-Exercise-3-2
This is a repository link of the COP2664-1 Lesson 3 Programming Exercise 3-2

// This program is designed to calculate the price of a movie ticket depending on the moviegoer's age and the premiere time whether day or night.

import Foundation // This is a built-in library that allows the program to use the functions of the Foundation framework.
print("Enter 'day' or 'night': ") // This line of code asks the user to enter the premiere time of the movie.
var time = readLine() // This line of code reads the user's input and stores it in the variable 'time'.
print("Enter your age: ") // This line of code asks the user to enter their age.
var age = Int(readLine()!)! // This line of code reads the user's input and stores it in the variable 'age'.
switch (time, age) { // This line of code starts a switch statement that checks the value of the variables 'time' and 'age'.
  case ("day", _): // This line of code checks if the value of 'time' is 'day' and the value of 'age' is less than or equal to 13.
    print("Your ticket price is $8") // This line of code prints the message 'Your ticket price is $8'.
  case ("night", _): // This line of code checks if the value of 'time' is 'night' and the value of 'age' is less than or equal to 13.
    print("Your ticket price is $12") // This line of code prints the message 'Your ticket price is $12'.
  case ("night", 4...16): // This line of code checks if the value of 'time' is 'night' and the value of 'age' is between 4 and 16.
    print("Your ticket price is $15") // This line of code prints the message 'Your ticket price is $15'.
  case ("night", 17...54): // This line of code checks if the value of 'time' is 'night' and the value of 'age' is between 17 and 54.
    print("Your ticket price is $13") // This line of code prints the message 'Your ticket price is $13'.
  case ("night", _): // This line of code checks if the value of 'time' is 'night' and the value of 'age' is greater than 54.
    print("Your ticket price is $12") // This line of code prints the message 'Your ticket price is $12'.
  default: // This line of code is executed if none of the previous cases are true.
    print("Your ticket price is free") // This line of code prints the message 'Your ticket price is free'.
}
