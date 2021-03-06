# 利用Home Assistant真正打通小米生态链

下载5.0.19版本之前的[米家App](https://mi-home.en.uptodown.com/android/download/1690042)


Android模拟器 http://mumu.163.com/

[利用wireshark插件抓包米家设备miio局域网UDP包](https://v2ex.com/t/625376)

[穷鬼 HomeKit 智能家居踩坑攻略](https://www.v2ex.com/t/523297)

[一些关于智能家居的讨论](https://v2ex.com/t/637183)

[如何评价Home Assistant](https://www.v2ex.com/t/421873)

[入坑 HomeKit，咨询下大家是怎么玩的](https://www.v2ex.com/t/421873)


```
echo "select name,localIP,token from devicerecord;" | sqlite3 ./
```

|名称|IP|token|
|---|---|---|
|插座|192.168.1.141|43d205b33927917138525eff554b92de|
|吸顶灯|192.168.1.150|32230ddd82a31b3aa927613118ddd84e|
|台灯|192.168.1.108|a052116379abaeb0afe0b6f93d780960|
|破壁料理机|192.168.1.124|eae9af7cae6391459f2f86adc5f62e53|
|电磁炉|192.168.1.2|3355f5412d9d4f5177661069b6b3309a|
|扫地机器人|192.168.1.51|30534961356b574f616367596b763539|
|风扇|192.168.1.116|a20f46f2b9aaf31c52fed626ce9ac2d1|
|空调伴侣|192.168.1.232|89a4c6ef592bbbb89ebebcb5e8dc5a1c|
|电饭煲|192.168.1.229|1b1f280fe78cdfcba4ce0a57a80f90b0|


Zigbee 终端设备 -> Zigbee网关 -> tcp/udp -> 自己写的驱动程序 -> 消息队列-> Home Assistant

消息队列一般用**MQTT**，这个已经成物联网事实标准了。


## Aqara

只要在米家App里出现的产品都是可以实现联动的，但是依赖的网关必须连接互联网


[1]: https://github.com/pkozul/ha-floorplan
[2]: https://demo.home-assistant.io/#/lovelace/0
[3]: https://www.google.com/search?q=site:v2ex.com/t%20home+assistant