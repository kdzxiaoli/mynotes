@Aspect
@Component
@Before
@After

spring.aop.auto= false
spring.aop.proxy-target-class = true  -> cglib  or jdbc dong tai daili

JoinPoint jp 获取拦截的方法的参数


@EnableAopAutoProxy  
