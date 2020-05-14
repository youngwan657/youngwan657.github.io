---
title: "Several progarmming language comparison"
date: 2020-05-12 00:00:00 -0800
categories: language
---
## Package and imports

python
```python
import random
from random import *
```

java
```java
package com.demo;

import java.util.List;
```

kotlin
```kotlin
package com.demo

import org.mockito.*
```

scala
```scala
package com.demo

import org.apache.spark.sql._
```

## Classes

python
```python
class Car:
    wheel = 4
    def __init__(self, brand, color):
        self.brand = brand
        self._color = color     # just private naming convention
c = Car("Ferrari", "red")
```

java
```java
public class Car {
    private static int wheel = 4;
    private String brand;
    public Car(String brand) {
        this.brand = brand;
    }
    public static int getWheels() {
        return wheels;
    }
}
c = new Car("Ferrari")
```

kotlin
```kotlin
open class Car(var brand: String) {}
val c = Car("Ferrari")
```

scala
```scala
class Car(var brand: String)
val c = new Car("Ferrari")
```

## Functions

python
```python
def sum(a, b):
    return a + b
```

java
```java
int sum(int a, int b) {
    return a + b;
}
```

kotlin
```kotlin
fun sum(a: Int, b: Int): Int {
    return a + b
}
```

scala
```scala
def sum(a: Int, b: Int): Int {
    return a + b
}
```

## Variables

python
```python
num = 1
```

java
```java
int num = 1;
final int num = 1;
```

kotlin
```kotlin
val num: Int = 1
var num: Int = 1
```

scala
```scala
val num: Int = 1
var num: Int = 1
```

## String templates

python
```python
"Number %d" % num
"String %s, number %d" % (str, num)
```

java
```java
String.format("String %s, number %d", str, num);
```

kotlin
```kotlin
"string is $str"
"string is ${obj.get()}"
```

scala
```scala
s"string is $str"
s"string is ${obj.get()}"
```

## Join and split

python
```python
str = ''.join(list)
list = str.split()
```

java
```java
String.join("", list);
String[] strs = str.split(" ");
```


## Conditional expressions

python
```python
if a < b < c and not flag:
    d += 1
```

java
```java
if (a < b && b < c) {
    d++;
}
```

kotlin
```kotlin
if (a < b) {
    return a
}
```

scala
```scala
if (a < b) {
}
```

## For loop

python
```python
for num in nums:
    pass

for num in range(11):
    pass

for ch in str:
    pass

for k, v in dict:
    pass
```

java
```java
for (int num : nums);
for (int i = 0; i < 11; i++);
for (char ch : str.toCharArray());
```

kotlin
```kotlin
for (num in nums) {
    println(num)
}
```

scala
```scala
for (i <- 1 to 10) {
    print(i)
}
```

## While loop

python
```python
while True:
    # infinity loop
    pass
```

java
```java
while (true);
```

kotlin
```kotlin
while (true) {
}
```

scala
```scala
while (true) {
}
```

## Collections

python
```python
list = []
set = set()
dict = {}

list.pop(index)
list.remove(value)

key in set
key in dict

set1 | set2     # union
set1 & set2     # intersection
set1 - set2     # difference
set1 ^ set2     # complementary
```

java
```java
List<Integer> list = new ArrayList<>();
Set<Integer> set = new HashSet<>();
Map<Integer, Integer> map = new HashMap<>();

set.contains(key)
map.containsKey(key)
```

kotlin
```kotlin
listOf(1, 2, 3)
setOf(1, 2, 3)
mapOf("key1" to 1, "key2" to 2)
```

scala
```scala
List(1, 2, 3)
```

## Sorts

python
```python
nums.sort(key = lambda n:(n[0], -n[1]), reverse = True)
```

java
```java
nums.sort((a1, a2) -> (a1 - a2))
Arrays.sort(nums, (a1, a2) -> Math.abs(a1) - Math.abs(a2))
```

## Initialize list

python
```python
maze = [[0] * len(input[0]) for i in range(len(input))]
```

java
```java
Arrays.fill(nums, -1)
```

## Keep minimum

python
```python
mini = float('inf')
mini = min(mini, cur)
```

java
```java
mini = Integer.MAX_VALUE
int mini = Math.min(mini, cur)
```

## Priority queue

python
```python
from heapq import *

min_heap, max_heap = [], []
heappush(min_heap, num)   # min heap
heappush(max_heap, -num)   # max heap
top = heappop(heap)
peek = heap[0]
```

java
```java
PriorityQueue<Integer> heap = new PriorityQueue<>();
heap.add(num)
top = heap.poll()
peek = heap.peek()
```

## Random

python
```python
from random import *

randint(0, 2)   # 0, 1, 2
```

java
```java
Random rand = new Random();
rand.nextInt(3);    // 0, 1, 2
```

## Deque

python
```python
from collections import deque
deq = deque()
deq.append(1)
deq.appendLeft(2)
right = deq.pop()
left = deq.popLeft()
```

java
```java
import java.util.*;
Deque<Integer> deque = new LinkedList<>();
deque.addFirst(1);
deque.addLast(2);
right = deque.pollFirst();
left = deque.pollLast();
```
