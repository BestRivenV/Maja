<p align="center" >
<img src="https://upload-images.jianshu.io/upload_images/2523674-1ad917d7d89c9625.png">
</p>

# Maja
Maja 是一款在Mac OS上运行的代码混淆工具，针对iOS应用机审4.3被拒。为了过机审，我会做下面这些处理：
1. 修改项目名
2. 修改类名前缀（.h .m）
3. 修改项目里的文件夹名
4. 打乱项目里的文件结构，可新增或删除一些文件夹，拖动文件至其他文件夹下
5. 压缩项目里的图片资源，目的是改变其编码
6. 修改图片名
7. 代码混淆 

以上是对项目的改动，除此之外还有提审信息、账号证书等改动大家可以在网上查到，在此不再赘述。Maja提供以上1、2、3、5、6、7的功能。

## 使用介绍
直接下载Maja.dmg安装运行

## 注意
- 修改类名前缀，如果没有原类名前缀，就填XX，不要空着，空着就不会执行此修改了。
- 代码混淆，混淆会在填入的项目路径下生成ignoreKey.txt、system_identifiers.txt、user_identifiers.txt、confuse_log.log、XXXXTimeString.h等文件。XXXXTimeString.h为混淆文件，请自行改名后导入到工程中，并在预编译.pch文件中引用此文件，其他可删除。
- 垃圾代码，如果添加的垃圾代码是随机字符构成的会被认为是混淆代码而悲剧，垃圾代码的方法没被调用会被机审过滤掉，不知道是不是真的，如果你有垃圾代码可先导入到工程中然后用本工具混淆。
- 补充，代码里不要包含任何“代码混淆、加密、CodeMix、CodeConfuse...”等中英文字段

## 最后
理论上只要你肯改就能过审，提上去的包里无非是代码和资源。以上的处理会改掉一些马甲包4.3的特征，或者说不让苹果100%认定Which is considered a form of spam，不过现在是宁可错杀不放一个。人审也会给4.3，注意区分，最后祝大家早日过包:)

>Guideline 4.3 - Design(人审)  
We noticed that your app provides the same feature set as other apps submitted to the App Store; it simply varies in content or language, which is considered a form of spam.  

>Guideline 4.3 - Design(机审)  
This app duplicates the content and functionality of other apps submitted by you or another developer to the App Store, which is considered a form of spam.
