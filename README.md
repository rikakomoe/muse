# YmPlayer
Just a Music Player : )

---

### Description

一个简单的音乐播放器（颜值不高 _ (:з」∠) _），全 CSS/Javascript 完成，需要 Font-Awesome 图标库，无需 jQuery。

### Screenshot

正常形态：

![with no lrc](https://www.imim.pw/usr/uploads/with-no-lrc.jpg)

贴入 LRC 的时候：

![with lrc](https://www.imim.pw/usr/uploads/with-lrc.jpg)

### How to use?

> 引入 ymplayer.css 和 ymplayer.min.js：

```
<link rel="stylesheet" type="text/css" href="ymplayer.css">
<script type="text/javascript" src="ymplayer.min.js"></script>
```

> 构造 HTML DOM：

//如果没有歌词

```
<ymplayer src="mp3 文件地址" name="标识ID，支持 0-9 A-Z a-z _" song="歌曲名" artist="歌手" cover="歌曲专辑封面" loop="是否单曲循环，yes or no"></ymplayer>
```

//如果有歌词

```
<ymplayer src="mp3 文件地址" name="标识ID，支持 0-9 A-Z a-z _" song="歌曲名" artist="歌手" cover="歌曲专辑封面" loop="是否单曲循环，yes or no">
	<lrc>歌词内容</lrc>
</ymplayer>
```

### Argument

```
src    string    歌曲文件的地址，必填
name     string    标识ID，用于在一个页面摆放多个 YmPlayer 时区分，*必须唯一*
song      string     歌曲名
artist       string     歌手
cover      string      专辑封面，或者你喜欢的图片
loop      string       是否开启单曲循环，如果是填写 yes ， 否则填 no，在播放时可以通过播放器按钮改动
```

### Issues

> Q:使用 PJAX 时不加载 YmPlayer 怎么办 _ (:з」∠) _
A:在 PJAX 的 end 事件中，插入 YmPlayer 的 Initer 函数，如：

```
$(document).pjax("end",function(){
	YmplayerIniter();
});
```

### Other

目前处于 Alpha 阶段，在不同的站点上可能出现不同程度的错位，还请自己解决。

欢迎开 issues 报告问题。

### To do

- [ ] 播放进度拖拽控制（目前支持点击控制）
- [ ] 响应式的优化
- [ ] 多音乐播放

### License

遵循 GPL v2 开源。