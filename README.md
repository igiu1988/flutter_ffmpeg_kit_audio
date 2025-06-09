# ffmpeg_kit_flutter_audio

### Installation

## 1. 在pubspec中添加依赖
下载 ffmpeg_kit_flutter_audio，把其添加到 `pubspec.yaml file`.
由于ffmpegKit相关的flutter库都无法下载了，所以我都改造为了本地依赖。
对于有时间、有需要的人，可以把它再推到自己的私有maven库中。

```yaml
dependencies:
  ffmpeg_kit_flutter_audio:
    path: /Users/your-dir-path/flutter_ffmpeg_kit_audio
```

## 2. 安卓插件相关
查看 flutter_ffmpeg_kit_audio/android/build.gradle中的依赖可以发现

```
// build.gradle中添加本地 maven 仓库，
// 另外，clone 我的另一个github仓库: my-maven-repo
// 修改下面的路径，把 /Users/wangyang/Projects 替换成你的目录
maven {
    url '/Users/wangyang/Projects/my-maven-repo/maven-repo'
}

// 还有两个依赖
implementation 'com.arthenica:ffmpeg-kit-audio:6.0-2'
implementation 'com.arthenica:smart-exception-java:0.2.1'

```


## 3. iOS插件相关
iOS不用处理，我直接在 flutter_ffmpeg_kit_audio/iOS 中做好了处理