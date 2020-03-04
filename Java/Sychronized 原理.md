给一个对象上锁  会分配一个管程Monitor  包裹起来
monitorenter成功 则 执行任务
如果失败则进度管程阻塞队列
monitorexits 通知队列唤醒
