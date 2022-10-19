### 部署之后找不到文件的问题
SOA课的实验中，Tomcat部署并完成工件修复之后，按照一般的访问方式居然找不到资源：
```
http://localhost:8080/services
```
后来阴差阳错在service前添加了工件所在的路径，才完成了部署
```
http://localhost:8080/axisTest_war_exploded/services
```
产生此问题的原因是什么仍未可知