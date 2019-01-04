# Learning-Summary
学习总结

# Linux
head, tail </br>
head -10000 > file </br>
合并文件：cat file1 file2 > file </br>
grep 要查找的 file </br>
统计行数：wc -l fiel </br> 

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

