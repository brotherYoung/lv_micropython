文档去看官方，这里放几个问题。
+ Q1: /usr/bin/env: ‘python’: No such file or directory
   + A1：sudo apt-get install python-is-python3
+ Q2: /usr/bin/python: No module named pip
   + A2: sudo apt install python3-pip
+ Q3: 'cmake' must be available on the PATH to use /home/young/esp-idf/tools/idf.py
   + A3: apt-get install cmake
+ Q4: fatal error: db.h: No such file or directory
   + A4：
+ Q5: 想重新编译应该怎么做？
   + Q5: make clean即可，如果想删除 esp-idf 与 lv_mirropython 重新下载编译，别忘了 whereis python, 删除 esp-idf 创建的 python 虚拟运行环境
