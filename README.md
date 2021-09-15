# regx

1- find target string inside qoutes simple
```
import re

txt = "8 times before [] = 'something' 11:45 AM"
x = re.findall("\'{1}[a-zA-Z]+\'{1}", txt)
print(x)
if x:
  print("Yes, there is at least one match!")
else:
  print("No match")

```

2- find target string inside qoutes simple harder
```
import re

# can be used for translate json files with php
txt = "The rain in $['lang']= 'Hello'  $['lang']= 'world' Spain"
x = re.search("[\${1}\={1}\'{2}]", txt)

if x:
  y = re.findall("\s{1}\'{1}[a-zA-Z]+\'{1}", txt)
  print(y)
  
  
else:
  print("No match")


```
