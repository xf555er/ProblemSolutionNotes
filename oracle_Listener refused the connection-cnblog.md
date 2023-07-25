# 问题详情

在sqldeveloper新建连接时出现以下错误, 只需修改Oracle的SID值即可

```
状态: 失败 -测试失败: Listener refused the connection with the following error:ORA-12505, TNS:listener does not currently know of SID given in connect descriptor
```

<img src="oracle_Listener refused the connection/image-20220909200823234.png" alt="image-20220909200823234" style="zoom:67%;" />	

<br>

# 解决方法

**1.`win + R` 输入`regedit` 打开注册表,找到`HKEY_LOCAL_MACHINE\SOFTWARE\Oracle\KEY_OraDB12Home1`, 查看`ORACLE_SID`的值, 此SID的值为`orcl`**

注意: `KEY_OraDB12Home1`不是固定的, 不同版本的oracle其文件名是不一样的

![image-20220909201801625](https://img2022.cnblogs.com/blog/1779065/202210/1779065-20221009233105453-1585692244.png)	

<br>

**2.在sqldeveloper新建数据库连接界面修改SID的值为orcl, 随后点击测试连接, 状态显示成功**

![image-20220909202052593](https://img2022.cnblogs.com/blog/1779065/202210/1779065-20221009233104596-1330389676.png)	



​	