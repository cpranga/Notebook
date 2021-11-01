# Major DIfferences
* No main method; first line of code is first executed
* Return type is to right of function declaration

# Variable Declarations

Type|Declaration
--|--
Const|`let var: Double = 3.0`
Mutable|`var: Double = 3.0`

Can also infer types based on value
`let var = 3.0` will infer the type to be a Double

# Optionals
Need to specify if a Variable can be Nil
`let var: String?` specifies that var may be a String or Nil

## Forced Unwrapping
to access an optional, you need a special keyword `!`
`print(var!)` will unwrap var and access the value
**will** crash if unwraps to Nil

## Optional Binding
basically checking that the variable is not Nil
```
if let count = var? {
print(count)
}
```
if var is Nil, this block will be skipped over

## Coalescing Operator `??`
`let var = count ?? 0`
if count is not Nil, sets var to count; if count is Nil, set var to 0

## Chaining Operator
`let var: String? = count?`
if count is not Nil, set var to count; if count is Nil, set var to Nil

# Loops

## For Loops
### Iterating over Objects
Type|Syntax
--|--
List or Set|`for item in listOrSet`
Dictionary|`for key, value in dictObj`

### Iterating over Ranges
Type|Syntax|Result
--|--|--
Closed Range|`for i in 0..10`|0 - 10
Half-open Range|`for i in 0..<10`| 0 - 9

## While Loop

To print out 1 - 10 (inc)
```
index = 1
while index <= 10{
	print(index)
	index++
}
```

## Repeat-While (Do-While)
Print 1-10 inc
```
index = 1
repeat{
print(index)
index++
} while index <= 10
```

# Conditionals
## Basic If Statements
```
if price == 10 {}
else if price == 20 {}
else {}
```
## Ternary Operators
Basically a short-hand for if/else statements
`let isTall = height > 200 ? true : false`

## Guard
Guard can be used to transfer program control OOS if conditions aren't met
```
guard expression else {
  // statements
  // control statement: return, break, continue or throw.
}
```
So if we only want to do logic on even numbers within range 1 - 100:
```
for index in 1..100{
	guard n%2 == 0{
		continue
	}
}
```

## Switch
Major differences
* Only single will be executed
* Can also use ranges within checks

```
switch year{
	case 2003, 2004: // if year is 2003 or 2004
	case 2005...2009: // if year is in range of 2005 to 2009
	default: // if no cases are True
}
```

# Functions

Specific Feature|Syntax
--|--
Void|`func() funcName() {}`
Parameters|`func funcName(varName:varType){}`
Default Parameters|`func funcName(varName:varType = defaultValue){}`
Return Value|`func funcName() -> Int{}`

