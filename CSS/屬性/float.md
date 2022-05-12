浮動，可以做出類似文繞圖的效果，但會無法撐起父層的範圍。
解決方法有:
1. 在浮動物件後建立偽元素，以此撐起邊框。如:`::after{content: ""; display: block; clear: both;}`
2. 在父層框架加入`overflow: auto`屬性值