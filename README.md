![Image text](https://github.com/Jiangzqts/EpubRead/blob/master/img-folder/test1.png);![Image text](https://github.com/Jiangzqts/EpubRead/blob/master/img-folder/test2.png);
![Image text](https://github.com/Jiangzqts/EpubRead/blob/master/img-folder/test3.png);![Image text](https://github.com/Jiangzqts/EpubRead/blob/master/img-folder/test4.png);
Guide:
1. 此项目是个阅读epub的阅读器，直接导入moudle,按照mainactivity调用方法即可实现阅读，可自己定制阅读页面，默认只能读20%，如若想修改可在BookMode类的createTextModel方法中做修改。
2. 自定义的Application一定要继承KooReader项目中的ZLAndroidApplication
3. 需要把KooReaderIntents 里把DEFAULT_PACKAGE 常量改为自己的项目名称：com.xx.xx
缘由：
 我使用Jiangzqts的项目，修改了UI之后，想集成到我工作的项目中，遇到一个恼人的问题，电子书打不开。
 调试后发现是BookCollectionShadow.bindService返回false.
 (然后比较源文件找哪里没有配置好，最后看了FBReader项目集成时需要注意的问题中第三条，第四条)
 KooReaderIntents里面的DEFAULT_PACKAGE等于Jiangzqts/EpubRead的项目名称："com.ma.readerdemo"
 哈哈，因此需要把KooReaderIntents 里把DEFAULT_PACKAGE 常量改为自己的项目名称：com.xx.xx；就可以打开书籍了

作者：一路狂奔mgStupid
链接：https://www.jianshu.com/p/febc1f032ff2
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
Thanks
   1:https://github.com/koreader/koreader  开源项目
   2：其他开发者
