### Somehow find the flag on this very limited shell. 

* The `ls` and `cat` command available on the shell were custom created and didn't support any of the useful functionality. After a lot of trial and error. I found that the wildcard expansion is allowed on the restricted shell.

* After that it was a matter of just using one of the classis tricks to leak the first line of the file.

Image goes here