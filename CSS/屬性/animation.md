---
date: 2021-12-31
aliases: []
---
設定動畫
- animation-name: 關鍵影格的名稱
- animation-duration: 完成一次週期的時間
- animation-delay:  元素讀取完畢到動畫開始的間隔時間
- animation-iteration-count: 重複次數，infinite為永遠重複
- animation-timing-function:  動畫漸變的時間函數
- animation-direction:  是否反向播放
- animation-play-state: 播放狀態，有pause與running(預設)
- animation-fill-mode:  元素在沒播放動畫時的狀態
- animation: name duration timing-function delay iteration-count direction fill-mode;

animation: 動畫名稱 播放時間 延遲執行的時間 速度 次數 方向 填充模式 播放狀態


@keyframes 動畫名稱{
                  0%{0%時的樣子}
				50%{50%時的樣子}
			   100%{100%時的樣子}
}