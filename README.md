### 说明

本文档来自与[elasticsearch-cn](https://github.com/elasticsearch-cn/elasticsearch-definitive-guide)。由于，文档是asciidoc格式的，我习惯html格式故装换为html。放上来方便大家使用。

`git clone git@github.com:imjdl/elasticsearch-guide-html.git`下载下来直接使用就好。

---------------------

如果您想自己转换可以参考下面

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

转换前

`sudo apt update`

`sudo apt install asciidoctor`

准备好后开始

`python3 youscript.py 此处为asciidoc文件的路径`

### 谢谢

### :)
