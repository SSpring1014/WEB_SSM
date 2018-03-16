# WEB_SSM
springmvc初步调试

****************************************************
SpringMVC中JSP取不到ModelAndView的数据的解决方案：
****************************************************
利用 jstl 去获取 ModelAndView 传入的值时--有时得不到传入的值${itemsList};
--原因：
用maven自动生成的web.xml文件 如下：
-----------------------------------------------------------------------------------------------
[html] view plain copy
<!DOCTYPE web-app PUBLIC  
"-//Sun Microsystems, Inc.//DTD Web Application 2.3//EN"  
"http://java.sun.com/dtd/web-app_2_3.dtd" >  
  
<web-app>  
  
</web-app>  
-----------------------------------------------------------------------------------------------
但这样的文件不行，需要改成
-----------------------------------------------------------------------------------------------
[html] view plain copy
<?xml version="1.0" encoding="UTF-8"?>  
  
<web-app version="2.5"  
xmlns="http://java.sun.com/xml/ns/javaee"  
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  
xsi:schemaLocation="http://java.sun.com/xml/ns/javaee  
http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd">  
</web-app>  
-----------------------------------------------------------------------------------------------
