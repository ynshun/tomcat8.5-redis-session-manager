tomcat-redis-session-manager 
---




tomcat版本
--------

支持：tomcat8.5.60

下载：https://mirror.bit.edu.cn/apache/tomcat/tomcat-8/v8.5.60/bin/apache-tomcat-8.5.60.zip


用法
---
添加下面的配置到tomcat的context.xml中

    <Valve className="com.kacheap.tomcat.redis.sessions.RedisSessionHandlerValve"/> 
	<Manager className="com.kacheap.tomcat.redis.sessions.RedisSessionManager" 
			  host="172.16.20.140"
			  port="6379"
			  database="0" 
			  password="123456"
			  maxInactiveInterval="60" /> 


---

	<Valve className="com.kacheap.tomcat.redis.sessions.RedisSessionHandlerValve"/> 
	<Manager className="com.kacheap.tomcat.redis.sessions.RedisSessionManager" 
			  host="172.20.201.120"
			  port="6379"
			  database="0" 
			  password="alinewchargedb015P2y2BGPFlENerlJzzKUBc9cDV8xK7"
			  maxInactiveInterval="60" /> 



复制下面的文件到TOMCAT_BASE/lib目录:

- tomcat8.5-redis-session-manager-0.0.1.jar
- jedis-2.5.2.jar
- commons-pool2-2.2.jar

感谢
---
此版本修改自 https://github.com/jcoleman/tomcat-redis-session-manager

