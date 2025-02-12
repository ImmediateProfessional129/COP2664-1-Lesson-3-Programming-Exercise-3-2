# COP2664-1-Lesson-3-Programming-Exercise-3-2
This is a repository link of the COP2664-1 Lesson 3 Programming Exercise 3.2

// This program is designed to determine the ticket price for a movie based on the age the moviegoer puts down and the time of day.

let timeOfDay = "night" // or "day"

let age = 15 // or "50"

var ticketPrice: Double = 0.0
switch timeOfDay.lowercased(){
  // day time price is $8 for everyone age 4 or higher
case "day":
    if age >= 4{
        ticketPrice = 8.00 
    } else {
        ticketPrice = 0.0 // free for anyone under age 4
    }
case "night":
   // nighttime price based on age ranges
   switch age{
   case 4...16:
      ticketPrice = 12.0
   case 17...54:
      ticketPrice = 15.0
   case _ where age >= 55:
      ticketPrice = 13.0
   default:
      ticketPrice = 0.0 // free for anyone under age 4
}
default:
   print("Invalid time of day entered.")
   ticketPrice = -1.0 // invalid time input
}
if ticketPrice != -1.0 { // valid time input
   print("The ticket price for a \(age)-year-old person watching the movie in the \(timeOfDay) is $\(ticketPrice).") // print the ticket price
}
