title: Shell Function return string 
date: 2015-08-30 21:46:33
tags: [shell]
---

Below example work, but performance may be an issue as it spawn a subprocess

``` bash

#!/bin/bash

function functionReturnStringValue() {
	echo "HIHI $1 $2"
}

PARAM1="OTHER"
RESULT=$(functionReturnStringValue $PARAM1 "PARAM2")

echo $RESULT


```

it return 

``` bash

lujunjie@mac:~/code/tempDir/shell_study > ./run.sh 
HIHI OTHER PARAM2

```