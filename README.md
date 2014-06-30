# Quizr

Quizr is a quiz game, based on the Topeka application of the Polymer project (http://www.polymer-project.org/). It is basically a simple KitKat web view that renders the polymer quiz sample quiz game. This is the code used on https://play.google.com/store/apps/details?id=com.androninja.quizr

## HOW TO:

Under 'mobile' folder, on the MainActivity.java we set the web view to render the quiz game, hosted on GAE:
```
private void setWebView() {
        mWebView = (WebView) findViewById(R.id.activity_main_webview);
        mWebView.setWebChromeClient(new WebChromeClient());
        mWebView.getSettings().setJavaScriptEnabled(true);
        mWebView.getSettings().setDomStorageEnabled(true);
        mWebView.loadUrl("http://quizr-app.appspot.com/static/v1/index.html");
    }
```

The "backend" folder contains a GAE project ready to be deployed, with a static/v1 folder that holds the polymer app. 