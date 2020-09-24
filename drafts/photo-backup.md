
本地或NAS的照片管理lightroom是很好的选择



### 需求与思考
什么样的图片是需要分享的
什么样的图片是你希望在随时查看的
是那些关于你的，关于你的旅行，你的人生，你的记忆中美好的
你亲手拍下的，你所珍惜的。

所以一些身外之物的照片，截图也好，网上下载的也好，不要放iCloud photos里

### 一些疑问
百度云利用原文件名，定位到本地的原图
EXIF星级，关键字编辑，以实现一定程度的跨平台
lightroom编辑过的图片是否可以作标记？
网上下载的图片是存储在百度云。还是NAS里？
文件夹作为来源管理，标签作为分类管理。
对隐私图片的文件夹设置权限

### 手机拍照
截图定期删除
网上下载的图片定期归档到NAS
拍好的相片，利用碎片时间整理一下，每个月或每周导入mac photo
文档类的可以OCR的，就转成文档的形式存储在Qsync或iCloud Drive

### 相机拍照
导入NAS后，修过的图片有必要再导入iCloud
RAW文件排除后再备份到Google Photo

### 产品对比
QuMagic的人脸识别没有Google Photos和百度云好用

百度云：
2TB空间，

一刻相册
无限空间，100M内视频备份

Google Photos:
无限空间，照片16M内，视频1080P

iCloud:
更好的产品体验和设计
注重隐私
空间小
没有评级


### 方案
备份: NAS，百度云，Google Photos
同步：iCloud，百度云
整理：分组，AI分类，关键字
查询：根据时间命名原文件，根据活动和时间整理文件夹
视频：Google Photos(支持1080P)，NAS

### 工作流
其实存储不是难事，难的是有效的整理，并能让元信息可以在各平台同步。比如说你自己整理的智能收藏夹，既可以在iPhone上查看，也可以在Windows上查看，同时又能不是很麻烦的找到原件（虽然这个不经常）。
lightroom
百度云全量备份，Google Photos作同步备份，同时同步到NAS。
在NAS端进行照片分类，标签，整理，因为那才是带得走，和随时编辑的数据
~~iPhone的图片定期整理归档到mac photos，归档前需要清理下截图什么的~~
iPhone定期整理归档到NAS，进行简单的分类：
- web放网图
- document放一些记录型的文件（后期看能不能转录成文字后存储）
- qsync放一些需要同步的文件类照片(身份证之类的)
~~mac photos不连接iCloud，不然iCloud会存在很多照片。photos library放在NAS上，用作备份。~~

iPhone，iPad开启iCloud同步，iCloud只存放精选的照片。

个人信息类的文档图片放在NAS里独立（不同步到百度云）的文件夹进行，在个人设备间进行共享。

一年内的图片放本地SSD上方便编辑，同时后期完成的图片热备份到NAS。




一年以内的存固态上方便编辑处理，一年前的放 NAS，两个照片库均通过 Lightroom 管理，在 NAS 的另一块硬盘上用 borgbackup 做备份。
拍完以后导入 Lightroom，修完图之后移动到日期的目录下。目前还没做标签，因为太多了（懒）……
在 Adobe 云上存低分辨率照片（智能预览），方便其他同步查看。
挺好的，就是 Lightroom 差不多 600+/年有一点贵，但目前还没找到替代方案。

[1]: https://web.everphoto.cn/
[2]: https://pan.baidu.com
[3]: https://photos.google.com/
[4]: https://support.google.com/photos/answer/6220791?hl=en&ref_topic=6156061
[5]: https://picasa.google.com/
[6]: https://www.zhihu.com/question/316519032/answer/627698452 "摄影师都怎么管理自己的图片？"
[7]: https://www.zhihu.com/question/35583053/answer/137968992 "请教下用lightroom管理照片,硬盘又不够大,怎么存储数据呢, NAS? - 以宁的回答 - 知乎"
[10]: https://v2ex.com/t/657535 "你们都是如何管理自己的照片的？"
[11]: https://www.v2ex.com/t/407080 "关于跨平台备份和浏览照片"
[12]: https://www.youtube.com/watch?v=9E0EDIqREqg
[13]: https://www.youtube.com/watch?v=h-a739LKnro