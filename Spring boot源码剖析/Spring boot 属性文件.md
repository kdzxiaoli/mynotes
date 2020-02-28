# 获取配置文件的方式
## 1
ConfigrableApplicationContext context = SpringbootApplication.run(App.class, args);  
context.getEnviroment().getProperty('name');  
context.close();


## 2

@Autowired
Enviroment enviroment;


## 3
@Value("${dddddd}")

## 4 属性文件里引用
name = jack  
value = test ${name}  

## 5 默认值
@Value("${port:9999}")


## 6 属性文件的位置  
默认文件名application.properties  
在classpath   
在 classpath/config  
如果改名  可以：    
-spring-config.name=?  
--spring-config.location=classpath:/config/app.properties  

## 7  above class annotation
@PropertySource("classpath:jdbc.properties")  tip: 1...n  
@PropertySources({...})  


## 8  prefix
@ConfigrationProperties(prefix="ds")  
or  
@ConfigrationProperties(prefix="ds", location="classpath:app.properties")  

## 9  注入集合
host[0]=1  
host[1]=1  >> List or array  

## 10 动态使用配置文件
这个类要在META-INFO/spring.factories文件里注册  
@Component  
implements EnviromentPostProcessor {  
  Properties source = new Properties();  
  source.load(input);  
  PropertiesPropertySource pps = new PropertiesPropertySource("my", source);  
  enviroment.getPropertySources().addLast(pps);  
}

##  11 区别环境
application-dev or application.prod.properties  
ConfigrableApplicationContext context = SpringbootApplication.run(App.class, args);   
context.setAdditonalProfiles("dev")     

--spring.profiles.active=test    

### @Profile("dev")
could be used in method or class



