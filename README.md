文档去看官方，这里放几个问题。
+ Q1: /usr/bin/env: ‘python’: No such file or directory
   + A1：sudo apt-get install python-is-python3
+ Q2: /usr/bin/python: No module named pip
   + A2: sudo apt install python3-pip
+ Q3: 'cmake' must be available on the PATH to use /home/young/esp-idf/tools/idf.py
   + A3: apt-get install cmake
+ Q4: fatal error: db.h: No such file or directory
   + A4：少操作了一个步骤，先 cd /lv_micropython/ports/esp32 执行一次 make submodules，然后再 make 编译。（整整一周才发现这个细节）
+ Q5: 想重新编译应该怎么做？
   + Q5: make clean即可，如果想删除 esp-idf 与 lv_mirropython 重新下载编译，别忘了 whereis python, 删除 esp-idf 创建的 python 虚拟运行环境



使用中遇到的一些问题：
+ Q1: 如何在 windows 中打开 wsl 文件夹
   + A1：/mnt/c/Windows/explorer.exe .
+ Q2: 重新编译了为什么还提示 ili9341 micropython driver requires defining LV_COLOR_DEPTH=16
   + A2：在执行新的 make 命令之前，需要 make clean
