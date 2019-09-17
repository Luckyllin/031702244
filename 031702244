# -*- coding: utf-8 -*-
import re
import json
str1=input()
ty=str1[0]
d={}
reg1="\d!(.*?),"
reg2="1\d{10}"
nam=re.search(reg1,str1)
str1=re.sub(reg1,"",str1)
num=re.search(reg2,str1)
str1=re.sub(reg2,"",str1)
nam=nam.group(0)[2:-1]
num=num.group(0)
d["姓名"]=nam
d["手机"]=num
f=[]
sheng=re.match(".*省",str1)
if sheng!=None:
    f.append(sheng.group(0))
    str1=re.sub(".*省","",str1)
else:
    f.append("")
shi=re.match(".*市",str1)
ls=["北京市","重庆市","天津市","上海市"]
if shi!=None:
    if shi.group(0) in ls:
        sheng1=shi.group(0)
        str1=re.sub(".*市","",str1)
        sheng=sheng1[:-1]
        f.append(sheng)
    f.append(shi.group(0))
else:
    f.append("")
qu=re.search(".*[区|县]",str1)
str1=re.sub(".*[区|县]","",str1)
if qu!=None:
    f.append(qu.group(0))
else:
    f.append("")
zhen=re.search(".*[街道|镇|乡]",str1)
str1=re.sub(".*[街道|镇|乡]","",str1)
if zhen!=None:
    f.append(zhen.group(0))
else:
    f.append("")
if ty=="1":
     xiang=str1[:-1]
     if xiang!=None:
        f.append(xiang)
     else:
        f.append("")
else:
    lu=re.match(".*[路|街|巷]",str1)
    str1=re.sub(".*[路|街|巷]","",str1)
    if lu!=None:
       f.append(lu.group(0))
    else:
       f.append("")
    hao=re.match(".*号",str1)
    str1=re.sub(".*号","",str1)
    if hao!=None:
       f.append(hao.group(0))
    else:
       f.append("")
    xiang=str1[:-1]
    if xiang!=None:
       f.append(xiang)
    else:
       f.append("")
d["地址"]=f
j=json.dumps(d)
print(j)











