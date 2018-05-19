### 说明

本文档来自与[elasticsearch-cn](https://github.com/elasticsearch-cn/elasticsearch-definitive-guide)。由于，文档是asciidoc格式的，我习惯html格式故装换为html。放上来方便大家使用。

### 转换脚本

```python
#!/usr/bin/env python3
# coding=utf-8
# asciidoc 转 html
import os,sys
import re
args = sys.argv[1]

for root,dirs,files in os.walk(args):
    for f in files:
        if re.match(r'^.*\.asciidoc$', f):
            filepath = root + "/" + f
            print(filepath)
            os.popen("asciidoctor " + filepath)
```

### 要求

装换前

&emsp;装换之前

`sudo apt update`

`sudo apt install asciidoctor`

准备好后开始

`python3 youscript.py 此处为asciidoc文件的路径`

### 谢谢

### :)