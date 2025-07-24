一個功能強大的網頁版圖片分析比較工具，可以自動分析兩張圖片的品質並提供詳細的比較報告。
✨ 功能特色

🔍 智慧場景偵測: 自動識別白色背景人像場景，並調整評分權重
📊 多維度分析: 分析圖片的清晰度、亮度平衡和對比度
📈 視覺化評分: 直觀的進度條顯示各項評分
🖱️ 簡單易用: 支援點擊上傳和拖拽上傳
📱 響應式設計: 適配各種螢幕尺寸
🚀 純前端: 無需伺服器，所有處理都在瀏覽器中完成

🖼️ 功能展示
主要介面

雙圖片上傳區域，支援預覽
即時分析結果顯示
詳細的比較報告

分析指標

清晰度: 使用拉普拉斯算子和邊緣檢測評估圖片銳利度
亮度平衡: 檢測過度曝光和曝光不足的像素
對比度: 計算亮度標準差評估圖片對比
整體評分: 根據場景類型調整權重的綜合評分

🚀 快速開始
線上使用
直接下載 image-comparison-analyzer-v44.html 檔案，用瀏覽器開啟即可使用。
本地部署

克隆此專案

bashgit clone https://github.com/yourusername/image-comparison-analyzer.git
cd image-comparison-analyzer

開啟檔案

bash# 用瀏覽器開啟 HTML 檔案
open image-comparison-analyzer-v44.html
# 或
python -m http.server 8000  # 啟動本地伺服器

在瀏覽器中訪問 http://localhost:8000

📋 使用說明
基本操作

上傳圖片: 點擊「選擇圖片」按鈕或直接拖拽圖片到上傳區域
預覽圖片: 上傳後會顯示圖片縮圖和檔案名稱
開始分析: 當兩張圖片都上傳後，點擊「分析比較」按鈕
查看結果: 檢視各項評分和詳細的比較報告

評分說明

0-60分: 品質較差，建議重新拍攝或後製處理
60-80分: 品質良好，可能有小幅改善空間
80-100分: 品質優秀，適合使用

場景適應
工具會自動偵測以下場景並調整評分權重：

白色背景人像: 提高亮度權重，適合證件照等場景
一般場景: 平衡的權重分配

🛠️ 技術細節
核心技術

前端: 純 HTML5 + CSS3 + JavaScript
圖片處理: Canvas API
算法:

拉普拉斯算子（銳利度檢測）
Sobel 邊緣檢測
亮度平衡計算
場景分類



瀏覽器支援

Chrome 60+
Firefox 55+
Safari 12+
Edge 79+

檔案結構
image-comparison-analyzer/
├── image-comparison-analyzer-v44.html  # 主要應用檔案
├── README.md                           # 說明文件
└── LICENSE                             # 授權檔案
🔧 自訂設定
調整評分權重
您可以修改 sceneWeights 物件來調整不同場景的評分權重：
javascriptconst sceneWeights = {
    white_portrait: {
        clarity: 0.2,      // 清晰度權重
        brightness: 0.45,  // 亮度權重
        contrast: 0.35     // 對比度權重
    },
    standard: {
        clarity: 0.33,
        brightness: 0.33,
        contrast: 0.34
    }
};
調整閾值參數
可以修改場景偵測和評分計算的參數：

白色背景偵測閾值
邊緣檢測敏感度
曝光評估範圍

📈 版本歷史
v4.4 (最新)

新增詳細的除錯資訊輸出
改善白色背景場景的清晰度計算
優化評分準確性

v4.3

新增智慧場景偵測功能
實作自適應權重調整
改善使用者介面

v4.0

重構分析算法
新增多種評分指標
改善視覺化效果
