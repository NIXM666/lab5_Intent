# lab5_Intent
主界面：上面的按钮：使用系统默认浏览器打开网址；下面的按钮：选择使用自创浏览器打开网址。</br>
![](https://github.com/NIXM666/lab5_Intent/blob/master/app/src/main/res/images/1.jpg)</br>
系统默认浏览器</br>
![](https://github.com/NIXM666/lab5_Intent/blob/master/app/src/main/res/images/2.jpg)</br>
弹出选择打开方式,由于系统原因，需要强制弹出选择框，否则还是会使用默认浏览器：</br>
Intent chooser = Intent.createChooser(intent, "选择一个丑的人做的浏览器");</br>
![](https://github.com/NIXM666/lab5_Intent/blob/master/app/src/main/res/images/3.jpg)</br>
使用自创浏览器：要设置Webview的显示属性，否则无法在app内打开网址，仍会使用默认浏览器：</br>
web.setWebViewClient(new WebViewClient(){</br>
    @Override</br>
    public boolean shouldOverrideUrlLoading(WebView view,String url){</br>
        view.loadUrl(url);</br>
        return true;</br>
    }</br>
});    
</br>![](https://github.com/NIXM666/lab5_Intent/blob/master/app/src/main/res/images/4.jpg)</br>
