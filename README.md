# BKing
## 简介
现代信息检索课程设计，其中包括索引器的设计和TREC比赛

## 任务内容

### Part 1:

基本要求：构建词典和倒排索引
* 实现 Single-pass In-memory Indexing
* 实现倒排索引的 Gamma 编码压缩 / 解压
* 实现词典的单一字符串形式压缩 / 解压，任意数据结构（如哈希表、 B 树等）
* 实现关键字的查找，命令行中 Print 给定关键字的倒排记录表
* 给出以下语料统计量：词项数量，文档数量，词条数量，文档平均长度（词条数量）
* 对停用词去除、词干还原等无要求，但应实现最基本的词条化功能 例如：将所有非字母和非数字字符转换为空格，不考虑纯数字词项

[Test Data](http://gucasir.org/ModernIR/shakespeare-merchant.trec.tgz)
解压命令： `tar zxvf shakespear-merchant.trec.tgz`

### Part 2:

采用类似 TREC 竞赛的形式
* 以小组形式在给定数据上进行实验
* 鼓励创新思维
   – 评分：综合考虑实验结果和使用的新方法、提出的新思路

## 任务设计思路

第一部分是对我们课上学习内容的实现，通过实现任务一，对于加深对课程学习的立即是很有帮助的  
主要涉及:  
1. 词项归一化(选择哪种归一化方法？)与去停用词(哪些是停用词？)和词条化  
2. 字符串压缩与解码  
3. 倒排索引的构建  
4. 语料的读取与分词   
5. 统计分析词项数量与文档数量、文档长度(词条数目)，词条数量  

第二部分是research能力与开发能力并重的，可以使用开源软件提升检索能力，也可以自己实现检索器


## Parser Doc get index file
	`python corpusParser.py -w shakespeare-merchant.trec.1 -s stopword`

	Start......
	dump index from memory to file shakespeare-merchant.trec.1.index.txt
	----------------------------------------------------------
	finish
	----------------------------------------------------------
	Total time analysis:
	1.9920001029968262, 's'
