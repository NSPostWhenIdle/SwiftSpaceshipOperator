Spaceship Operator for Swift
============================

The spaceship operator (more info in link) is an operator from Ruby and several other languages that looks like... well... a spaceship! ( <=> ).

It returns 1 if the left operand is greater of the two, -1 if the left operand is less, and 0 if the two numbers have the same value.

http://en.wikipedia.org/wiki/Spaceship_operator

## Usage

```swift
let less: Int = 6.0 <=> 17.0
let greater: Int = 4.0 <=> 2.0
let equal: Int = 9001.0 <=> 9001.0

println(less) // Outputs -1
println(greater) // Outputs 1
println(equal) // Outputs 0
```

### Implementation

```swift
operator infix <=> { associativity left precedence 140 }

@infix func <=> (left: Double, right: Double) -> Int {

    if left < right {
        return -1
    } else if left > right {
        return 1
    } else {
        return 0
    }
}
```



#####The MIT License (MIT)

Copyright (c) 2014 Michael MacCallum

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.