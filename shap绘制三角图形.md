# shap绘制三角图形 #
- indicator.xml

	代码中的@dimen/dip_xx,表示为dip单位的尺寸（在values/dimens文件夹下）

		<?xml version="1.0" encoding="utf-8"?>
		<layer-list xmlns:android="http://schemas.android.com/apk/res/android">
		    <item
		        android:width="@dimen/dip_100"
		        android:height="@dimen/dip_50"
		        android:top="@dimen/dip_20">
		        <shape>
		            <solid android:color="@color/color_white" />
		        </shape>
		    </item>
		    <item
		        android:width="@dimen/dip_15"
		        android:height="@dimen/dip_15"
		        android:left="@dimen/dip_20"
		        android:top="@dimen/dip_15">
		        <rotate
		            android:fromDegrees="45"
		            android:toDegrees="45">
		            <shape android:shape="rectangle">
		                <solid android:color="@color/color_white" />
		            </shape>
		        </rotate>
		    </item>
		</layer-list>

- 最终生成的效果图：

![](http://i.imgur.com/Mo0BtmH.png)