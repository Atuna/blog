
微信备份是否可以无缝迁移到另一台电脑上?



ls -alh ~/Library/Containers/com.tencent.xinWeChat/Data/Library/Application\ Support/com.tencent.xinWeChat/*/*/Message/*.db

将Backup文件夹放入
~/Library/Containers/com.tencent.xinWeChat/Data/Library/Application Support/com.tencent.xinWeChat/
注意，不同时间段同账户与会话的备份文件夹是同名的，所以会相互覆盖，所以还原时一次只能还原一次

土办法导出 Mac 版微信聊天记录[3]
0x600000ea6d00: 0xd1 0x84 0x3e 0x1d 0xc2 0xd2 0x46 0xaa
0x600000ea6d08: 0x9a 0xfe 0x6c 0xfb 0x27 0x7c 0x17 0xa1
0x600000ea6d10: 0x76 0x2b 0xcd 0x7a 0x09 0xee 0x48 0x43
0x600000ea6d18: 0xa2 0xa9 0x5f 0x9d 0x39 0xac 0xd1 0x9b

d1843e1dc2d246aa9afe6cfb277c17a1762bcd7a09ee4843a2a95f9d39acd19b

[1]: https://zhuanlan.zhihu.com/p/60802321
[2]: http://ask.zol.com.cn/x/4739948.html
[3]: https://v2ex.com/t/466053 
[4]: http://xferris.cn/dao-chu-wei-xin-bei-fen-de-mac/
[5]: https://github.com/wongjohn/wechat-analyser "从iTunes备份查看微信聊天记录"
[6]: https://github.com/tsycnh/WeChatExporter "另一个从iTunes备份查看微信聊天记录，但好像更麻烦"
[7]: https://github.com/wongjohn/wechat-analyser "从iTunes备份查看微信聊天记录, C#版"
[8]: https://medium.com/@anluoridge/记录-微信备份工具和原理-b6b504c88217