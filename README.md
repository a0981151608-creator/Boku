<!DOCTYPE html> <html lang="zh-TW"> <head>
    <meta charset="UTF-8"> <title>鬼崎源 Onizaki moto</title> 
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Yuji+Boku&display=swap" rel="stylesheet">
    <style>
    
        body {
            font-family: "Yuji Boku", "Microsoft JhengHei", sans-serif; /* 設定字體 */
            background-color:#003D79; /* 背景顏色 */
            margin: 0;
            font-size: 18px;
            padding: 20px;
            text-align: center; /* 讓內容置中 */
        }
        
        .container {
            background-color:#ACD6FF;
            width: 80%;
            margin: 0 auto; /* 區塊置中 */
            padding: 20px;
            border-radius: 10px; /* 圓角效果 */
            box-shadow: 0 0 10px rgba(0,0,0,0.1); /* 陰影效果 */
        }

        h1 {
            color:#000000; /* 標題顏色 */
        }
        h2{
            color:#000000;
        }
        p {
            color:#3C3C3C;
            line-height: 1.6; /* 行高，讓閱讀舒適點 */
            font-size: 24px;
        }

        .btn {
            display: inline-block;
            background-color: #3498db;
            color: white;
            padding: 10px 20px;
            text-decoration: none; /* 去除連結底線 */
            border-radius: 5px;
            margin-top: 10px;
        }
        
        .btn:hover {
            background-color: #2980b9; /* 滑鼠滑過去變深色 */
        }
    </style>
</head>

<body>
    <style>
    /* ...保留之前的 CSS... */
    
    /* 新增圖片樣式 */
    .profile-img {
        width: 150px;       /* 限制寬度，不然圖片會太大 */
        height: 150px;      /* 高度設定一樣 */
        object-fit: cover;  /* 保持比例裁切，不會變形 */
        border-radius: 50%; /* 讓圖片變成圓形 */
        border: 5px solid white; /* 加個白框 */
        box-shadow: 0 0 15px rgba(0,0,0,0.2); /* 讓照片有浮起來的陰影 */
        margin-bottom: 20px; /* 跟下面的標題保持距離 */
    }
        
    .gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between; /* 左右分散對齊 */
    gap: 20px; /* 每個作品之間的間距 */
        }

/* 新增：作品小相框 (用來包住圖片+文字) */
    .artwork-item {
    width: 48%; /* 每個相框佔 48% 寬度 (兩欄式) */
    display: flex;
    flex-direction: column; /* 讓裡面的圖片跟文字「垂直」排列 */
    align-items: center;    /* 讓內容水平置中 */
    margin-bottom: 20px;
    }

/* 修改：圖片設定 */
    .artwork {
    width: 100%;        /* 圖片寬度佔滿小相框 */
    height: auto;       /* 高度自動 */
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

/* 新增：Holder 文字連結設定 */
    .holder-link {
    display: block;       /* 讓它變成區塊元素 */
    margin-top: 10px;     /* 跟圖片留點距離 */
    font-size: 18px;      /* 字體加大 (原本預設約 16px) */
    font-weight: bold;    /* 加粗體比較明顯 */
    color:#0000C6;       /* 連結顏色 */
    text-decoration: none;/* 去除底線 */
    text-align: center;   /* 文字置中 */
    }

    .holder-link:hover {
    color:#AE0000;       /* 滑鼠移過去變色 */
    text-decoration: underline;
    }
    
    .social-links {
    display: flex;
    justify-content: center; /* 水平置中 */
    gap: 20px;               /*圖示之間的距離 */
    margin-top: 20px;        /* 跟上方文字保持距離 */
    margin-bottom: 30px;     /* 跟下方邊界保持距離 */
    }
    
    .social-character{
    display: block;       /* 讓它變成區塊元素 */
    margin-top: 10px;     /* 跟圖片留點距離 */
    font-size: 18px;      /* 字體加大 (原本預設約 16px) */
    font-weight: bold;    /* 加粗體比較明顯 */
    text-decoration: none;/* 去除底線 */
    text-align: center; 
        
    }

/* 社群圖示的基本設定 */
    .social-icon {
    width: 80px;            /* 設定圖示大小，可以自己改 */
    height: 80px;
    border-radius: 50px;
    object-fit: contain;    /* 保持圖片比例 */
    transition: transform 0.3s ease; /* 關鍵！設定動畫時間 0.3秒 */
    }

/* 滑鼠移上去 (Hover) 的效果 */
    .social-icon:hover {
    transform: scale(0.9);  /* 縮小為原本的 0.9 倍 (如果要放大改成 1.1) */
    opacity: 0.8;           /* 順便讓顏色稍微變淡一點點，增加互動感 */
    }
        /* --- Linktree 風格按鈕區 --- */

/* 外層容器：控制按鈕不要太寬，並且置中 */
    .link-group {
    max-width: 600px;   /* 限制最大寬度，才不會電腦版變超長 */
    margin: 0 auto;     /* 讓整個區塊水平置中 */
    display: flex;
    flex-direction: column; /* 讓按鈕一個接一個垂直排列 */
    gap: 15px;          /* 按鈕之間的距離 */
    margin-bottom: 30px; /* 跟下方內容保持距離 */
    }

/* 按鈕本體 */
    .pill-btn {
    display: flex;          /* 彈性盒子：讓圖示跟文字並排 */
    height: 40px;
    align-items: center;    /* 垂直置中 */
    padding: 15px 25px;     /* 內距：讓按鈕胖一點比較好看 */
    
    border: 2px solid #888; /* 邊框顏色 (灰色) */
    border-radius: 50px;    /* 關鍵！讓四角變成圓弧形 (膠囊狀) */
    
    text-decoration: none;  /* 去除超連結底線 */
    color: #333;            /* 文字顏色 */
    font-weight: bold;      /* 粗體 */
    font-size: 25px;
    background: linear-gradient(135deg,#005AB5,	#4EFEB3); /* 背景色 */
    
    transition: transform 0.2s ease, background-color 0.2s; /* 動畫設定 */
    }

/* 滑鼠移上去的效果 (Hover) */
    .pill-btn:hover {
    transform: scale(0.95);     /* 縮小為 0.95 倍 */
    background-color: #f9f9f9;  /* 背景稍微變深一點點 */
    border-color: #333;         /* 邊框變深色 */
    }

/* 按鈕裡面的小圖示 */
    .btn-icon-img {
    width: 30px;        /* 圖示大小 */
    height: 30px;
    margin-right: 15px; /* 圖示跟文字的距離 */
    }

/* 讓文字在視覺上更置中 (選用) */
    .btn-text {
    flex-grow: 1;       /* 佔據剩餘空間 */
    text-align: center; /* 文字置中 */
    padding-right: 24px;/* 因為左邊有圖示，右邊補一個 padding 平衡一下視覺 */
    }
</style>

<body>

    <div class="container">
        
        <img src="https://github.com/a0981151608-creator/Boku/blob/main/assets/images/9-24_da52fcc8de41dd63bf1f282297da9453.jpg?raw=true" 
             alt="邱惠君的大頭貼" 
             class="profile-img">
        
        <h1>はじめまして 我是鬼崎源</h1>
        
        <p>主設是狼+龍，喜歡音樂、畫畫還有自學點程式跟玩遊戲w</p>
        <h3>關於我</h3>
        <p>目前就讀嘉義大學，正在籌備畢業論文。</p>
        <p>歡迎認識!</p>
        <div class="social-links">
    
            <a href="https://x.com/gos88741776" target="_blank">
                <img src="https://pbs.twimg.com/profile_images/1955359038532653056/OSHY3ewP.jpg" 
                alt="X (Twitter)" 
                class="social-icon">
            </a>

            <a href="https://www.facebook.com/gui.qi.yuan?locale=zh_TW" target="_blank">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR43HQpKFjAd-Ka_tLRdM37RKIsJMpEmh7Wgw&s" 
                alt="Facebook" 
                class="social-icon">
            </a>

            <a href="https://www.instagram.com/q_huijun/" target="_blank">
                <img src="https://github.com/a0981151608-creator/Boku/blob/main/assets/images/121.jpg?raw=true" 
                alt="Instagram" 
                class="social-icon">
            </a>

        </div>
        <div class="link-group">

        <a href="mailto:a0981151608@gmail.com" class="pill-btn">
            <img src="https://github.com/a0981151608-creator/Boku/blob/main/assets/images/lance_6438219.png?raw=true" class="btn-icon-img" alt="Mail Icon">
            <span class="btn-text">Commission(籌備中)</span>
        </a>

        <a href="#gallery" class="pill-btn">
            <img src="https://github.com/a0981151608-creator/Boku/blob/main/assets/images/paper_14540421.png?raw=true" class="btn-icon-img" alt="Portfolio Icon">
            <span class="btn-text">Portfolio(籌備中)</span>
        </a>

        </div>
        
        <hr>
        <h2>我的作品集 (2026/1/8更新）</h2>
        <p>以下是我最近的練習與創作：</p>

        <div class="gallery">

            <div class="artwork-item">
                <img src="https://github.com/a0981151608-creator/Boku/blob/main/assets/images/IMG_1464.PNG?raw=true" 
                alt="作品1" 
                class="artwork">
                <a href="https://www.facebook.com/Waffie0819?locale=zh_TW" target="_blank" class="holder-link">
                Holder: 超級大鬆餠（Waffie）
                </a>
            </div>

            <div class="artwork-item">
                <img src="https://github.com/a0981151608-creator/Boku/blob/main/assets/images/IMG_1487.png?raw=true" 
                alt="作品2" 
                class="artwork">
                <a href="https://www.facebook.com/fox.leap.2025?locale=zh_TW" target="_blank" class="holder-link">
                Holder: Fox Leap（狐躍）
                </a>
            </div>

            <div class="artwork-item">
                <img src="https://github.com/a0981151608-creator/Boku/blob/main/assets/images/IMG_1510.PNG?raw=true" 
                alt="作品3" 
                class="artwork">
                <a href="https://www.facebook.com/loster.mavrick?locale=zh_TW" target="_blank" class="holder-link">
                Holder: Maverick Loster（小洸）
                </a>
            </div>

            <div class="artwork-item">
                <img src="https://github.com/a0981151608-creator/Boku/blob/main/assets/images/IMG_1561.PNG?raw=true" 
                alt="作品4" 
                class="artwork">
                <a href="https://www.facebook.com/bai.chong.404279?locale=zh_TW" target="_blank" class="holder-link">
                Holder: 白舂（舂舂）
                </a>
            </div>

        </div>

        <a href="mailto:a0981151608@gmail.com" class="btn">聯絡我</a>
    </div>
</body>
</html><!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>邱惠君 | 個人介紹</title>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">

    <style>
        :root {
            --navy-dark: #0D1B2A;
            --navy-main: #1B263B;
            --navy-soft: #415A77;
            --blue-soft: #778DA9;
            --text-main: #E0E1DD;
            --card-bg: rgba(27,38,59,0.9);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Noto Sans TC', sans-serif;
            min-height: 100vh;
            background: linear-gradient(135deg, var(--navy-dark), var(--navy-main));
            color: var(--text-main);
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 30px;
        }

        .container {
            max-width: 680px;
            width: 100%;
            background: var(--card-bg);
            padding: 45px;
            border-radius: 22px;
            box-shadow: 0 20px 45px rgba(0,0,0,0.35);
            animation: fadeIn 0.8s ease forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* ===== Header ===== */
        header {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 35px;
        }

        .avatar {
            width: 90px;
            height: 90px;
            border-radius: 50%;
            border: 3px solid rgba(255,255,255,0.6);
            object-fit: cover;
            flex-shrink: 0;
        }

        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.4rem;
            letter-spacing: 2px;
            margin-bottom: 6px;
        }

        .tagline {
            font-size: 0.85rem;
            letter-spacing: 3px;
            color: var(--blue-soft);
        }

        /* ===== Info Section ===== */
        .info-item {
            background: rgba(119,141,169,0.08);
            border-radius: 16px;
            padding: 18px 20px;
            margin-bottom: 18px;
            transition: var(--transition);
        }

        .info-item:hover {
            background: rgba(119,141,169,0.18);
            transform: translateX(6px);
        }

        .label {
            font-size: 0.85rem;
            letter-spacing: 1px;
            font-weight: 700;
            color: var(--blue-soft);
            margin-bottom: 6px;
            display: block;
        }

        .value {
            font-size: 1.05rem;
        }

        a {
            color: #A2D2FF;
            text-decoration: none;
            border-bottom: 1px solid transparent;
        }

        a:hover {
            border-bottom-color: #A2D2FF;
        }

        .badge-container {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }

        .badge {
            background: var(--navy-soft);
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        /* ===== Image Gallery ===== */
        .gallery {
            margin-top: 40px;
        }

        .gallery h2 {
            font-size: 1.2rem;
            letter-spacing: 2px;
            margin-bottom: 18px;
            color: var(--blue-soft);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 18px;
        }

        .gallery-grid img {
            width: 100%;
            border-radius: 16px;
            object-fit: cover;
            box-shadow: 0 10px 25px rgba(0,0,0,0.35);
            transition: var(--transition);
        }

        .gallery-grid img:hover {
            transform: scale(1.03);
        }

        footer {
            margin-top: 45px;
            text-align: center;
            font-size: 0.75rem;
            color: var(--blue-soft);
            opacity: 0.8;
        }

        @media (max-width: 520px) {
            header {
                flex-direction: column;
                text-align: center;
            }
            .gallery-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

<main class="container">

    <header>
        <img src="9-24_da52fcc8de41dd63bf1f282297da9453.jpg" alt="頭像" class="avatar">
        <div>
            <h1>邱惠君</h1>
            <p class="tagline">PERSONAL PROFILE</p>
        </div>
    </header>

    <section>
        <div class="info-item">
            <span class="label">電子郵件 / Contact</span>
            <span class="value">
                <a href="mailto:a0981151608@gmail.com">a0981151608@gmail.com</a>
            </span>
        </div>

        <div class="info-item">
            <span class="label">學歷背景 / Education</span>
            <span class="value">國立嘉義大學｜碩士班在讀</span>
        </div>

        <div class="info-item">
            <span class="label">研究現狀 / Research</span>
            <p class="value">畢業論文籌備中，專注於實驗設計與學術成果累積。</p>
        </div>

        <div class="info-item">
            <span class="label">自我提升 / Self-Learning</span>
            <p class="value">持續在研究之外拓展個人能力：</p>
            <div class="badge-container">
                <span class="badge">精進畫畫</span>
                <span class="badge">日文學習</span>
                <span class="badge">自我進化中</span>
            </div>
        </div>
    </section>

    <section class="gallery">
        <h2>Research Record</h2>
        <div class="gallery-grid">
            <img src="20251211_152948.jpg" alt="實驗照片一">
            <img src="20251211_153033.jpg" alt="實驗照片二">
        </div>
    </section>

    <footer>
        設計與開發 © <span id="year"></span> 邱惠君
    </footer>

</main>

<script>
    document.getElementById('year').textContent = new Date().getFullYear();
</script>

</body>
</html>
# Boku
