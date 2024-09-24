---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Types



## Position

Position is stored in tuple. To allow more controls over the position, more params are allowed behind the coordinate.

#### Basic:&#x20;

The following position is X10 Y20 Z30

```
(10, 20, 30)
```

#### Additional:

The following position is X10 Z20, plus P10 Q20

```
(10, , 20, P=10, Q=20)
```
