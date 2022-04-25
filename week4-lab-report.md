# Debugging Tutorial
> Author: Jeffrey Li \
This Page showcases the processes of debugging MarkdownParse.java
___
## Fix #1
**Changes to MarkdownParse.java**
![](/LabReport2/bugfix1.png)
**Failure-inducing Input** \
[Test File](/LabReport2/testfiles/test-file2.md) \
**Failure Output** \
`Exception in thread "main" java.lang.StringIndexOutOfBoundsException: begin 0, end -1, length 2
        at java.base/java.lang.String.checkBoundsBeginEnd(String.java:4601)
        at java.base/java.lang.String.substring(String.java:2704)
        at MarkdownParse.getLinks(MarkdownParse.java:19)
        at MarkdownParse.main(MarkdownParse.java:30)`
1. The bug was that the code did not check for possible scienrios where the implementation of the link was incomplete.
2. The symptom caused by this bug was that the program would throw an IOException.
3. The bug was fixed by adding lines of code that checked for the normality of each data before updating the ArrayList. 
___
## Fix #2
**Changes to MarkdownParse.java**
![](/LabReport2/bugfix2.png)
**Failure-inducing Input** \
[Test File](/LabReport2/testfiles/test-file3.md) \
**Failure Output** \
`[someRandomImage.png]`
1. The bug was that the code did check for the '!' character infront of the implemented links.
2. The symptom was that the program could not distinguish between image links and file/web links.
3. The bug was fixed bying adding lines of code that checks if there is a '!' character infront of the link, and if there is, the program would ignore that link.
___
## Fix #3
**Changes to MarkdownParse.java**
![](/LabReport2/bugfix3.png)
**Failure-induing Input** \
[Test File](/LabReport2//testfiles/test-file4.md) \
**Failure Output** \
```
[                                              something.html]
```
1. The bug was that the code could not reconigze space characters within the link.
2. The symptom resulted from this bug was that the ouput would contain long sequences of spaces next to the link if the input conatained such sequence of white spaces.
3. The bug was fixed by adding a line of code that replaced all the white spaces in the link with empty chars, thereby elimnating any space char in the link.