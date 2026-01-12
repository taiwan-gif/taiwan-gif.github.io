<!DOCTYPE html>
<html>
<head>
    <title>资料</title>
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
        （）<br>
        <small></small>
    </div>
<script>
        // 僅顯示模擬訊息，不收集真實資料
        const fakeMessages = [
            "偵測到資料外傳...",
            "嘗試攔截通訊錄... [模擬]",
            "GPS定位記錄: [已屏蔽]",
            "系統漏洞檢測: CVE-XXXX-XXXX [模擬]"
        ];
        
        let index = 0;
        const interval = setInterval(() => {
            if (index < fakeMessages.length) {
                const p = document.createElement('p');
                p.textContent = fakeMessages[index];
                document.getElementById('fakeInfo').appendChild(p);
                index++;
            } else {
                clearInterval(interval);
            }
        }, 1500);
        
        // 僅顯示瀏覽器公開資訊（不涉及隱私）
        console.log('測試存取:');
        console.log('- 使用者代理:', navigator.userAgent);
        console.log('- 螢幕尺寸:', screen.width + 'x' + screen.height);
        console.log('- 語言:', navigator.language);
