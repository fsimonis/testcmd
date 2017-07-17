# testcmd
A small python program for simple blackbox-testing a command given an input and expected output.

## Example
Assuming you need to test a program `prog` that is supposed to capitalise every word of the input and remove whitespaces.
Create an input and an output file for the test case.

input.txt
```
This is a simple example
```

output.txt
```
ThisIsASimpleExample
```

To check this scenario and use the return value only:
```
$ testcmd input.txt output.txt prog
```
Use `-v` or `--verbose` to see the expected and actual output in case of a mismatch:
```
$ testcmd -v input.txt output.txt prog
Outputs do not match!
Received: b'This Is A Simple Example'
Expected: b'ThisIsASimpleExample'
```

## Credits
This program is inspired and motivated by the subreddit [dailyprogrammer](https://www.reddit.com/r/dailyprogrammer/).
