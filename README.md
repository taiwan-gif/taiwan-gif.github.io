<!-- 將此程式碼儲存為 index.html -->
<!DOCTYPE html>
<html>
<head>
    <title>安全測試頁面</title>
    <style>
        body {
            background: black;
            color: red;
            font-family: monospace;
            text-align: center;
            padding-top: 100px;
            overflow: hidden;
        }
        .blink {
            animation: blink 1s infinite;
            font-size: 3em;
        }
        @keyframes blink {
            50% { opacity: 0; }
        }
        .info {
            color: yellow;
            margin-top: 50px;
        }
    </style>
</head>
<body>
    <div class="blink">⚠ 警告！裝置安全性遭破壞！</div>
    <div id="fakeInfo"></div>
    <div class="info">
        （此為安全測試模擬
