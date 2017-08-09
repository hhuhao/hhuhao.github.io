### Important

Bit is a good alogrithm.

### Problem

#### Description

Give you some operate.

$0\ l\ r\ w\ \ \  $:$f_{l..r}+=w$

$1\ x\ \ \ \ \ \ \ \ $:Ask $f_x$

#### [Sample](\sample\)

#### Constraints

|  Data   |   n    |   m    |
| :-----: | :----: | :----: |
| $1..3$  | $10^3$ | $10^3$ |
| $4..10$ | $10^5$ | $10^5$ |

#### Solution

$0$:

```c++
add(l,w);
add(r+1,-w);
```

$1$:

```c++
query(x);
```

#### [Code](\code\)

