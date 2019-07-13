# Functions lab 1

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

Complete the function so that it will print out total cost after tax. Make sure to **call the function** afterwards.

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax(itemCost: Double) -> Double {
let nyTax = 0.08775
let tax = itemCost * nyTax
print(itemCost + tax)
return(itemCost + tax)
}
totalWithTax(itemCost: 45)

```
Then, modify the function you implemented to have a return type of `Int`, and use an external name that looks more readable. Function calls should look something like "total cost of the item after tax"

```
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax(itemCost: Double) -> Int {
let nyTax = 0.08775
let tax = itemCost * nyTax
let answer = Int(itemCost) + Int(tax)
print("Total cost of the item after tax is: $\(answer)")
return answer
}
totalWithTax(itemCost: 45)

```
## Question 2

Convert the the following if/else statement below into function with a `String` return type.

```swift
let todaysTemperature = 72

if todaysTemperature <= 40 {
    print("It's cold out.")
} else if todaysTemperature >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}
```
```
func weatherDescription(todaysTemperature: Int) -> String {
var answer = ""
if todaysTemperature <= 40 {
answer = "It's cold out."
} else if todaysTemperature >= 85 {
answer = "It's really warm."
} else {
answer = "Weather is moderate."
}
print(answer)
return answer
}


weatherDescription(todaysTemperature: 72)
```


## Question 3

Write a function named `min2` that takes two `Int` values, `a` and `b`, and returns the smallest one.

Function Definition
`func min2(a: Int, b: Int) -> Int`

Example:
Input: `min2(a:1, b:2)`

Output: `1`

```
func min2(a: Int, b: Int) -> Int {
var min = 0
if a > b {
min = b
} else {
min = a
}; return min
}

min2(a: 1, b: 2)

```

## Question 4

Write a function that takes an `Int` and returns its last digit. Name the function `lastDigit`. Use _ to ignore the external parameter name.

Function Definition:
`func lastDigit(_ number: Int) -> Int`

Example:
Input: `lastDigit(12345)`

Output: `5`

```
func lastDigit(_ number: Int) -> Int {
let x = number
return x % 10
}

lastDigit(12345)
```

## Question 5

Write a function that takes in any two positive integers and return the sum.
```
func sumOfTwoPositiveIntegers(number1: Int, number2: Int) -> Int {
return (number1 + number2)
}

sumOfTwoPositiveIntegers(number1: 2, number2: 8)
```



## Question 6

Write a function takes in any number grade and returns a corresponding letter grade.

| Number Grade | Equivalent Letter Grade |
| :--------: | :---------: |
| 100 | A+ |
| 90 - 99 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 65 - 69 | D |
| Below 65 | F |
```
func letterGrade(NumberGrade: Int) -> String {
var grade = ""
let num = NumberGrade
if num == 100 {
grade = "A+"
}
for n in 90...99 {
if num == n {
grade = "A"
}
}
for n in 80...89 {
if num == n {
grade = "B"
}
}
for n in 70...79 {
if num == n {
grade = "C"
}
}
for n in 65...69 {
if num == n {
grade = "D"
}
}
if num < 65 {
grade = "F"
}
print(grade)
return grade
}
letterGrade(NumberGrade: 6)
```

## Question 7

Make a calculator function that takes in three parameters (two numbers and one operator) and returns the answer of the operation.

Operator parameter: (+, -, x, /)
```
func calculator(number1: Int, number2: Int, Operator: Character) -> Int {
var answer = 0
if Operator == "+" {
answer = (number1 + number2)
}
if Operator == "-" {
answer = (number1 - number2)
}
if Operator == "x" {
answer = (number1 * number2)
}
if Operator == "/" {
answer = (number1/number2)
}
print(answer)
return answer
}

calculator(number1: 6, number2: 3, Operator: "/")
calculator(number1: 20, number2: 4, Operator: "x")
calculator(number1: 500, number2: 2, Operator: "-")
```
## Question 8

Write a function so that it will print out **total cost after tip.**

```swift
let mealCost = 45
let tipPercentage = 0.15

let myFinalCost = totalWithTip() //Fill in the arguments
```
```
func totalWithTip(mealCost: Int, tipPercentage: Double) -> Double {
let tipAmount = Double(mealCost) * tipPercentage
print(Double(mealCost) + tipAmount)
return (Double(mealCost) + tipAmount)
}
let myFinalCost = totalWithTip(mealCost: 45, tipPercentage: 0.15)
```
Write a function that will print out **total cost after tip and tax.**

```
func totalWithTip(mealCost: Int, tipPercentage: Double, taxPercentage: Double) -> Double {
let tipAmount = Double(mealCost) * tipPercentage
let taxAmount = Double(mealCost) * taxPercentage
print(Double(mealCost) + tipAmount + taxAmount)
return (Double(mealCost) + tipAmount + taxAmount)
}
let myFinalCost = totalWithTip(mealCost: 45, tipPercentage: 0.15, taxPercentage: 0.09)

```


## Question 9

Implement a function named `repeatPrint` that takes a string `message` and a integer `count` as parameters. The function should print `message` `count` number of times and then print a newline.

Example:
Input: `repeatPrint(message: "+", count: 10)`

Output: `++++++++++`

```
func repeatPrint(message: String, count: Int) -> String {
var answer = ""
for _ in 1...count {
answer.append(message)
}
print(answer)
return answer
}
repeatPrint(message: "hi", count: 10)
```


## Question 10

Write a function named `first` that takes an Int named n and returns an array with the first n numbers starting from 1.

Function Definition
`func first(_ n: Int) -> [Int]`

Example:
Input: `first(3)`

Output: `[1, 2, 3]`

```
func first(_ n: Int) -> [Int] {
var array: [Int] = []
for numbers in 1...n {
array.append(numbers)
}
print(array)
return array
}
first(3)
```

## Question 11

Write a function that prints the numbers from 1 to x, except:

If the number if a multiple of 3, print `"Fizz"` instead of the number
If the number is a multiple of 5, print `"Buzz"` instead of the number
If the number is a multiple of 3 AND 5, print `"FizzBuzz"` instead of the number
Your function should take in one parameter: x (the number to count up to)
```
func numberStuff(_ n: Int) -> [String] {
var array: [String] = []
for numbers in 1...n {
array.append(String(numbers))
}
for (index, stuff) in array.enumerated() {
if Int(stuff)! % 3 == 0 {
array[index] = "Fizz"
}
if Int(stuff)! % 5 == 0 {
array[index] = "Buzz"
}
if Int(stuff)! % 5 == 0 && Int(stuff)! % 3 == 0 {
array[index] = "FizzBuzz"
}
}
print(array)
return(array)
}
numberStuff(30)
```


## Question 12

Write a function named `reverse` that takes an array of integers named `numbers` as a parameter. The function should return an array with the numbers from `numbers` in reverse order.


Example:
Input: `reverse([1, 2, 3])`

Output: `[3, 2, 1]`

```
func reverse(numbers: [Int]) -> [Int] {
var answer: [Int] = []
answer = numbers.reversed()
print(answer)
return answer
}
reverse(numbers: [1, 2, 3, 7, 9])
```

## Question 13

Write a function that prints out the most frequently appearing Int in an array of Int.


## Question 14

Write a function that sums all the even indices of an array of Ints.

```
func evenIndexSum(array:[Int]) -> Int {
var evenNumbers: [Int] = []
for (index, element) in array.enumerated() {
if index % 2 == 0 {
evenNumbers.append(element)
}
}
print(evenNumbers.reduce(0,+))
return (evenNumbers.reduce(0,+))
}

evenIndexSum(array: [1,2,3,4,5,6,7,8,9,10])
```

## Question 15

Write a function that flips a dictionary.  All of the keys are now values and all of the values are now keys.

Example:
Input: `[1: "hi", 5: "bye:]`

Output: `["hi": 1, "bye": 5]`

```
func reverseDict(dict:[Int: String]) -> [String: Int] {
var newDict: [String: Int] = [:]
for (key, value) in dict {
newDict[value] = key

}
print(newDict)
return newDict
}

reverseDict(dict: [1: "hi", 5: "bye", 6: "die"])
```
## Question 16

Write a function that finds the person with the second highest test score in a Dictionary that maps names to scores.

Example:
Input: `["Person 1": 83, "Person 2": 74, "Person 3": 82]`

Output: `"Person 3"`

```
func secondHighest(input: [String:Int]) -> String {
var scores = Array(input.values.sorted().dropLast())
var name = ""
let secondLast = scores.popLast()
for (key, value) in input {
if value == secondLast {
name = key
}}
print(name)
return name
}

secondHighest(input: ["Person 1": 83, "Person 2": 74, "Person 3": 82, "Person 4": 90, "Person 5": 85])
```
## Question 17

Write a function that determines if a value is inside of array.
```
func isThereStuffInIt(array:[Any]) -> Bool {
if array.isEmpty {
return true
} else {
return false}
}
```

## Question 18

Write a function takes an `Int` as input, and returns true if it is even, or false if it is odd.
Using your new function, write code that prints out whether `dieRoll` is even or odd:

`let dieRoll = Int(arc4random_uniform(6) + 1)`

```
func evenOrOdd(n: Int) -> Bool {
if n % 2 == 0 {
return true
} else {
return false
}
}
let dieRoll = Int(arc4random_uniform(6) + 1)
print(evenOrOdd(n: dieRoll))
```


## Question 19

Write a function that takes `[Int]` as input. It should return the largest Int in the array.

Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

`let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]`

If you haven't already done so, write a function that takes in an Int and returns whether that number is even or odd. Use that function to print a sentence that states whether the largest Int in `myArray` is even or odd.
```
func evenOrOdd(n: Int) -> Bool {
if n % 2 == 0 {
return true
} else {
return false
}
}

func largestInt(array: [Int]) -> Int {
var arr = array.sorted()
return arr.popLast()!
}

let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]

print("The largest integer in \(myArray) is \(largestInt(array: myArray)) and it is \(evenOrOdd(n: largestInt(array: myArray))) that this number is even.")
```


## Question 20

Write a function that takes a String as input and returns the number of characters in the string

Using your function, print how many characters are in myString:

`let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."`

```
func numberofChars(input: String) -> Int {
return input.count
}
print(numberofChars(input: myString)) // 163
```

## Question 21

Write a function that counts how many characters in a String match a specific character.  (e.g: count how many "a"s are in a String, or count how many ","s are in a String.

Example:
Input:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"
```

Sample output: `3`

```
func howManyChars(string: String, character: Character) -> Int {
let targetChar = character
var groupedChars: [String] = []
for stuff in string {
if stuff == targetChar {
groupedChars.append(String(stuff))
}
}
return groupedChars.count
}

print(howManyChars(string: "this is a test string for your code", character: "i"))
```
## Question 22

Write a function that counts how many characters in a String match one of several possible characters.  (e.g: count how many vowels are in a String, or count how many "a"s "b"s and "c"s are in a Sting)

Example:
Input:
```swift
let inputString = "This one is a little more complicated"
let targetCharacters: [Character] = ["a","e","i","o","u"]
```
Output: `13`
```
func howManyChars(string: String, character: [Character]) -> Int {
let targetChar = character
var groupedChars: [String] = []
for stuff in string {
for moreStuff in targetChar {
if moreStuff == stuff {
groupedChars.append(String(stuff))
}
}
}
return groupedChars.count
}

print(howManyChars(string: "This one is a little more complicated", character: ["a","e","i","o","u"]))
```


## Question 23

Write a function that returns the number of unique Ints in an array of Ints.

Example:
Input: `let inputArray2 = [3,1,4,1,3,2,6,1,9]`

Output: `4`

//Explanation: 2, 4, 6, 9 are unique in the array. Every other number is not unique.

Not sure how to put into syntax. 

## Question 24

Write a function that converts a binary number into decimal. The binary number will be given as an array of Ints.

Example:
Input: `let binaryArray = [1,0,1,1,1,0,1]`

Output: `93`

## Question 25

Write a function named `timeDifference`. It takes as input four numbers that represent two times in a day and returns the difference in minutes between them. The first two parameters `firstHour` and `firstMinute` represent the hour and minute of the first time. The last two `secondHour` and `secondMinute` represent the hour and minute of the second time. All parameters should have external parameter names with the same name as the local ones.

Example:
Input: `timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)`

Output: `67`


## Question 26

Write a function called `filterOdd` that takes an array of ints and returns it with just the even numbers.

Example:
Input:  `filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])`

Output: `[2, 4, 6, 8]`

```
func filterOdd(arr: [Int]) -> [Int] {
var newArray: [Int] = []
for num in arr {
if num % 2 == 0 {
newArray.append(num)
}
}
return newArray
}

filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])
```

## Question 27

Write a function called `doubleIt` that takes an array of ints and returns it with all the elements doubled.

Example:
Input: `doubleIt(arr: [1, 2, 3, 4])`

Output: `[2, 4, 6, 8]`

```
func doubleIt(arr: [Int]) -> [Int] {
var newArray: [Int] = []
for num in arr {
newArray.append(num * 2)
}
return newArray
}


print(doubleIt(arr: [1, 2, 3, 4]))
```


Then write a function called `multiplyBy` that takes an array of ints and an int n that will return the array with all the elements multiplied by n.

Example:
Input:  `multiplyIt(arr: [1, 2, 3, 4], n: 4)`

Output:  `[4, 8, 12, 16]`

```
func multiplyBy (arr: [Int], n: Int) -> [Int] {
var newArray: [Int] = []
for num in arr {
newArray.append(num * n)
}
return newArray
}


print(multiplyBy(arr: [1, 2, 3, 4], n: 4))
```

## Question 28

Write a function called `unwrap` that takes an array of optional ints and returns an array with them unwrapped with any nil values removed.

Example:
Input:  `unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])`

Output: `[7, 4, 43, 11, 2]`

```
func unwrap(array:[Int?]?) -> [Int] {
var newArray: [Int] = []
if let array = array {
for number in array {
if number != nil {
newArray.append(number!)
}
}
}
return newArray
}

print(unwrap(array: [nil, 7, 4, nil, 43, 11, nil, 2]))
```

## Question 29

Write a function that takes an array of bools and returns a dictionary that maps the bools to how many times they appear in the array.

Example:
Input:  `countBools(arr: [true, true, false, true, false, true])`

Output: `[false: 2, true: 4]`


## Question 30

Write a function that takes a string as input and returns a dictionary that maps each unique character to how many times they appear in the string.

Example:
Input:  `countCharacters(str: "Hello, World!")`

Output: `["H": 1, "r": 1, "!": 1, "e": 1, "o": 2, "l": 3, ",": 1, " ": 1, "W": 1, "d": 1]`


## Question 31

Write a function that takes this dictionary of baseball teams by ID and returns an array of tuples that contain each team's ID and name.

`let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]`

Example:
Input:  `dictToTuples(dict: baseballTeamsById)`

Output: `[(.0 1003, .1 "Rays"), (.0 1001, .1 "Mets"), (.0 1004, .1 "Marlins"), (.0 1002, .1 "Yankees")]`


## Question 32

Write a function that checks if a String is a [Palindrome](https://en.wikipedia.org/wiki/Palindrome)
```
func palindromeCheck(Input: String) -> Bool {
var answer = Bool()
let stringInput = Input.replacingOccurrences(of: " ", with: "")
if stringInput == String(stringInput.reversed()) {
answer = true
} else {
answer = false
}
return answer
}

palindromeCheck(Input: "go hang a salami im a lasagna hog") // true

```

## Question 33

Write a function that checks if a String is a [pangram](https://en.wikipedia.org/wiki/Pangram)
```
func pangramCheck(input: String) -> Bool {
var answer = Bool()
let alphabet = "abcdefghijklmnopqrstuvwxyz"
let alphabetSet = Set(alphabet)
let inputSet = Set(input)
let intersect = alphabetSet.intersection(inputSet)

if intersect.count == alphabet.count {
answer = true
} else {
answer = false
}
return answer
}
print(pangramCheck(input: "The quick brown fox jumps over the lazy dog"))
```

## Question 34

Write your own `min()` and `max()` functions for an Array of Ints

max
```
func maxNumber(Array: [Int]) -> Int {
var arraySorted = Array.sorted()
return arraySorted.popLast()!
}

print(maxNumber(Array: [2, 3, 6, 4, 2, 9, 25, 512, 10024, 3, 420])) // 10024
```
min
```
func minNumber(Array: [Int]) -> Int {
var arraySorted = Array.sorted()
return arraySorted[0]
}

print(minNumber(Array: [2, 3, 6, 4, 2, 9, 25, 512, 10024, 3, 420]))
```

## Question 35

Given two arrays of Ints, write a function that tells you all the values they have in common.

```
func valuesInCommon(array1: [Int], array2: [Int]) -> [Int] {
return Array(Set(array1).intersection(Set(array2))).sorted()
}

print(valuesInCommon(array1: [1,2,4,5,9,10,19], array2: [2,4,8,10,12,15,17,19]))
```
## Question 36

Find the most-frequently appearing Array of Ints in an Array of Arrays of Ints.


## Question 37

Given a String as input, rotate all a-z characters by one.  This is called [ROT-1 encryption](http://www.rot-n.com/).

Sample input:
`This is a test string. Anything can be written in here (even Zebras and zebras).`

Sample output:
`Uijt jt b uftu tusjoh. Bozuijoh dbo cf xsjuufo jo ifsf (fwfo Afcsbt boe afcsbt).`
