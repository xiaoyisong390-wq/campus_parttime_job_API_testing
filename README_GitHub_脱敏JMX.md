# 校园兼职系统 API 测试计划

此仓库包含 M1-001 至 M1-037 的 JMeter 测试计划（按用例独立线程组）。原始桌面文件未修改；仓库中的 JMX 已将数据库及有效测试密码替换为 JMeter 属性，避免在仓库中保存明文凭据。

运行前配置以下属性：

- `DB_USERNAME`：测试数据库用户名
- `DB_PASSWORD`：测试数据库密码
- `TEST_PASSWORD`：测试账号的有效密码

命令行运行示例：

```bash
jmeter -n -t "校园兼职系统用户账号模块_M1-001至M1-037_脱敏版.jmx" -JDB_USERNAME=你的数据库用户名 -JDB_PASSWORD=你的数据库密码 -JTEST_PASSWORD=你的测试账号密码
```

请仅在受控测试环境运行；计划中的 JDBC 清理线程组会删除匹配的测试账号数据。
