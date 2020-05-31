---
layout: post
title: Map遍历几种方法
date: 2020-05-29 22:18:25
tags:
  - Java
---

### 循环遍历Map的几种方式



Java代码 

```
1. Map<String,String> map=**new** HashMap<String,String>(); 
2. map.put("username", "qq"); 
3. map.put("passWord", "123"); 
4. map.put("userID", "1"); 
5. map.put("email", "qq@qq.com"); 
```

<!-- more -->


第一种用for循环

Java代码 

```
1. **for**(Map.Entry<String, String> entry:map.entrySet()){ 
2. System.out.println(entry.getKey()+"--->"+entry.getValue()); 
3. } 
```





第二种用迭代

Java代码

```
1. Set set = map.entrySet();    
2. Iterator i = set.iterator();    
3. **while**(i.hasNext()){  
4. Map.Entry<String, String> entry1=(Map.Entry<String, String>)i.next(); 
5. System.out.println(entry1.getKey()+"=="+entry1.getValue()); 
6. } 
```




用keySet()迭代

Java代码 

```
1. Iterator it=map.keySet().iterator(); 
2. **while**(it.hasNext()){ 
3. String key; 
4. String value; 
5. key=it.next().toString(); 
6. value=map.get(key); 
7. System.out.println(key+"--"+value); 
8. } 
```





用entrySet()迭代

Java代码 

```
1. Iterator it=map.entrySet().iterator();     
2. System.out.println( map.entrySet().size()); 
3. String key;     
4. String value; 
5. **while**(it.hasNext()){ 
6. ​    Map.Entry entry = (Map.Entry)it.next();     
7. ​    key=entry.getKey().toString();     
8. ​    value=entry.getValue().toString();     
9. ​    System.out.println(key+"===="+value);          
10. }   
```

