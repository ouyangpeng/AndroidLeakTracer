# AndroidLeakTracer

native内存泄漏检测工具LeakTracer的使用Demo


参考链接：
https://fucknmb.com/2017/06/05/Android-NDK-%E5%86%85%E5%AD%98%E6%B3%84%E9%9C%B2%E6%A3%80%E6%B5%8B/
https://www.jianshu.com/p/9058f0514416?utm_campaign=maleskine&utm_content=note&utm_medium=seo_notes&utm_source=recommendation


本案例查看效果为：

在 AndroidLeakTracer\leak-tracer-helpers 目录下 ，右键 使用 Git Bash Hear，然后模拟Linux环境运行下面的脚本

$ ./leak-analyze-addr2line libleaktracer.so leakLog.txt

Processing "leakLog.txt" log for "libleaktracer.so"
Matching addresses to "libleaktracer.so"
found 2 leak(s)
C:\msys64\mingw64\bin\addr2line.exe: DWARF error: could not find variable specification at offset 54
1 bytes lost in 1 blocks (one of them allocated at 14028.301603), from following call stack:
        E:/AndroidLeakTracer/app/src/main/cpp/libleaktracer/src/MemoryTrace.cpp:310
        E:/AndroidLeakTracer/app/src/main/cpp/libleaktracer/include/MemoryTrace.hpp:384
        E:/AndroidLeakTracer/app/src/main/cpp/libleaktracer/src/AllocationHandlers.cpp:29
        E:/AndroidLeakTracer/app/src/main/cpp/leaktracer_jni.cpp:63
100 bytes lost in 1 blocks (one of them allocated at 14028.301472), from following call stack:
        E:/AndroidLeakTracer/app/src/main/cpp/libleaktracer/src/MemoryTrace.cpp:310
        E:/AndroidLeakTracer/app/src/main/cpp/libleaktracer/include/MemoryTrace.hpp:384
        E:/AndroidLeakTracer/app/src/main/cpp/libleaktracer/src/AllocationHandlers.cpp:77
        E:/AndroidLeakTracer/app/src/main/cpp/leaktracer_jni.cpp:57
