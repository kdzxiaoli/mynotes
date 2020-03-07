是用c语言实现的
底层实现主要通过汇编lock前缀指令
它会锁定这块内存区域的缓存 并回写到主内存
会将当前处理器缓存行的数据立即写回答系统内存
这个写回内存的操作回引起其他CPU缓存无效 MESI


实际在store 的时候加锁了  写完unlock


加入volatile 开启mesi 



Java 程序汇编代码查看
下载两个包  放入bin
-server -Xcomp -XX:+UnlockDiaglosticVMOptions
-XX:+PrintAssembly -XX:CompileCommand=compileonly,
*VolatileVisibilityTest.prepareData
