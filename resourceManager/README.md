# 3.资源管理中心
题目：在游戏中，有很多需要使用共享资源来处理的功能，这时候就需要单独管理进程来分配，并且按照请求有序执行资源分配，假设当前系统有X个资源，每个请求携带需要占用Y个资源，占用耗时Z秒
要求：

1) 使用gen_server实现该管理进程
2) 请求资源消息 分配资源 资源不足时 返回失败 耗时结束时释放资源"
3) 取消资源消息 立马释放资源"

# 4.优化资源管理中心
"题目：为了更方便的查看资源使用情况，游戏中往往通过ets进行数据查询 并且将数据存储于dets中方便重启服务器后能载入之前资源情况"
要求:

1) 将当前使用资源情况存在ets和dets中 能实时查询每个请求的处理情况(开启时间 耗时 占用资源)"
2) 管理进程从dets加载上次关闭时资源使用情况

# 5.资源管理中心日志
题目：游戏中每一件事都要进行记录，方便技术和运营查看并分析数据，那么我们需要对该资源管理中心增加日志记录
要求：

1) 每个任务开启/完成/取消，需要写入文件log.txt中
2) 每条日志需要记录发生的时间戳