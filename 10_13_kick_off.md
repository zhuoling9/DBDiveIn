
1. sqlite 源码：https://github.com/sqlite/sqlite/tree/master
2. wcdb 源码：https://github.com/Tencent/wcdb


SQLite 源码学习计划
        
模块1：SQLite核心架构 @华亚楠

Week 1-2: SQLite总体结构与启动流程 

•任务：了解SQLite的代码结构，分析main.c中的主函数，理解SQLite是如何初始化并启动的。
•目标：能够讲解SQLite如何从接收到SQL命令到执行流程的整体过程。

Week 3-4: SQL解析与语法树生成 

•任务：深入阅读parse.y文件，了解Yacc生成SQL语法解析器的过程，分析抽象语法树的构造。
•目标：理解SQL解析的详细过程，能够手动调试解析部分代码。

Week 5-6: 虚拟数据库引擎（VDBE）

•任务：阅读vdbe.c，分析VDBE的工作原理，特别是如何将SQL解析结果转化为VDBE的操作码。
•目标：了解SQLite的执行引擎并能解释VDBE如何执行SQL语句。

模块2：SQLite存储引擎 @韩卓伶

Week 7-8: B-Tree结构及其操作

•任务：学习btree.c，研究SQLite的B-Tree数据结构，理解它如何进行数据的增删改查。
•目标：掌握B-Tree的操作逻辑，能够跟踪调试B-Tree相关操作。

Week 9-10: 分页系统与数据存储

•任务：阅读pager.c，理解分页系统如何管理磁盘上的数据块，以及页面缓存机制。
•目标：掌握分页系统的工作原理，能够在调试时分析页面读取和写入过程。

Week 11-12: 操作系统接口（文件I/O）

•任务：研究os_unix.c，分析SQLite如何通过操作系统接口进行文件读写。
•目标：理解SQLite如何实现跨平台文件I/O，能够调试与文件操作相关的代码。

模块3：事务与并发控制 @杨英琦

Week 13-14: 事务管理与回滚日志

•任务：阅读pager.c和journal.c，分析事务的开启、提交、回滚流程。
•目标：理解SQLite事务的实现原理，掌握回滚日志的作用与机制。

Week 15-16: 并发控制与锁机制

•任务：深入分析sqlite3_mutex.c的锁机制，实现SQLite并发访问的控制。
•目标：理解并发控制的基本方法，并能调试与事务锁相关的功能。

Week 17-18: WAL日志与数据恢复

•任务：学习wal.c文件，分析WAL日志的工作原理和性能优化手段。
•目标：掌握WAL机制的实现细节，理解如何通过WAL实现高效的数据同步。

模块4：全文检索（FTS）@刘文博

Week 19-20: FTS模块结构

•任务：阅读fts3.c和fts5.c，分析全文检索模块的结构和工作原理。
•目标：理解FTS如何通过倒排索引实现高效的全文检索。

Week 21-22: 分词器与搜索优化

•任务：研究分词器的实现细节，特别是tokenizer接口。
•目标：掌握自定义分词器的工作原理，能够通过调试理解分词的执行过程。

模块5：SQLite加密（SQLCipher）@LPY

Week 23-24: SQLCipher加密机制

•任务：阅读SQLCipher的补丁代码，理解如何在SQLite中集成加密功能。
•目标：掌握SQLCipher如何加密数据库文件，以及如何进行密钥管理。
