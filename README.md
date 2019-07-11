# Sets lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1√

Ms. Gabriel Williams is a botany professor at District College. One day, she asked her student Mickey to compute the average of all the plants with distinct heights in her greenhouse.

Input: heights of trees below:
`161 182 161 154 176 170 167 171 170 174`

Output:
`169.375`

```swift
var output: Set<Int> = []
output = Set(inputPlant)
var result = output.reduce(0, +)/output.count
print(result)
```

## Question 2√

Determine if a String is a pangram. A pangram is a string that contains every letter of the alphabet at least once.

 e.g `"The quick brown fox jumps over the lazy dog"` is a pangram
 e.g `"The quick brown fox jumped over the lazy dog"` is NOT a pangram

```swift
var one = "The quick brown fox jumps over the lazy dog"
var two = "The quick brown fox jumped over the lazy dog"



var alphabet = "abcdefghijklmnopqrstuvwxyz"
var firstString = Set(one.lowercased())
var secondString = Set(two.lowercased())

// isSuperset check to see if all the characters are in the string the string
if firstString.isSuperset(of: alphabet){
print("it is a pangram")
}else {
print("it is Not a pangram")
}


if secondString.isSuperset(of: alphabet){
print("it is a pangram")
}else {
print("it is Not a pangram")
}

```
## Question 3

The set S originally contains numbers from 1 to n in ascending order. Unfortunately, due to the data error, one of the numbers in the set was duplicated to another number in the set. This results in the repetition of one number and loss of another number in the set.

You are given an array `nums` representing the data status of the set S after the error occurred. Your task is to first find the number occurs twice and then find the number that is missing from the sequence. Return these two values in the form of an array.

 Example 1:
 Input: `nums = [1,2,2,4]`
 Output: `[2,3]`

 Example 2:
 Input: `nums = [1,1]`
 Output: `[1,2]`

 Example 3:
 Input: `nums = [2,2]`
 Output: `[2,1]`
 
 ```swift
 var nums = [1,2,2,4]
 var testNumber = 1
 var result = [Int]()
 for num in nums {
 if num == testNumber {
 testNumber += 1
 } else {
 result.append(num)
 result.append(testNumber)
 break
 
 }
 }
 print(result)
 ```


## Question 4√

Given the 4 arrays of Ints below, create a new array, sorted in ascending order, that contains all the values without duplicates.

```swift
let arr1 = [2, 4, 5, 6, 8, 10, 12]
let arr2 = [1, 2, 3, 4, 5, 6]
let arr3 = [5, 6, 7, 8, 9, 10, 11, 12]
let arr4 = [1, 3, 4, 5, 6, 7, 9]
```
```swift
var fullArray = [arr1,arr2,arr3,arr4]
var newArray = [Int]()

for i in fullArray{
newArray += i
}
print(Set(newArray).sorted())
```
OR
```swift
let arr5 = Set(arr1).union(Set(arr2)).union(Set(arr3)).union(Set(arr4)).sorted()
print (arr5)
```
## Question 5√

Perform the following set operations on the lists below:

1. Find the intersection and print the result
2. Find the symmetric difference and print the result
3. Find the union and print the result
4. What is the outcome of subtracting `list2` from `list1`? Print the result

```swift
//union will return all values combined with no duplicates
print(list1.union(list2))
//intersection is returning the values that are in both arrays
print(list1.intersection(list2))
//SymmetricDifference will return the values that are not in both arrays
print(list1.symmetricDifference(list2))
//Subtracting will remove values that are only unique to the list1
print(list1.subtracting(list2))
//Subtracting will remove values that are only unique to the list2
print(list2.subtracting(list1))

```
```swift
print(list1.union(list2))
print(list1.intersection(list2))
```

## Question 6√

What output will be produced by the code below? Select one answer.

```swift
var spaceships = Set()

spaceships.insert("Serenity")
spaceships.insert("Enterprise")
spaceships.insert("TARDIS")
spaceships.insert("Serenity")

print(spaceships.count)
```

- 3 √
- 4
- Nothing will be output
- 0
- This code will not compile
- 1
- This code will compile but crash


## Question 7√

What output will be produced by the code below?

```swift
var spaceships1 = Set()

spaceships1.insert("Serenity")
spaceships1.insert("Enterprise")
spaceships1.insert("TARDIS")

let spaceships2 = spaceships1

if spaceships1.isSubset(of: spaceships2) {
  print("This is a subset")
} else {
  print("This is not a subset")
}
```

- This code will compile but crash
- "This is not a subset"
- This code will not compile
- "This is a subset" √
- Nothing will be output
