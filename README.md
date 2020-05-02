Python3 build in Sublime
=========================
Make sure you have Python3 installed on your system.
This works for Mac, Linux and Windows

Go to **Tools > Build System > New Build System**.

Rename the file to "Python3.sublime-build" and change the code to:

```
{
 "cmd": ["python3", "-u", "$file"],
 "file_regex": "^[ ]File \"(...?)\", line ([0-9]*)",
 "selector": "source.python"
}
```
Safe the file and select Python3 from the build menu. 

To try it out:
``` 
import sys
print(sys.version)
``` 
Save the file, press **CTRL-b** and it shows the correct version.

If it doesn't work you could use the complete path in the build. To change the build, you'll have to change the file manually on your system by going to: 

``` 
Linux: ~/.config/sublime-text-3/Packages
OS X: ~/Library/Application Support/Sublime Text 3/Packages
Windows: C:\Users\<insert-username>\AppData\Roaming\Sublime Text 3\Packages

``` 
Check your Python3 path with:
```
Lunx: which python3
OS X: type -a python3 
Windows: where python3
```

Add the path to the buildfile (so for example change python3 to /usr/bin/python3).


