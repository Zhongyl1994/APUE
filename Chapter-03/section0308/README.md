1. 调用write函数向打开文件写数据

2. 返回值成功是写入文件的字节数，通常于参数nbytes相同。否则，表示出错，出错的常见
原因是：
    
    2.1 磁盘空间写满

    2.2 超过了一个给定进程的文件长度限制

3. 对于普通文件，写操作从文件的当前偏移量处开始。如果打开文件时，指定了O_APPEND选项
则在每次写操作前，将文件偏移量设置在文件的当前结尾处。在一次成功写之后，该文件的偏移量
增加实际写的字节数。
