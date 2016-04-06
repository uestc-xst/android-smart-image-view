Smart Image View for Android
==============================

SmartImageView is a drop-in replacement for Android’s standard ImageView which additionally allows images to be loaded from URLs or the user’s contact address book. Images are cached to memory and to disk for super fast loading.


Features
--------
- Drop-in replacement for ImageView
- Load images from a URL
- Load images from the phone’s contact address book
- Asynchronous loading of images, loading happens outside the UI thread
- Images are cached to memory and to disk for super fast loading
- SmartImage class is easily extendable to load from other sources


Documentation, Features and Examples
------------------------------------
Full details and documentation can be found on the project page here:

<http://loopj.com/android-smart-image-view/><br>
<br>
补充：一般情况下用public void setImageUrl(String url, final Integer fallbackResource, final Integer loadingResource)即可满足需求。<br>
<br>
参数说明：url-请求的网络图片的url地址<br>
----------fallbackResource-从网络请求失败后现实的本地drawable图片<br>
----------loadingResource-刚加载SmartImageView时的本地drawable图片<br>
<br>
使用说明：<br>
- 1.     在布局文件中放置控件：<br>
        <app.myqq.com.myqq.smart.SmartImageView<br>
        android:id="@+id/smartImageView"<br>
        android:layout_width="50dp"<br>
        android:layout_height="50dp"<br>
- 2.    在Activity中设置控件参数<br>
      SmartImageView smartImageView= (SmartImageView) findViewById(R.id.smartImageView);<br>
      //1.请求的URL地址，2.显示请求失败的图片。3.正在请求的图片<br>
      smartImageView.setImageUrl("http://192.168.1.1:8080/users/image1.png", R.drawable.image1, R.drawable.touxiang);<br>
        android:src="@drawable/ic_launcher" />
