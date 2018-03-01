一、Android中clipChildren属性的用法


二、为了做出这种效果图你能想到的方式是什么呢？用RelativeLayout？还是.......

其实很简单，只要用了这个神奇的属性后这个效果很容易就可以实现，下面是注意点：

1、只需在根节点设置android:clipChildren为false即可，默认为true，注意：一定是在布局文件的根节点设置，否则不起作用

2、可以通过android:layout_gravity控制超出的部分如何显示

3、android:clipChildren的意思：是否限制子View在其范围内，我们将其值设置为false后那么当子控件的高度高于父控件时也会完全显示,而不会被压缩 
布局文件如下：


三、布局

<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:clipChildren="false">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="48dip"
        android:background="#B0C4DE"
        android:orientation="horizontal" 
        android:layout_alignParentBottom="true">

        <ImageView
            android:layout_width="0dip"
            android:layout_height="fill_parent"
            android:layout_weight="1.0"
            android:scaleType="fitCenter"
            android:src="@drawable/ic_launcher" />

        <ImageView
            android:layout_width="0dip"
            android:layout_height="fill_parent"
            android:layout_weight="1.0"
            android:scaleType="fitCenter"
            android:src="@drawable/ic_launcher" />

        <ImageView
            android:layout_width="0dip"
            android:layout_height="70dip"
            android:layout_gravity="bottom"
            android:layout_weight="1.0"
            android:scaleType="fitCenter"
            android:src="@drawable/ic_launcher" />

        <ImageView
            android:layout_width="0dip"
            android:layout_height="fill_parent"
            android:layout_weight="1.0"
            android:scaleType="fitCenter"
            android:src="@drawable/ic_launcher" />

        <ImageView
            android:layout_width="0dip"
            android:layout_height="fill_parent"
            android:layout_weight="1.0"
            android:scaleType="fitCenter"
            android:src="@drawable/ic_launcher" />
    </LinearLayout>

</RelativeLayout>
