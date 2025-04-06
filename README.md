# username-.github.io
u777
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>選擇技術</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
        }
        img {
            max-width: 100%;
            height: auto;
            margin-top: 20px;
        }
        .info {
            margin-top: 20px;
            font-size: 18px;
        }
        .contact {
            margin-top: 30px;
            font-size: 20px;
            font-weight: bold;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>選擇一種技術</h1>
        <select id="techSelect" onchange="updateContent()">
            <option value="">-- 請選擇 --</option>
            <option value="html">HTML</option>
            <option value="css">CSS</option>
            <option value="js">JavaScript</option>
        </select>
        <div id="content" class="info"></div>
        <img id="techImage" src="" alt="" style="display: none;">
        <div class="contact">聯絡人：洪重發油漆 | 電話：0915189498</div>
    </div>
    
    <script>
        function updateContent() {
            var select = document.getElementById("techSelect");
            var content = document.getElementById("content");
            var image = document.getElementById("techImage");
            var value = select.value;
            
            if (value === "html") {
                content.innerHTML = "HTML（超文本標記語言）用於建立網頁的基本結構。";
                image.src = "https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg";
                image.style.display = "block";
            } else if (value === "css") {
                content.innerHTML = "CSS（層疊樣式表）用於設計和美化網頁的外觀。";
                image.src = "https://upload.wikimedia.org/wikipedia/commons/6/62/CSS3_logo.svg";
                image.style.display = "block";
            } else if (value === "js") {
                content.innerHTML = "JavaScript 是一種用於創建動態交互式網頁的程式語言。";
                image.src = "https://upload.wikimedia.org/wikipedia/commons/6/6a/JavaScript-logo.png";
                image.style.display = "block";
            } else {
                content.innerHTML = "";
                image.style.display = "none";
            }
        }
    </script>
</body>
</html>
