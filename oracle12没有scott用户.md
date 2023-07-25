# 问题详情

在oracle11上是有scott用户的, 但是在oracle12及以上版本scott用户就被移除了, 只能自己新建一个scott用户

<br>

# 解决方法

**1.创建c##scott用户**

此处创建的用户为`c##scott`, 密码为`tiger`

```sql
create user c##scott identified by tiger
```

<br>

**2.给c##scott用户授权**

```sql
grant connect,resource,unlimited tablespace to c##scott container=all;
```

<br>

**3.设置用户表空间**

```sql
alter user c##scott default tablespace users;  

alter user c##scott temporary tablespace temp;
```

<br>

**4.登录c##scott用户**

```sql
connect c##scott/tige
```

<br>

**5.显示当前登录用户**

```sql
show user;
```

![image-20220909195448278](oracle12没有scott用户/image-20220909195448278.png)	



