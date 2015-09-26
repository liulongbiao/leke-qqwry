# leke-qqwry

leke-qqwry 是一个纯真IP地址库(`qqwry.dat`)数据读取类库。

使用方式：

```java
ClassPathResource datFile = new ClassPathResource("data/qqwry.dat");
IPv4LocatorFactoryBean fb = new IPv4LocatorFactoryBean();
fb.setDatFile(datFile);
fb.afterPropertiesSet();
IPv4Locator locator = fb.getObject();

IPv4Loc loc = locator.locate("39.184.174.243");
System.out.println(loc); // 浙江省 移动
```