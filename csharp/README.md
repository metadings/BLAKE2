﻿
**﻿BLAKE2 reference source code package - C# implementation**

```
Written in 2012 by Samuel Neves <sneves@dei.uc.pt>
Written in 2012 by Christian Winnerlein <codesinchaos@gmail.com>
Written in 2016 by Uli Riehm <metadings@live.de>

To the extent possible under law, the author(s) have dedicated all copyright
and related and neighboring rights to this software to the public domain
worldwide. This software is distributed without any warranty.

You should have received a copy of the CC0 Public Domain Dedication along with
this software. If not, see <http://creativecommons.org/publicdomain/zero/1.0/>.
```

**Usage**

```
using Blake2;
using System;
using System.Text;

string text = "HHHHAAAALLLLOOOOWWWWEEEELLLLTTTT";
byte[] bytes = Encoding.UTF8.GetBytes(text);
byte[] value;

using (var hash = new Blake2B()) value = hash.ComputeHash(bytes);
```

**Examples**

```
~/Blake2B.cs/bin/Debug $ echo -n HHHHAAAALLLLOOOOWWWWEEEELLLLTTTT > ./Hallo.txt

~/Blake2B.cs/bin/Debug $ mono ./Blake2B.exe --In=./Hallo.txt
bbc9e82dbf9a8897a5ec2f6836c381dbe27ac0b8ecd9912afa67459ef9474d70a52bf24ad5dcf29dbb8004d19a387b6516cc47ffae99d59d52efc013456c6b48
```

Ask questions on [stackoverflow](http://stackoverflow.com/questions/tagged/c%23+blake2) using tags `C#``Blake2` !

