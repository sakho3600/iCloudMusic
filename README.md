# icloudmusic
> #### 总觉得该说点啥   
+      最近开始学习Flutter 

       但是呢，光看光写点样例呢，总感觉不太稳
       
       《iCloudMusic》是萌新使用 Flutter 开发的一款第三方网易云音乐播放器
> #### 构建项目
+     flutter create 项目名称  
      -t      =>    项目类型 
      --org   =>    bundle identifier
      -i      =>    IOS开发语言  
      -a      =>    Android开发语言
      flutter create -t app --org com.monoka -i swift -a kotlin icloudmusic 
> #### 需要使用的插件
+     cupertino_icons: ^0.1.2
      sqflite: ^1.1.3                        // SQLite数据库
      dio: ^1.0.9                            // http请求
      flushbar: ^1.4.0                       // Tosat提示
      video_player: ^0.6.4                   // 视频播放
      flutter_swiper : ^1.1.6                // swiper插件
> #### 构建页面
+ 欢迎页/引导页   
>     首次开启app，将会会跳转到欢迎页面
>
>     使用video_player完成视频背景widget
>
>     使用Stack层叠布局，将视频作为背景，并循环自动播放
>
>     离开欢迎页面时需要释放播放器资源

+     initialize() - 初始化播放器
      dispose() - 释放播放器资源
      notifyListeners() - 监听播放消息   
      addListener(listener) - 添加监听器   
      removeListener(listener) - 移除监听器  
      pause() - 暂停播放   
      play() - 开始播放   
      position - 播放位置   
      seekTo(moment) - 指定到某个位置播放  
      setLooping(looping) - 是否循环播放   
      setVolume(volume) - 设置音量大小
>     使用flutter_swiper组件完成欢迎页的轮播widget
>     
>     添加注册及登录跳转button      
      