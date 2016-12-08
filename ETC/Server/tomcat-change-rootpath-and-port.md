# Change Root Path & Port on Tomcat Server

### default path (index.jsp) on localhost:8080  
```
webapps/ROOT
```

### to change path
insert the **Context** node inside **Host** node like following ex in the conf/server.xml  

```xml
<Host name="localhost"  appBase="webapps" unpackWARs="true" autoDeploy="true">
  <Context path="" docBase="/Users/AllieKim/WebstormProjects/project1" reloadable="true" />
        <Valve className="org.apache.catalina.valves.AccessLogValve" directory="logs"
               prefix="localhost_access_log" suffix=".txt"
               pattern="%h %l %u %t &quot;%r&quot; %s %b" />
</Host>
```

### to change the port 8080 to 8800 (which you want)
change the port of **Connector** node in the conf/server.xml  
```xml
<Connector port="8800" protocol="HTTP/1.1" connectionTimeout="20000" redirectPort="8443" />
```