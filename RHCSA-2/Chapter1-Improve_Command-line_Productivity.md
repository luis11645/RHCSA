# 1.2 Loops and Conditional Constructs in Scripts #

## Examples of using `for` loop conditional ##

* for HOST in host1 host2 host3; do echo $HOST; done

In this example `HOST` ins the variable name and it can be whatever and `host1 host2 and host3` is the differents values that the variable `HOST` is goint to have until it process all the strings

We can use the test shell scripts format by using one of the following methods:
* `test 1 -gt 0 ; echo$?`
* `[ 1 -gt 0 ]; echo$?`
* `[[ 1 -gt 0 ]]; echo$?` this new method supports file name globbing and regex
