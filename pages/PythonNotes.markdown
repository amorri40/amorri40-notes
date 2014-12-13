---
title: Python Notes by AlasdairMorrison.com
---

# General Python



#### UTF-8 Header
``` python
# -*- coding: utf-8 -*- 
```

#### String Formatting
``` python
var = '%(foo)s %(foo)s %(foo)s' % { 'foo': 'look_at_me_three_times' }
```
#### Installing pip libraries that cause clang error
``` python
sudo ARCHFLAGS=-Wno-error=unused-command-line-argument-hard-error-in-future pip install lxml
```
### Naming (PEP-8)
#### Python Filename
Lowercase with underscores e.g:
``` python
from nib import Nib
from foo import Foo
from spam.eggs import Eggs, FriedEggs
```
https://stackoverflow.com/questions/711884/python-naming-conventions-for-modules/711908#711908 

### Testing in Python
#### doctest
doctest is great it tests the example in the docstring but it can also test code for tutorials and books. This would be awesome for writing books!
This will make sure function_name returns 0.
``` python
“””
>>>function_name()
0
“””
```

#### pytest
seems to be a smarter version of the default unittest module, gives much more useful output for why the test failed!

### pyCharm
#### creating a test in pyCharm
This was surprisingly hard to find but when you know where it is its very handy. Right click the class you want to create a test for and select “Go to” -> “Test” this will give you the option to create a new test
Set default file template

### Dates and Times

http://www.cyberciti.biz/faq/howto-get-current-date-time-in-python/ 

#### Print date and Time
``` python
import time
print (time.strftime("%H:%M:%S"))
 
####  12 hour format
print (time.strftime("%I:%M:%S"))

####  Date
print (time.strftime("%d/%m/%Y"))
```
### Files and Directories

#### Get list of Files and Directories in current location
``` python
current_working_path = os.getcwd()
for (dirpath, dir_names, file_names) in walk(current_working_path):
    for directory_name in dir_names:
        print (directory_name)
    for file_name in file_names:
        print (file_name)
    break
```
#### Get File created date
http://stackoverflow.com/questions/237079/how-to-get-file-creation-modification-date-times-in-python 

#### Get Current Working Directory
``` python
import os
current_working_path = os.getcwd()
```
#### Send to Trash

``` python
# http://www.hardcoded.net/articles/send-files-to-trash-on-all-platforms.htm
pip install send2trash 
```

#### Get if file exists
``` python
os.path.exists
```

#### Using Python Libraries
### Wand (imageMagick)
The most up-to-date and developed imageMagick API for python is wand
http://docs.wand-py.org/en/0.3.7/ 

### sh
Use bash in python like functions!
