# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

//
Name: Kane Kriz

Response:
The mystery() function in the attatched piece of code first checks if array a is of length 1, which if true, it simply returns that value as it is the only value within the array.

Second, var foo is defined as mystery(a.slice(1, a.length)) through recursion.
I was unfamilar with slice() so I used an attatched external resource to learn about it.
The line mystery(a.slice(1, a.length)) calls the function with what remains of array a, now without the first entry in the array.
This process repeats until an array of length 1 is called into mystery, which results in a[0] being returned as specified earlier.

Next, the results of the recursive calls are compared to a[0]. If a[0] is larger, a[0] is once again returned. However, if foo (which is the result of the prior made recursive calls)
is larger than a[0], foo is instead returned. This process repeats, comparing along the varying foo values and the original a[0] to see which of all the values within the array is greatest.
This results in the largest value within the array (and thus the largest recorded value of foo) being returned in the end of the function.

//

Resources / Citations:

I was not fully familar with the JS slice() method. I used this link to become informed properly on what the method does and its behaviors.
[https://www.w3schools.com/jsref/jsref_slice_string.asp](url)

“JavaScript String Slice() Method.” Www.w3schools.com, www.w3schools.com/jsref/jsref_slice_string.asp. Accessed 28 Jan. 2025.
