# gdb的基本命令
为了使用gdb功能，我们一般需要在编译的时候加上-o选项
随后通过 gdb ./要调试的文件

---
### 基础控制
- run arg1 "参数" 运行程序
- quit 退出调试器

---
### 断点管理
- b main 在main() 开头设置断点
- b 42 在第42行设置断点
- b file.cpp:100 在指定文件第100行设置断点
- info breakpoints 显示所有断点
- delete 3 删除3号断点
- disable 2 临时禁用2号断点
- enable 2 重新启用2号断点
- clear 清除所有断点

---
### 执行控制
- next 跳过函数调用，执行下一行代码
- step 执行下一行（进入函数内部）
- continue 运行到下一个断点
- finish 执行完当前函数并暂停
- until 100 运行到行号100

---
### 查看数据和源码
- list 查看上下文
- print 变量 打印变量值

---
### 调用栈分析
- backtrace 查看调用栈
- frame 2 查看第二层函数调用
- info locals 查看当前帧的变量

---
### 多线程调试
- info threads 列出所有线程
- thread 3 切换到线程3
- thread apply all backtrace 所有线程打印调用栈

---
- bt 查看崩溃点
- x/20xb 0x7fffffffdc80  # 查看16进制内存
- x/10dw &array   # 查看10个十进制word
- info registers 检查寄存器值