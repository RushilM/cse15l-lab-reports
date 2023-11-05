# Lab Report 3
## Part 1 - Bugs
*A failure inducing input for the buggy program*

"reverseInPlace(int[] arr)" a function within the the class ArrayExamples contains a bug and is shown below:
```
 static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
*A failure-inducing input for the buggy program, as a JUnit test:*

```
  @Test
  public void testReversedinPlace2(){
    int[] input1 = {1,2,3,4,5};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{5,4,3,2,1}, input1);
  }
```
*An input that doesn't induce a failure, as a JUnit test:*

```
  @Test
  public void testReversedinPlace3(){
    int[] input1 = {1};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{1}, input1);
  }
```



*The symptom, as the output of running the tests*
![Alt text](Lab3Screenshot1.png)


## Part 2



## Part 3

Using RSA encryption to save a private key on to your public computer is something I didn't know about. I think this is a great way to not have to enter your password when accessing a remote server from a trusted personal device. It was cool to see the physical RSA key that was being used aswell, because we know that RSA encryption is used widely today but we do not actually get to see the key that is in use. 
