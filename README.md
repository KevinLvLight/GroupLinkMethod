# 成组链接法
操作系统原理实验

### 环境
> Ubuntu (虚拟机)
### 基本数据结构要求
```c
#define BLOCKSIZ  512 //磁盘块大小 
#define NICFREE   10  //每组的块数 
#define FILEBLK   25  //文件区磁盘块总数 
#define DATASTART 11  //文件区开始块
```
```c
struct filsys                     // 超级块部分数据结构 
{  
   unsigned int s_nfree;          //空闲盘块数
   unsigned short s_pfree;        //空闲盘块指针 
   unsigned int s_free[NICFREE];  //空闲盘块堆栈 
};
```
### 运行说明
> 输入fd打印当前分配情况

> 输入 alloc 进行分配

> 输入 bfree 回车后再输入盘块号进行回收

> 输入 exit 退出运行

### 其他
> 应该使用数组或者链表来存储表示已分配的盘块的，以后再改
