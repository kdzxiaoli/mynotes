spring.mvc.view.prefix=/WEB-INF/
spring.mvc.view.suffix=.jsp

tomcat-embeded-jasper 需要这个依赖才能解析jsp

spring.resources.staticLocations=? //static files route


@WebServlet("/dddd")

@ServlerComponentScan 


@WebFilter

FilterRegistrationBean 

@WebListener 
ServletContextListener  

ServletListenerRegisterationBean get a listener 


ServletRegistrationBean get a servlet extends HttpServlet


拦截器

实现InterceptorHandler 
 extends  WebMvcConfigAdapter  addInterceptor
 
 @ExceptionHandler(value=?)
 
 @ControllerAdvice
 @ResponseBody
 GloblalExceptionHandler {
 
    @ExceotionHandler
 
 }

