### This question is about combining the best of two worlds!

#### From the name gets and the js file, it's clear that we need to trigger buffer overflow on the native binary in order to get the flag. After some effort, I came up with this request to extract the flag.

Image goes here

* The rational behind this request is to bypass the length check by sending the parameter twice. As in 

```
/prime?n=100&n=asdfasdfasdfasasdfasdf
```

This way, node js will receive n as a list containing 2 items (bypassing the length protection). When the input is passed to the binary, it'll be the string representation of the list (big enough to trigger the bof and get the flag.)