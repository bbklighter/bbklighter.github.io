<img width="1920" height="1232" alt="image" src="https://github.com/user-attachments/assets/b778a93d-b598-432b-bb82-3945be7cfe11" /><!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Windows XP 电视频道选择器</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft Sans Serif", Tahoma, Arial, sans-serif;
        }
        
        body {
            background: linear-gradient(to bottom, #3a6ea5, #7db9e8);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #1a3c6c;
        }
        
        .taskbar {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            height: 30px;
            background: linear-gradient(to bottom, #0a246a, #a3c6f3);
            display: flex;
            align-items: center;
            padding: 0 5px;
            box-shadow: inset 0 1px 0 #ffffff;
            z-index: 100;
        }
        
        .start-btn {
            height: 24px;
            background: linear-gradient(to bottom, #33b45c, #0d7d3a);
            border: 1px solid #0a5c26;
            border-radius: 3px;
            color: white;
            font-weight: bold;
            padding: 0 8px;
            display: flex;
            align-items: center;
            cursor: pointer;
            box-shadow: inset 0 1px 0 #7ad698;
        }
        
        .start-btn img {
            margin-right: 5px;
        }
        
        .window {
            width: 500px;
            background: #ece9d8;
            border: 1px solid #0a246a;
            box-shadow: 3px 3px 5px rgba(0, 0, 0, 0.3);
        }
        
        .title-bar {
            background: linear-gradient(to right, #0a246a, #a3c6f3);
            color: white;
            padding: 4px 8px;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .title-bar-btns {
            display: flex;
        }
        
        .title-bar-btn {
            width: 20px;
            height: 20px;
            margin-left: 4px;
            background: #c0c0c0;
            border: 1px solid #808080;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            cursor: pointer;
        }
        
        .window-content {
            padding: 20px;
            border: 2px solid #0a246a;
            border-top: none;
        }
        
        .xp-control-group {
            margin-bottom: 20px;
        }
        
        .xp-label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        .xp-input {
            width: 100%;
            padding: 6px;
            border: 2px solid #7f9db9;
            background: white;
            font-size: 16px;
        }
        
        .xp-btn {
            background: linear-gradient(to bottom, #f6f6f6, #e3e3e3);
            border: 1px solid #7f9db9;
            padding: 6px 12px;
            font-weight: bold;
            cursor: pointer;
        }
        
        .xp-btn:hover {
            background: linear-gradient(to bottom, #e8f4ff, #d6e8ff);
        }
        
        .xp-btn:active {
            background: linear-gradient(to bottom, #d6e8ff, #e8f4ff);
        }
        
        .channels-grid {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 10px;
            margin-top: 20px;
        }
        
        .channel-btn {
            height: 60px;
            background: linear-gradient(to bottom, #f6f6f6, #e3e3e3);
            border: 1px solid #7f9db9;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: all 0.2s;
        }
        
        .channel-btn:hover {
            background: linear-gradient(to bottom, #e8f4ff, #d6e8ff);
            transform: scale(1.05);
        }
        
        .channel-btn:active {
            background: linear-gradient(to bottom, #d6e8ff, #e8f4ff);
        }
        
        .channel-number {
            font-size: 18px;
            font-weight: bold;
            color: #0a246a;
        }
        
        .channel-name {
            font-size: 12px;
            margin-top: 5px;
            color: #333;
        }
        
        .footer {
            margin-top: 20px;
            text-align: center;
            font-size: 12px;
            color: #666;
        }
        
        /* 小窗样式 - 在频道页面使用 */
        .channel-banner {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(0, 0, 0, 0.7);
            border: 2px solid #f0f0f0;
            padding: 10px;
            display: flex;
            align-items: center;
            z-index: 1000;
            border-radius: 5px;
            animation: fadeOut 5s forwards;
        }
        
        .channel-logo {
            width: 60px;
            height: 60px;
            margin-right: 15px;
            background-color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            font-size: 12px;
            text-align: center;
            padding: 5px;
        }
        
        .channel-title {
            font-size: 24px;
            font-weight: bold;
            color: white;
        }
        
        @keyframes fadeOut {
            0% { opacity: 1; }
            70% { opacity: 1; }
            100% { opacity: 0; display: none; }
        }
        
        /* 频道页面样式 */
        .video-container {
            position: relative;
            width: 100%;
            padding-top: 56.25%; /* 16:9 Aspect Ratio */
            background-color: #000;
        }
        
        .video-player {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .back-btn {
            position: absolute;
            top: 20px;
            left: 20px;
            background: rgba(0, 0, 0, 0.5);
            color: white;
            padding: 8px 15px;
            border: none;
            cursor: pointer;
            z-index: 50;
        }
    </style>
</head>
<body>
    <!-- Windows XP 任务栏 -->
    <div class="taskbar">
        <div class="start-btn">
            <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAi0lEQVQ4T2NkoDJgpLK5DCMWgKOi4v8fP378x1dQXFwcA1cBIS1gLf/+/ft/9uxZbEaA8ZkzZ8L4cAXYtIBFb9y4gaEFrOXGjRtYtTAyMjLCFcA9gM0GpCjCqgXqGpgnkL0P9wRcCzY3gGXhWv7+/fv/zJkzON0A1oJTC1TL379//589exavFqQoQvEEUjSCTQd7Ap8WkCxOLeDcDdICAAwSXv3sMo2NAAAAAElFTkSuQmCC" alt="Start">
            <span>开始</span>
        </div>
    </div>

    <!-- 主窗口 -->
    <div class="window">
        <div class="title-bar">
            <div>Windows XP 电视频道选择器</div>
            <div class="title-bar-btns">
                <div class="title-bar-btn">_</div>
                <div class="title-bar-btn">□</div>
                <div class="title-bar-btn">×</div>
            </div>
        </div>
        
        <div class="window-content">
            <div class="xp-control-group">
                <label class="xp-label" for="channel-input">输入频道号 (1-10):</label>
                <input type="number" id="channel-input" class="xp-input" min="1" max="10" value="1">
            </div>
            
            <button id="watch-btn" class="xp-btn">观看频道</button>
            
            <div class="channels-grid">
                <!-- 频道按钮将通过JS生成 -->
            </div>
            
            <div class="footer">
                <p>Windows XP © 2001 Microsoft Corporation. 保留所有权利。</p>
            </div>
        </div>
    </div>

    <script>
        // 频道数据
        const channels = [
            { number: 1, name: "翡翠台", img: "http://www.redhotmedia.com.cn//FCK/userupfile/images/2009727562397793085.jpg", url: "1.html" },
            { number: 2, name: "凤凰资讯", img: "https://upload.wikimedia.org/wikipedia/zh/1/16/Phoenix_InfoNews.svg", url: "2.html" },
            { number: 3, name: "CNN", img: "https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/CNN.svg/2560px-CNN.svg.png", url: "3.html" },
            { number: 4, name: "国家地理", img: "https://upload.wikimedia.org/wikipedia/commons/thumb/f/fc/Natgeologo.svg/1280px-Natgeologo.svg.png", url: "4.html" },
            { number: 5, name: "体育频道", img: "https://cdn.worldvectorlogo.com/logos/espn-2.svg", url: "5.html" },
            { number: 6, name: "电影频道", img: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/80/HBO_logo.svg/1280px-HBO_logo.svg.png", url: "6.html" },
            { number: 7, name: "卡通频道", img: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/80/Cartoon_Network_2010_logo.svg/1280px-Cartoon_Network_2010_logo.svg.png", url: "7.html" },
            { number: 8, name: "新闻频道", img: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/67/CNN_International_logo.svg/1280px-CNN_International_logo.svg.png", url: "8.html" },
            { number: 9, name: "音乐频道", img: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/98/MTV_Logo_2010.svg/1280px-MTV_Logo_2010.svg.png", url: "9.html" },
            { number: 10, name: "财经频道", img: "https://upload.wikimedia.org/wikipedia/commons/thumb/0/0c/Bloomberg_Television_Logo_2017.svg/1280px-Bloomberg_Television_Logo_2017.svg.png", url: "10.html" }
        ];

        // 生成频道按钮
        const grid = document.querySelector('.channels-grid');
        channels.forEach(channel => {
            const btn = document.createElement('div');
            btn.className = 'channel-btn';
            btn.innerHTML = `
                <div class="channel-number">${channel.number}</div>
                <div class="channel-name">${channel.name}</div>
            `;
            btn.addEventListener('click', () => {
                window.location.href = channel.url;
            });
            grid.appendChild(btn);
        });

        // 观看按钮事件
        document.getElementById('watch-btn').addEventListener('click', () => {
            const channelNum = document.getElementById('channel-input').value;
            if (channelNum >= 1 && channelNum <= 10) {
                window.location.href = `${channelNum}.html`;
            } else {
                alert('请输入有效的频道号 (1-10)');
            }
        });
    </script>
</body>
</html>
