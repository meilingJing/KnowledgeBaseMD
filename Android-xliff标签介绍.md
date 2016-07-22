# Android-string.xml中使用xliff的用法 # 
## 简介 ##

**xliff:XML Localization Interchange File Format ： XML本地化数据交换格式 **

    <xliff:g>

属性id --可以随便命名

属性值 --举例说明

%n$ms:代表输出的是字符串，n：第几个参数；m:在输出之前放置空格

%n$md:代表输出的是整数，n：第几个参数；m:在输出之前放置空格，也可以设为0m,在输出	  之前放置m个0

%n$mf:代表输出的是浮点数，n：第几个参数；m:控制小数位数，eg:m=2.2时i，输出格式W	  为00.00
	
**简写**	

%d：表示整数；
%f：表示浮点数；
%s：表示字符串

***
## 使用举例 ##

1. 在字符文件中添加以下内容

    `<?xml version="1.0" encoding="utf-8"?>`

	`<resources xmlns:xliff="urn:oasis:names:tc:xliff:document:1.2">` 

2. string.xml文件中使用

	`<string name="test_xliff">小姐今年<xliff:g id="xxx">%1d</xliff:g>岁了，上<xliff:g id="yyy">%2s</xliff:g>年级！</string>`

	加上参数和空格的写法：

	`<string name="test_xliff">小姐今年<xliff:g id="xxx">%1$3d</xliff:g>岁了，上<xliff:g id="yyy">%2$5s</xliff:g>年级！</string>`

3. 代码中设置

	`String test = String.format(getResources().getString(R.string.test_xliff), 7, "二");`

4. 输出

	小姐今年7岁了，上二年级！

	加上参数和空格的输出：

	小姐今年   7岁了，上     二年级！

**注意**

	%1$d表达的意思是整个name=”old”中，第一个整型的替代。如果一个name中有两个需要替换的整型内容，则第二个写为：%2$d，以此类推；具体程序中替换见下面的string型； 