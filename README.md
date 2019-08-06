# BestPractices
最佳实践
秒杀：解决超卖问题

synchronized
SETNX
redisson

示例环境部署:
NGINX反向代理
**************************************************
下载nginx  并在nginx.conf 修改为如何内容
        location / {
            root   html;
            index  index.html index.htm;
	proxy_pass http://tccluster;
        }
        
        upstream  tccluster  {
                server   localhost:8080 weight=1;
                server   localhost:8090 weight=1;
}
**************************************************
Maven 解决依赖
JMeter 测试并发
