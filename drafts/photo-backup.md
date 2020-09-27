
### 需求与思考
什么样的图片是需要分享的
什么样的图片是你希望在随时查看的
是那些关于你的，关于你的旅行，你的人生，你的记忆中美好的
你亲手拍下的，你所珍惜的。
所以一些身外之物的照片，截图也好，网上下载的也好，不要放iCloud photos里

其实存储不是难事，难的是有效的整理，并能让元信息可以在各平台同步。
比如说你自己整理的智能收藏夹，既可以在iPhone上查看，也可以在Windows上查看，同时又能不是很麻烦的找到原件（虽然这个不经常）。
目前来看

### 一些疑问
百度云利用原文件名，定位到本地的原图
EXIF星级，关键字编辑，以实现一定程度的跨平台
lightroom编辑过的图片是否可以作标记？
网上下载的图片是存储在百度云。还是NAS里？
文件夹作为来源管理，标签作为分类管理。
对隐私图片的文件夹设置权限
mac finder支持iptc关键字检索
Q: Will tags of image files embedded in IPTC being reconized by iCloud Photos? 
A: Yes
Q: Will keywords of icloud photos stored in IPTC? 
A: No, but you can choose to export original with xml, or compressed jpeg with IPTC
Q: how to use digikam RAW import tool?
A:
A: Will google photos keep metadata when upload?
A: Yes but no, when download it you can see same metadata, but cannot used for search in google photos


### 产品对比
QuMagie
人脸识别没有Google Photos和百度云好用
对jpeg的评级并没有同步到文件内的元信息（将文件评级后下载到原文件，之后再上传，jpeg评级并没有显示在里面）
不支持HEIC的缩略图

百度云：
2TB空间，

一刻相册
无限空间，100M内视频备份

Google Photos:
无限空间，照片16MP内，视频1080P

iCloud:
更好的产品体验和设计
注重隐私
空间小
没有评级
不支持标签IPTC关键字，但可以建立智能文件夹包含对应关键字，对相应的文件夹进行检索
但你只能在mac photos上建立智能文件夹，网页版的iCloud也不行

digikam[15]:
直接读写photo的metadata
支持removable image library
支持database的导出，但因为性能原因，不支持nfs。最好放ssd上
实验性的mysql实现，支持nfs，和100000+图片更好的性能表现[16]


### 方案
备份: NAS，百度云，Google Photos
同步：iCloud
整理：评级，分组，AI分类，关键字
查询：根据时间命名原文件，根据活动和时间整理文件夹
视频：Google Photos(支持1080P)，NAS

### 工作流
在NAS端进行照片分类，标签，整理，因为那才是带得走，和随时编辑的数据
加入定时任务，百度云全量备份，RAW文件排除后再备份到Google Photo，[详情](#user-content-备份到百度云)
digikam整理图片，并将sqlite数据库定期同步到NAS
digikam图库同步到百度云,
digikam里标签为icloud的图片，同步到icloud(不确定标签会不会同步)
利用云的人工智能进行检索定位，通过拍摄时间定位照片
定期对没打标签的根目录图片（一般是手机来的）打上标签
#### 手机拍照
截图定期删除
图片定期归档到NAS的图片根目录
文档类的可以OCR的，就转成文档的形式存储在Qsync或iCloud Drive

~~iPhone的图片定期整理归档到mac photos，归档前需要清理下截图什么的~~
~~mac photos不连接iCloud，不然iCloud会存在很多照片。photos library放在NAS上，用作备份。~~
digkam可以mac windows双平台，所以不需要mac photos

iPhone定期整理归档到NAS，进行简单的分类，打标签：
- web放网图
- document放一些记录型的文件（后期看能不能转录成文字后存储）
- Qsync放一些需要同步的文件类照片(身份证之类的)

iPhone，iPad开启iCloud同步，iCloud只存放精选的照片。

#### 相机拍照
放入文件夹文件夹全名：日期-活动-客户(可选)
对于没有定位信息的图片，可以通过相同时间的有定位的手机图片，来添加定位。
加入评级，给精选的照片
在本地SSD上处理照片，后期过的照片存在原地同名保存，加入edited标签
精选的照片加入iCloud标签，导入iCloud
处理完成后转移到NAS归档

虽然云存储(icloud, google photos)大多不支持通过IPTC的关键字检索，
但通时间和地点，基本满足浏览的需求了
就是一些在常住地方的活动，有必要加入关键字，比如说装修，婚礼


### 备份到百度云
[19]: https://support.google.com/photos/answer/9316089 "Photos & Drive不再同步"
[20]: https://nascompares.com/answer/google-photos-sync-with-qnap-nas/ "利用"



[1]: https://web.everphoto.cn/
[2]: https://pan.baidu.com
[3]: https://photos.google.com/
[4]: https://support.google.com/photos/answer/6220791?hl=en&ref_topic=6156061 "Google Photos的上传尺寸限制" 
[4.1]: https://support.google.com/photos/answer/6193313?co=GENIE.Platform%3DDesktop&hl=en "Google Photos 支持的文件格式"
[5]: https://picasa.google.com/
[6]: https://www.zhihu.com/question/316519032/answer/627698452 "摄影师都怎么管理自己的图片？"
[7]: https://www.zhihu.com/question/35583053/answer/137968992 "请教下用lightroom管理照片,硬盘又不够大,怎么存储数据呢, NAS? - 以宁的回答 - 知乎"
[10]: https://v2ex.com/t/657535 "你们都是如何管理自己的照片的？"
[11]: https://www.v2ex.com/t/407080 "关于跨平台备份和浏览照片"
[12]: https://www.youtube.com/watch?v=9E0EDIqREqg
[13]: https://www.youtube.com/watch?v=h-a739LKnro
[14]: https://www.youtube.com/watch?v=h-a739LKnro
[15]: https://invent.kde.org/graphics/digikam
[16]: https://docs.kde.org/trunk5/en/extragear-graphics/digikam/using-setup.html#using-setup-database
[17]: https://www.youtube.com/watch?v=Lr826lxVfWk "完整的拍摄，整理，后期工作流示例"
[18]: https://stackoverflow.com/questions/9542359/does-png-contain-exif-data-like-jpg