Configuration 配置
SqlSessionFactory session工厂
SqlSession 提供操作数据库的方法
Executor 操作数据库
MappedStatement 输入输出映射
StatementHandler 具体数据库的handler
ResultHandler

mybatis 加载mapper的方式 
4中

class package resource  URL

package 优先级最高


mybatis缓存的作用是 减少对数据库的依赖 提高操作速度
一级缓存默认是开启的  一级缓存的作用域在SqlSession里

二级缓存 是跨SqlSession的


CacheKey 类
