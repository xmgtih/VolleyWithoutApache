# VolleyWithoutApache

http://developer.android.com/intl/zh-cn/about/versions/marshmallow/android-6.0-changes.html#behavior-apache-http-client

google在android 6.0（(API level 23) ）上删除了apache的http client。这样导致在app中使用http client的地方报错，虽然google也给出了依赖方式。但是考虑到有一些东西是以组件方式存在，如volley就依赖apache（很纳闷，既然google要去除apache的相关东西，那volley应该同时更新一下，可能后面会更新吧）。我们不能指望使用我们组件的也要像google指导的那样，要使用“'org.apache.http.legacy'”方式解决。这里我将volley依赖的apache的一些相关类，从apache中移植到volley中，这样volley就可以不依赖apache的相关的东西了。

