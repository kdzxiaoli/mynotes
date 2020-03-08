阻塞

从用户态 到内核态  内核太空间  用户空间  一直阻塞

非阻塞塞 
一直去问 有数据吗   有了  则从内核太拷贝到用户态   这个拷贝是阻塞

I/O复用
由selector 监听哪个 可以读 哪个可以写   

信号I/O
定义信号 有数据了通知   内核太到用户态  阻塞

异步I/O
从内核态到用户态数据拷贝你好了  才通知

NIO 面向缓冲区

IO 面向流

堆内存   非堆内存  

非堆内存 需要拷贝到虚拟机外一块内存  然后拷贝到内核态


flip  position=0 limit=写入的元素个数  进入读模式 
mark 标记位置 reset回退到 mark的位置 
compact 进入写模式 未读元素置到数组头部  position 指向未读元素个数的位置 limit  指向capacity position后有的元素会被替换



## 通道

FileChannel：文件通道，用于文件的读和写
DatagramChannel：用于 UDP 连接的接收和发送
SocketChannel：把它理解为 TCP 连接通道，简单理解就是 TCP 客户端
ServerSocketChannel：TCP 对应的服务端，用于监听某个端口进来的请求


clear 回到初始状态

slice  返回limit-position之间的内容  是浅拷贝 修改一个  影响另一个
duplicate 将源bf的所有数据 指针都拷贝一份 共用一份数据   浅拷贝
array 将源bf的内容拷贝一份 浅拷贝
get 获取limit -position之间的内容  源bf position = limit   不共享数据


