# Debugging Tutorial
> Author: Jeffrey Li
This Page showcases the processes of debugging MarkdownParse.java
## Fix #1
**Changes to MarkdownParse**
![](/LabReport2/bugfix1.png)
**Failure-inducing Input** \
[Test File](/LabReport2/testfiles/test-file2.md) \
**Failure Output** \
` Exception in thread "main" java.nio.file.NoSuchFileException: LabReport2\testfiles\test-file2.md
        at java.base/sun.nio.fs.WindowsException.translateToIOException(WindowsException.java:85)
        at java.base/sun.nio.fs.WindowsException.rethrowAsIOException(WindowsException.java:103)
        at java.base/sun.nio.fs.WindowsException.rethrowAsIOException(WindowsException.java:108)
        at java.base/sun.nio.fs.WindowsFileSystemProvider.newByteChannel(WindowsFileSystemProvider.java:236)
        at java.base/java.nio.file.Files.newByteChannel(Files.java:380)
        at java.base/java.nio.file.Files.newByteChannel(Files.java:432)
        at java.base/java.nio.file.Files.readAllBytes(Files.java:3288)
        at java.base/java.nio.file.Files.readString(Files.java:3366)
        at java.base/java.nio.file.Files.readString(Files.java:3325)
        at MarkdownParse.main(MarkdownParse.java:29) `
1. The bug was that the code did not check for possible scienrios where the implementation of the link was incomplete.
2. The symptom caused by this bug was that the program would throw an IOException.
3. The bug was fixed by adding lines of code that checked for the normality of each data before updating the ArrayList. 
___
## Fix #2
