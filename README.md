# http_server

make

./server

./server [-p port] [-l LOGWrite] [-m TRIGMode] [-o OPT_LINGER] [-s sql_num] [-t thread_num] [-c close_log] [-a actor_model]


    -p，自定义端口号
        默认9006
    -l，选择日志写入方式，默认同步写入
        0，同步写入
        1，异步写入
    -m，listenfd和connfd的模式组合，默认使用LT + LT
        0，表示使用LT + LT
        1，表示使用LT + ET
        2，表示使用ET + LT
        3，表示使用ET + ET
    -o，优雅关闭连接，默认不使用
        0，不使用
        1，使用
    -s，数据库连接数量
        默认为8
    -t，线程数量
        默认为8
    -c，关闭日志，默认打开
        0，打开日志
        1，关闭日志
    -a，选择反应堆模型，默认Proactor
        0，Proactor模型
        1，Reactor模型
