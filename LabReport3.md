## Part 1 - Bugs (Using Code From Lab4)

1)

Base Code:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {
      newArray[i] = newArray[arr.length - i - 1];
    }
    return newArray;
}
```

Failure-Inducing Test:
```
@Test
public void testReversed2() {
    int[] input4 = {1,2,3,4};
    assertArrayEquals(new int[]{4,3,2,1}, ArrayExamples.reversed(input4));
}
```

2)

Base Code:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {
      newArray[i] = newArray[arr.length - i - 1];
    }
    return newArray;
}
```
Non-Failing Test:
```
 @Test
  public void testReversed() {
    int[] input3 = {};
    assertArrayEquals(new int[]{}, ArrayExamples.reversed(input3));
 }
```

3)

Passing:

![Image](LabR3-1.png)

Failing:

![Image](LabR3-2.png)

4)

Base Code:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {
      newArray[i] = newArray[arr.length - i - 1];
    }
    return newArray;
}
```
Modified Code:
```diff
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {
-      newArray[i] = newArray[arr.length - i - 1];
+      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
}
```

5)

It was a simple fix of changing `newArray` to `arr` to correct the issue. With `newArray`, it was assigning the values to itself when it was supposed to assign them to `arr`.

## Part 2 - Researching Commands

1)

2)

3)

4)

5)

6)

7)

8)

