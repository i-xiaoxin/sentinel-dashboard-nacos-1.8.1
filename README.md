# sentinel-dashboard-nacos-1.8.1

sentinel-dashboard-nacos持久化

# application.properties

#spring settings
spring.http.encoding.force=true
spring.http.encoding.charset=UTF-8
spring.http.encoding.enabled=true

#cookie name setting
server.servlet.session.cookie.name=sentinel_dashboard_cookie

#logging settings
logging.level.root=info
logging.file=${user.home}/logs/sentinel/sentinel-dashboard.log
logging.pattern.file= %d{yyyy-MM-dd HH:mm:ss} [%thread] %-5level %logger{36} - %msg%n
#logging.pattern.console= %d{yyyy-MM-dd HH:mm:ss} [%thread] %-5level %logger{36} - %msg%n

#auth settings
auth.filter.exclude-urls=/,/auth/login,/auth/logout,/registry/machine,/version
auth.filter.exclude-url-suffixes=htm,html,js,css,map,ico,ttf,woff,png

#If auth.enabled=false, Sentinel console disable login

auth.username=sentinel
auth.password=sentinel

#Inject the dashboard version. It's required to enable

#filtering in pom.xml for this resource file.

sentinel.dashboard.version=1.8.1
#nacos settings  修改此处nacos地址ip即可启动使用
nacos.address=192.168.204.129:8848
nacos.namespace=sentinel
