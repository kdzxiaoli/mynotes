SPI  Services provider interaface

要求在classpath下 META-INF/services/包名 -内容 接口实现类     
要求实现类必须有默认构造函数  

```java
//保存接口 和当前类的加载器
//清楚缓存然后懒加载
ServiceLoader<IDocParse> serviceLoader = ServiceLoader.load(IDocParser.class);  
Iterator<IDocParser> iter = serviceLoader.iterator();  
while(iter.hasNext()) {
    iter.next().parser();
}
```



优点  解耦合 灵活调整实现类

Class.forName("com.mysql.jdbc.Driver") 底层就是用SPI实现的    触发初始化


ClassLoader cl = Thread.currentThread().getContextClassLoader();
打破双亲委派模型
