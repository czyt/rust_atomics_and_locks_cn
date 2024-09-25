## [第一章：Rust 并发基础](./1_Basic_of_Rust_Concurrency.md)

[//]: # ()
[//]: # (* [Rust 中的线程]&#40;./1_Basic_of_Rust_Concurrency.md#rust-中的线程&#41;)

[//]: # (* [作用域内的线程]&#40;./1_Basic_of_Rust_Concurrency.md#作用域内的线程&#41;)

[//]: # (* [共享所有权以及引用计数]&#40;./1_Basic_of_Rust_Concurrency.md#共享所有权以及引用计数&#41;)

[//]: # (  * [静态值（static）]&#40;./1_Basic_of_Rust_Concurrency.md#静态值static&#41;)

[//]: # (  * [泄漏（Leak）]&#40;./1_Basic_of_Rust_Concurrency.md#泄漏leak&#41;)

[//]: # (  * [引用计数]&#40;./1_Basic_of_Rust_Concurrency.md#引用计数&#41;)

[//]: # (* [借用和数据竞争]&#40;./1_Basic_of_Rust_Concurrency.md#借用和数据竞争&#41;)

[//]: # (* [内部可变性]&#40;./1_Basic_of_Rust_Concurrency.md#内部可变性&#41;（[Cell]&#40;./1_Basic_of_Rust_Concurrency.md#cell&#41;、[RefCell]&#40;./1_Basic_of_Rust_Concurrency.md#refcell&#41;、[互斥锁以及读写锁]&#40;./1_Basic_of_Rust_Concurrency.md#互斥锁和读写锁&#41;、[Atomic]&#40;./1_Basic_of_Rust_Concurrency.md#atomic&#41;、[UnsafeCell]&#40;./1_Basic_of_Rust_Concurrency.md#unsafecell&#41;）)

[//]: # (* [线程安全：Send 和 Sync]&#40;./1_Basic_of_Rust_Concurrency.md#线程安全send-和-sync&#41;)

[//]: # (* [锁：互斥锁和读写锁]&#40;./1_Basic_of_Rust_Concurrency.md#锁互斥锁和读写锁&#41;)

[//]: # (  * [Rust 的互斥锁]&#40;./1_Basic_of_Rust_Concurrency.md#rust-的互斥锁&#41;)

[//]: # (  * [锁中毒]&#40;./1_Basic_of_Rust_Concurrency.md#锁中毒poison&#41;)

[//]: # (  * [读写锁]&#40;./1_Basic_of_Rust_Concurrency.md#读写锁&#41;)

[//]: # (* [等待：阻塞和条件变量]&#40;./1_Basic_of_Rust_Concurrency.md#等待-阻塞park和条件变量&#41;)

[//]: # (  * [线程阻塞]&#40;./1_Basic_of_Rust_Concurrency.md#线程阻塞&#41;)

[//]: # (  * [条件变量]&#40;./1_Basic_of_Rust_Concurrency.md#条件变量&#41;)

[//]: # (* [总结]&#40;./1_Basic_of_Rust_Concurrency.md#总结&#41;)

## [第二章：Atomic](./2_Atomics.md)

[//]: # (* [Atomic 的加载和存储操作]&#40;./2_Atomics.md#atomic-的加载和存储操作&#41;)

[//]: # (  * [示例：停止标识]&#40;./2_Atomics.md#示例停止标识&#41;)

[//]: # (  * [示例：进度报道]&#40;./2_Atomics.md#示例进度报道&#41;)

[//]: # (    * [同步]&#40;./2_Atomics.md#同步&#41;)

[//]: # (  * [示例：惰性初始化]&#40;./2_Atomics.md#示例惰性初始化&#41;)

[//]: # (* [获取并修改操作]&#40;./2_Atomics.md#获取并修改操作&#41;)

[//]: # (  * [示例：来自多线程的进度报道]&#40;./2_Atomics.md#示例来自多线程的进度报道&#41;)

[//]: # (  * [示例：统计数据]&#40;./2_Atomics.md#示例统计数据&#41;)

[//]: # (  * [示例：ID 分配]&#40;./2_Atomics.md#示例id-分配&#41;)

[//]: # (* [比较并交互操作]&#40;./2_Atomics.md#比较并交换操作&#41;)

[//]: # (  * [示例：没有溢出的 ID 分配]&#40;./2_Atomics.md#示例没有溢出的-id-分配&#41;)

[//]: # (  * [示例：惰性一次性初始化]&#40;./2_Atomics.md#示例惰性一次性初始化&#41;)

[//]: # (* [总结]&#40;./2_Atomics.md#总结&#41;)

## [第三章：内存排序](./3_Memory_Ordering.md)

[//]: # (* [重排和优化]&#40;./3_Memory_Ordering.md#重排和优化&#41;)

[//]: # (* [内存模型]&#40;./3_Memory_Ordering.md#内存模型&#41;)

[//]: # (* [Happens-Before 关系]&#40;./3_Memory_Ordering.md#happens-before-关系&#41;)

[//]: # (  * [spawn 和 join]&#40;./3_Memory_Ordering.md#spawn-和-join&#41;)

[//]: # (* [Relaxed 排序]&#40;./3_Memory_Ordering.md#relaxed-排序&#41;)

[//]: # (* [Release 和 Acquire 排序]&#40;./3_Memory_Ordering.md#release-和-acquire-排序&#41;)

[//]: # (  * [示例：锁定]&#40;./3_Memory_Ordering.md#示例锁定&#41;)

[//]: # (  * [示例：使用间接的方式惰性初始化]&#40;./3_Memory_Ordering.md#示例使用间接的方式惰性初始化&#41;)

[//]: # (* [Consume 排序]&#40;./3_Memory_Ordering.md#consume-排序&#41;)

[//]: # (* [顺序一致性排序]&#40;./3_Memory_Ordering.md#顺序一致性排序&#41;)

[//]: # (* [屏障（Fence）]&#40;./3_Memory_Ordering.md#屏障fence2&#41;)

[//]: # (* [常见的误解]&#40;./3_Memory_Ordering.md#常见的误解&#41;)

[//]: # (* [总结]&#40;./3_Memory_Ordering.md#总结&#41;)

## [第四章：构建我们自己的自旋锁](./4_Building_Our_Own_Spin_Lock.md)

[//]: # (* [一个最小实现]&#40;./4_Building_Our_Own_Spin_Lock.md#一个最小实现&#41;)

[//]: # (* [一个不安全的自旋锁]&#40;./4_Building_Our_Own_Spin_Lock.md#一个不安全的自旋锁&#41;)

[//]: # (* [使用锁守卫的安全接口]&#40;./4_Building_Our_Own_Spin_Lock.md#使用锁守卫的安全接口&#41;)

[//]: # (* [总结]&#40;./4_Building_Our_Own_Spin_Lock.md#总结&#41;)

## [第五章：构建我们自己的 Channel](./5_Building_Our_Own_Channels.md)

[//]: # (* [一个简单的以 mutex 为基础的 Channel]&#40;./5_Building_Our_Own_Channels.md#一个简单的以-mutex-为基础的-channel&#41;)

[//]: # (* [一个不安全的一次性 Channel]&#40;./5_Building_Our_Own_Channels.md#一个不安全的一次性-channel&#41;)

[//]: # (* [通过运行时检查来达到安全]&#40;./5_Building_Our_Own_Channels.md#通过运行时检查来达到安全&#41;)

[//]: # (* [通过类型来达到安全]&#40;./5_Building_Our_Own_Channels.md#通过类型来达到安全&#41;)

[//]: # (* [借用以避免内存分配]&#40;./5_Building_Our_Own_Channels.md#借用以避免内存分配&#41;)

[//]: # (* [阻塞]&#40;./5_Building_Our_Own_Channels.md#阻塞&#41;)

[//]: # (* [总结]&#40;./5_Building_Our_Own_Channels.md#总结&#41;)

## [第六章：构建我们自己的“Arc”](./6_Building_Our_Own_Arc.md)

[//]: # (* [基础的引用计数]&#40;./6_Building_Our_Own_Arc.md#基础的引用计数&#41;)

[//]: # (  * [测试它]&#40;./6_Building_Our_Own_Arc.md#测试它&#41;)

[//]: # (  * [可变性]&#40;./6_Building_Our_Own_Arc.md#可变性&#41;)

[//]: # (* [Weak 指针]&#40;./6_Building_Our_Own_Arc.md#weak-指针&#41;)

[//]: # (  * [测试它]&#40;./6_Building_Our_Own_Arc.md#测试它2&#41;)

[//]: # (  * [优化]&#40;./6_Building_Our_Own_Arc.md#优化&#41;)

[//]: # (* [总结]&#40;./6_Building_Our_Own_Arc.md#总结&#41;)

## [第七章：理解处理器](./7_Understanding_the_Processor.md)

[//]: # (* [处理器指令]&#40;./7_Understanding_the_Processor.md#处理器指令&#41;)

[//]: # (  * [加载和存储操作]&#40;./7_Understanding_the_Processor.md#加载和存储操作&#41;)

[//]: # (  * [读并修改并写操作]&#40;./7_Understanding_the_Processor.md#读并修改并写操作&#41;)

[//]: # (    * [x86 lock 前缀]&#40;./7_Understanding_the_Processor.md#x86-lock-前缀&#41;)

[//]: # (    * [x86 比较并交换指令]&#40;./7_Understanding_the_Processor.md#x86-比较并交换指令&#41;)

[//]: # (  * [ll-和-sc-指令]&#40;./7_Understanding_the_Processor.md#ll-和-sc-指令&#41;)

[//]: # (    * [arm-的-ldxr-和-stxr-指令]&#40;./7_Understanding_the_Processor.md#arm-的-ldxr-和-stxr-指令&#41;)

[//]: # (    * [arm-的比较并交换操作]&#40;./7_Understanding_the_Processor.md#arm-的比较并交换操作&#41;)

[//]: # (* [缓存]&#40;./7_Understanding_the_Processor.md#缓存3&#41;)

[//]: # (  * [缓存一致性]&#40;./7_Understanding_the_Processor.md#缓存一致性&#41;)

[//]: # (    * [write-through 协议]&#40;./7_Understanding_the_Processor.md#write-through-协议&#41;)

[//]: # (    * [MESI 协议]&#40;./7_Understanding_the_Processor.md#mesi-协议4&#41;)

[//]: # (  * [对性能的影响]&#40;./7_Understanding_the_Processor.md#对性能的影响&#41;)

[//]: # (* [重排]&#40;./7_Understanding_the_Processor.md#重排&#41;)

[//]: # (* [内存排序]&#40;./7_Understanding_the_Processor.md#内存排序&#41;)

[//]: # (  * [x86-64：强排序]&#40;./7_Understanding_the_Processor.md#x86-64强排序&#41;)

[//]: # (  * [ARM64：弱排序]&#40;./7_Understanding_the_Processor.md#arm64弱排序&#41;)

[//]: # (  * [一个实验]&#40;./7_Understanding_the_Processor.md#一个实验&#41;)

[//]: # (  * [内存屏障]&#40;./7_Understanding_the_Processor.md#内存屏障&#41;)

[//]: # (* [总结]&#40;./7_Understanding_the_Processor.md#总结&#41;)

## [第八章：操作系统原语](./8_Operating_System_Primitives.md)

[//]: # (* [使用内核接口]&#40;./8_Operating_System_Primitives.md#使用内核接口&#41;)

[//]: # (* [POSIX]&#40;./8_Operating_System_Primitives.md#posix&#41;)

[//]: # (  * [在 Rust 中包装类型]&#40;./8_Operating_System_Primitives.md#在-rust-中包装类型&#41;)

[//]: # (* [Linux]&#40;./8_Operating_System_Primitives.md#linux&#41;)

[//]: # (  * [Futex]&#40;./8_Operating_System_Primitives.md#futex&#41;)

[//]: # (  * [Futex 操作]&#40;./8_Operating_System_Primitives.md#futex-操作&#41;)

[//]: # (  * [优先继承 Futex 操作]&#40;./8_Operating_System_Primitives.md#优先继承-futex-操作&#41;)

[//]: # (* [macOS]&#40;./8_Operating_System_Primitives.md#macos&#41;)

[//]: # (  * [os_unfair_lock]&#40;./8_Operating_System_Primitives.md#os_unfair_lock&#41;)

[//]: # (* [Windows]&#40;./8_Operating_System_Primitives.md#windows&#41;)

[//]: # (  * [重量级内核对象]&#40;./8_Operating_System_Primitives.md#重量级内核对象&#41;)

[//]: # (  * [轻量级对象]&#40;./8_Operating_System_Primitives.md#轻量级对象&#41;)

[//]: # (    * [精简的读写锁（SRW）]&#40;./8_Operating_System_Primitives.md#精简的读写srw锁5&#41;)

[//]: # (  * [基于地址的等待]&#40;./8_Operating_System_Primitives.md#基于地址的等待&#41;)

[//]: # (* [总结]&#40;./8_Operating_System_Primitives.md#总结&#41;)

## [第九章：构建我们自己的「锁」](./9_Building_Our_Own_Locks.md)

[//]: # (* [Mutex]&#40;./9_Building_Our_Own_Locks.md#mutex&#41;)

[//]: # (  * [避免系统调用]&#40;./9_Building_Our_Own_Locks.md#避免系统调用&#41;)

[//]: # (  * [进一步优化]&#40;./9_Building_Our_Own_Locks.md#进一步优化&#41;)

[//]: # (  * [基准测试]&#40;./9_Building_Our_Own_Locks.md#基准测试&#41;)

[//]: # (* [条件变量]&#40;./9_Building_Our_Own_Locks.md#条件变量&#41;)

[//]: # (  * [避免系统调用2]&#40;./9_Building_Our_Own_Locks.md#避免系统调用2&#41;)

[//]: # (  * [避免虚假唤醒]&#40;./9_Building_Our_Own_Locks.md#避免虚假唤醒&#41;)

[//]: # (* [读写锁]&#40;./9_Building_Our_Own_Locks.md#读写锁&#41;)

[//]: # (  * [避免 writer 忙碌循环]&#40;./9_Building_Our_Own_Locks.md#避免-writer-忙碌循环&#41;)

[//]: # (  * [避免 writer 陷入饥饿]&#40;./9_Building_Our_Own_Locks.md#避免-writer-陷入饥饿&#41;)

[//]: # (* [总结]&#40;./9_Building_Our_Own_Locks.md#总结&#41;)

## [第十章：理念和灵感](./10_Ideas_and_Inspiration.md)

[//]: # (* [信号量]&#40;./10_Ideas_and_Inspiration.md#信号&#41;)

[//]: # (* [RCU]&#40;./10_Ideas_and_Inspiration.md#rcu&#41;)

[//]: # (* [无锁链表]&#40;./10_Ideas_and_Inspiration.md#无锁链表&#41;)

[//]: # (* [基于队列的锁]&#40;./10_Ideas_and_Inspiration.md#基于队列的锁&#41;)

[//]: # (* [基于阻塞的锁]&#40;./10_Ideas_and_Inspiration.md#基于阻塞的锁&#41;)

[//]: # (* [顺序锁]&#40;./10_Ideas_and_Inspiration.md#顺序锁sequence-lock&#41;)

[//]: # (* [教学材料]&#40;./10_Ideas_and_Inspiration.md#教学材料&#41;)

## [索引](./attachment.md)
