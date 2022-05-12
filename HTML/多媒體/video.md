播放影片，相關屬性如下:
- src  檔案的位置(若子元素有source就不需要)
- controls  顯示原生的內建控制器
- autoplay  下載完自動播放
- loop  循環播放
- height  影片高
- width  影片寬
- poster  在播放前會在播放器上顯示的圖片
- preload  網頁一讀取完就開始下載視訊
  - none  不要預讀檔案，按下播放後才開始下載
  - auto  由瀏覽器自動決定(預設值)
  - metadata  預讀後設資料(尺寸、首畫格、持續時間等)，按下播放後才下載其他部分
- muted  播放時是否靜音
- mediagroup  
- crossotigin

用以下方式加入不同的影片格式，以防瀏覽器不支援某格式。
優先播放第一個
```html
<video>
	<source src="**.mp4" type="video/mp4">
	<source src="**.webm" type="video/vp8">
	<source src="**.ogv" type="video/ogg">
</video>

```
