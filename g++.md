编译简单的C程序：

    g++ -g -Wall XXX.c -o XXX

将XXX.c编译为机器码并存储在可执行文件XXX中。

[-g]表示生成的目标文件中带有调试信息。

[-Wall] Warning all, 开启所有常用Warning。

[-o]指定可执行文件名， 如果不添加[-o], 则使用默认的输入文件名‘a.out’。