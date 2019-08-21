-- 大端小端

### DOS头
* 固定长度为64bit（字节）
* 前两位是魔数(USHORT e_magic),固定值|4D|5A|(0x5A4D)
* 后四位是文件头偏移量(LONG e_lfanew),采用小端序

### PE文件头
* 前四位是PE文件头标志(DWORD Signature),固定值|45|50|00|00|(0x00005045)
