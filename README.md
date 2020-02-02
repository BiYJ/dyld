1. 安全防护

    `DYLD_INSERT_LIBRARIES`  环境变量
    
    `__RESTRICT`  machO 文件的 segment
    
    1. iOS10 以下 build setting - Other linker flags 设置 `-Wl,-sectcreate,__RESTRICT,__restrict,/dev/null`
    
        iOS10 以后，苹果的 DYLD 不再检测 RESTRICT 字段
    
    1. 查找是否有 `__RESTRICT,__restrict`，没有就知道被黑客攻击了

1. 攻击

    `tweak` 注入 hook