---
title: "Several progarmming language comparison"
date: 2020-05-12 00:00:00 -0800
category: language
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
num = int(1.1)
```

java
```java
double n = 1.1
int num = (int) n;
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

## Ascii
python
```python
ord('A')    # 65
```

java
```java
(int) 'A'
```

## String
python
```python
"strings"[1]    # "t"
str(123)
int("123")
int("12", 3)    # 5, base=3
pos = str.find(substring, fromIndex, toIndex)
```

java
```java
char ch = "strings".charAt(1);          // 't'
String str = String.valueOf(123);       // "123"
Integer i = Integer.valueOf("123");     // 123
Integer i = Integer.valueOf("12", 3);   // 5, base=3
int pos = str.indexOf(substring, fromIndex);
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
String str = String.join("", list);
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
list = [0, 1]
set = set()
set = {0, 1}
dict = {}
dict = defaultdict(list)

list.append(value)
list.insert(index, value)
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
List<Integer>[] list2 = new ArrayList[n];  // array of list
List<int[]> list3 = new ArrayList<>();       // list of array
int[] nums = new int[] {0, 1};
Set<Integer> set = new HashSet<>();
Map<Integer, Integer> map = new HashMap<>();

String[] array = {"a", "b", "c", "d", "e"};
List<String> list = Arrays.asList(array);
int[][] array = list.toArray(new int[length][2]);

list.add(value);
list.add(index, value);     // insert
list.set(index, value);
list2[i].add(value);
set.add(key);
set.contains(key);
map.containsKey(key);
map.put(key, value);
map.putIfAbsent(key, value);

treeSet.higher(key);
treeSet.lower(key);
treeSet.ceiling(key);
treeSet.floor(key);

treeMap.higherKey(key);
treeMap.lowerKey(key);
treeMap.ceilingKey(key);
treeMap.floorKey(key);  // Returns the greatest key less than or equal to the given key,
```

kotlin
```kotlin
val people = listOf<Person>(Person("name", age), bob)
val nums = listOf(1, 2, 3)
setOf(1, 2, 3)
mapOf("key1" to 1, "key2" to 2)
```

scala
```scala
List(1, 2, 3)
```

## Slice
java
```java
Arrays.copyOfRange(array, 0, 3);  // 3 exclusive
```

python
```python
list[0:3]
```


## Length

python
```python
length = len([0, 1])
length = len("str")
```

java
```java
int[] array = {0, 1, 2};
length = array.length;

List<Integer> list = new ArrayList<>();
length = list.size();

length = "str".length();
```

## Sorts

python
```python
nums.sort(key = lambda n:(n[0], -n[1]), reverse = True)
```

java
```java
nums.sort((a1, a2) -> (a1 - a2));
Arrays.sort(nums, Collections.reverseOrder());
Arrays.sort(nums, (a1, a2) -> Math.abs(a1) - Math.abs(a2));
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
mini = min(mini, val1, val2)
```

java
```java
int mini = Math.min(mini, val1)
mini = Math.min(mini, val2)
```

## Priority queue

python
```python
from heapq import *

min_heap, max_heap = [], []
heappush(min_heap, num)   # min heap
heappush(max_heap, -num)   # max heap
pop = heappop(heap)
peek = heap[0]
```

java
```java
PriorityQueue<Integer> pq = new PriorityQueue<>();
pq.add(value);
Integer v = pq.poll();
Integer v = pq.peek();

PriorityQueue<Person> pq = new PriorityQueue<>();
class Person implements Comparable<Person> {
    private int salary;
    @override
    public int compareTo(Person p) {
        return this.salary - p.salary;
    }
}

PriorityQueue<String> pq = new PriorityQueue<>(10, (p1, p2) -> (p1.length() - p2.length());
PriorityQueue<String> pq = new PriorityQueue<>(10, new Comparator<String>() {
    @override
    public int compare(String p1, String p2) {
        return p1.length() - p2.length();
    }
});
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

## Math

python
```python
abs(-2)
min(1, 2)
max(list)
int(3.7)         # 3
round(3.7)       # 4
round(3.777, 2)  # 3.78
float('int')
-float('int')
```

java
```java
Math.abs(-2);
Math.min(1, 2);
Math.max(1, 2);
int max = IntStream.range(0, array.length).map(i -> array[i]).max().getAsInt();
Math.floor(3.7);  // 3
Math.round(3.7);  // 4
Math.ceil(3.2);   // 4
Integer.MAX_VALUE
Integer.MIN_VALUE
```

## Enum

java
```java
enum CardType {
    SILVER("gray"),
    GOLD("yellow"),
    PLATINUM("black")

    CardType(String value) {
        this.value = value;
    }
}
```

kotlin
```kotlin
enum class CardType(val color: String) {
    SILVER("gray"),
    GOLD("yellow"),
    PLATINUM("black")
}
```
