# Part 1
* Here is a screenshot of my code for StringServer:
![Image](stringServer.png)
* And below are two screenshots using /add-message twice:
![Image](localHost1.png)
* In the image above, I am calling /add-message for the first time.
* The handleRequest method is called. When this is called, the String value str at first equals "", and the argument being passed is /add-message?s=hello
* Because /add-message is conatined in the url, "hello" and a line break are added into str, and the message "hello" is printed on the site.
![Image](localHost2.png)
* In the image above, I am calling /add-message for the second time.
* The handleRequest method is called. When this is called, str equals "hello" + "\n", and the argument being passed is /add-message?s=thanks
* Because /add-message is contained in the url, "thanks" and a line break are added into str, and the message "thanks" is printed on the site below the first message.

# Part 2
* Here is code for a method that attempts to reverse the order of items in an array:
```
public class ArrayExamples {
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
}
```
* This is the JUnit test using a failure-inducing input:
```
public class ArrayTests {
  @Test
  public void testReversed1() {
    int[] input2 = { 2, 5 };
    assertArrayEquals(new int[]{ 5, 2 }, ArrayExamples.reversed(input2));
  }
}
```
* This is the JUnit test using an input that doesn't induce a failure:
```
public class ArrayTests {
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
}
```
* When you run these two tests, the following symptom is shows:
![Image](JUnitFails.png)
* Note: this image is the result of running 4 tests, causing 1 of the 2 failures, but for the sake of focusing on one bug, this post is omitting these additional tests.
* So why is one of the tests showing an error and that other one isn't?
* The method creates a new empty array with the same length as the input array, but instead of adding the elements from the input array into the new array in reversed order, the method is putting elements from the empty array into the input array, and then returning the input array. To fix this, the method should return the new array created, and the roles should be reversed: elements from the input array should go into the new array instead. The code below is the same code as earlier but with fixes that was causing the JUnit failure:
```
public class ArrayExamples {
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
}
```
# Part 3
* This is a minor thing, and probably something I probably should've already known, but one thing I learned from lab in week 2 or 3 is that I have to go through only half of an array length during a for loop when I'm trying to return a new array that's the input array in reversed order (which is done in method reverseInPlace). 
* Another thing I learned from lab in week 2 or 3 is how to build and run a server. I know that behind every website is code that wrote it out, but I didn't know about local hosts, and being able to directly update a site I'm running through the terminal. I'm still not familiar with everything to do with urls, uris, etc. but I knew nothing about it before.
