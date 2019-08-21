-- 大端小端

### DOS头
* 固定长度为64bit（字节）
* 前两位是魔数(USHORT e_magic),固定值|4D|5A|(0x5A4D)
* 后四位是文件头偏移量(LONG e_lfanew),采用小端序

### PE文件头(aka NT头)
* 前四位是PE文件头标志(DWORD Signature),固定值|45|50|00|00|(0x00005045)
* 紧接着两位(第5·6位)是运行平台(WORD Machine)，一般为|4C|01|(0x014C)
* 再后两位(第7·8位)是section个数(WORD NumberOfSections),不固定
* 再后四位(第9·10·11·12位)是时间戳(DWORD TimeDateStamp)
* 再后八位(第13·14·15·16·17·18·19·20位)是symbol相关信息,不重要
* 最后两位(第21·22位)是扩展头的大小，32位程序是固定值|E0|00|(0x00E0)
