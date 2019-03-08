# Learning-Summary
学习总结

# Linux
```
head, tail </br>
head -10000 raw_file > file </br>
合并文件：cat file1 file2 > file </br>
grep 要查找的 file </br>
统计行数：wc -l fiel </br> 

sed [-nefri] 'command' 输入文本   
常用选项：
        -n∶使用安静(silent)模式。在一般 sed 的用法中，所有来自 STDIN的资料一般都会被列出到萤幕上。但如果加上 -n 参数后，则只有经过sed 特殊处理的那一行(或者动作)才会被列出来。
        -e∶直接在指令列模式上进行 sed 的动作编辑；
        -f∶直接将 sed 的动作写在一个档案内， -f filename 则可以执行 filename 内的sed 动作；
        -r∶sed 的动作支援的是延伸型正规表示法的语法。(预设是基础正规表示法语法)
        -i∶直接修改读取的档案内容，而不是由萤幕输出。       

常用命令：
        a   ∶新增， a 的后面可以接字串，而这些字串会在新的一行出现(目前的下一行)～
        c   ∶取代， c 的后面可以接字串，这些字串可以取代 n1,n2 之间的行！
        d   ∶删除，因为是删除啊，所以 d 后面通常不接任何咚咚；
         i   ∶插入， i 的后面可以接字串，而这些字串会在新的一行出现(目前的上一行)；
         p  ∶列印，亦即将某个选择的资料印出。通常 p 会与参数 sed -n 一起运作～
         s  ∶取代，可以直接进行取代的工作哩！通常这个 s 的动作可以搭配正规表示法！例如 1,20s/old/new/g 就是啦！

awk
提取列
awk  -F ':'  '{print $1"\t"$7}
```

# Python
## pandas
```python
df = pandas.read_csv(,usecols=[], nrow=5, dtype={}, low_memory=False)
```

## csv
```python
import csv
with open(self._path, encoding="utf-8", errors='ignore') as fi:
    reader = csv.DictReader(fi)
    for row in reader:
        print(row['asdd'])
    
```
## Re
```python
只保留中文，数字，字母
\u4e00-\u9fa5   汉字的unicode范围
\u0030-\u0039	数字的unicode范围
\u0041-\u005a	大写字母unicode范围
\u0061-\u007a	小写字母unicode范围

pattern = u"([^\u4e00-\u9fa5\u0030-\u0039\u0041-\u005a\u0061-\u007a])"
line = re.sub(pattern, "", line)
```

