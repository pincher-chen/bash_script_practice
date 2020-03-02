# 提取文本关键信息
## 数据描述
data文件夹下有85个文本，其文本内容如下：
```
$ head 10gs_docking_min.pdbqt
MODEL 1
REMARK VINA RESULT:      -7.9      0.000      0.000
REMARK  14 active torsions:
REMARK  status: ('A' for Active; 'I' for Inactive)
REMARK    1  A    between atoms: CA_2  and  N_1 
REMARK    2  A    between atoms: CA_2  and  CB_5 
REMARK    3  A    between atoms: CA_2  and  C_3 
REMARK    4  A    between atoms: CB_5  and  CG_6 
REMARK    5  A    between atoms: CG_6  and  CD_7 
REMARK       I    between atoms: CD_7  and  N_10 
```
## 脚本描述
获取data文件夹下每个文件中第二行的打分数（比如10gs：-7.9），然后将文件名和打分值对应，存储到指定文件中result_score.dat:
```
file score
10gs  -7.9
2pcp  -10.4
1xd0  -9.7

.....
```
然后根据打分值进行排序(倒序)，获得结果为：
```
file score
10gs  -7.9
1xd0  -9.7
2pcp  -10.4
.....
```
## 涉及相关命令
- for循环
- grep提取关键词
- awk提取关键词
- sort排序
- 管道
- echo
...
