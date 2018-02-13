# php--Memcache
Memcache(内存，缓存) ： 是一个高性能的分布式的内存对象缓存系统。通过在内存里



		基于libevent事件
	  	Linux下
	  	安装libevent时
			./configure –with-libevent=/usr
			Make && make install
		 安装memcached
			./configure –with-libevent=/usr
		  	Make && make install

		    启动Memcahced –d –m 128 –l 192.168.1.111 –p 11211 –u root
		    停止: kill `cat /tmp/memcached.pid`;
		      	Killall  memcached
		
		
	

         安装Memcache服务器（Linux和Window上分别安装）

          Windows下
			       memcached.exe -d install   :安装Memcach
	           memcached.exe -d uninstall  :卸载 Memcach
             memcached.exe -d start    :启动Memcahced
             netstat -an    查看是否启动成功
             Memcached.exe –d  -m 50(这里的50是指定的内存大小，单位:兆) –l 127.0.0.1(127.0.0.1指定的ip)
             -p 11211(11211指定的端口号) start

Memcached服务器的管理（启动）

		             memcached的基本设置：
                    -p 监听的端口 
                    -l 连接的IP地址, 默认是本机 
                    -d start 启动memcached服务 
                    -d restart 重起memcached服务 
                    -d stop|shutdown 关闭正在运行的memcached服务 
                    -d install 安装memcached服务 
                    -d uninstall 卸载memcached服务 
                    -u 以的身份运行 (仅在以root运行的时候有效) 
                    -m 最大内存使用，单位MB。默认64MB ，最大好像2G
                    -M 内存耗尽时返回错误，而不是删除项 
                    -c 最大同时连接数，默认是1024 
                    -f 块大小增长因子，默认是1.25 
                    -n 最小分配空间，key+value+flags默认是48 
                    -h 显示帮助
                    

                get	取值   (1)变量名
                set	设置值   (1) add 变量名 (2)1  (3)存多少秒 (4)字符串长度 
                add	添加值  例子: (1) add 变量名 (2)1  (3)存多少秒 (4)字符串长度 
                delete  删除值
                flush_all 删除所有值



