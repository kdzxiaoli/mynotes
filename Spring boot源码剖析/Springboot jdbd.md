@EnableTrasactionManagement
@Transacational 默认是运行时异常回滚 其他不回滚

@Transcational(runBackFor=Exception.class)
@NoRollbackFor=NullPointerException.class


调用的方法一定要有注解@Transcational
