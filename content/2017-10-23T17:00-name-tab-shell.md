Title: How to name tab in shell?
Date: 2017-10-23 17:00
Category: os admin devops 

# Problem 😱

You have multiple shell tabs with not really nice names.

![plain shell name](https://i.imgur.com/jXKzEqT.png) 


---

# Solution 🤓

```
function name() { echo -ne "\\033]0;$@\\007"; }
```

usage:
```
| => name writing blog post
```

result:

![nice shell name](https://i.imgur.com/wI7Ax7f.png)
