<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>bbklighter的私人博客</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Tahoma", "Microsoft Sans Serif", sans-serif;
        }
        
        body {
            background-color: #008080;
            background-image: url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI4IiBoZWlnaHQ9IjgiPgo8cmVjdCB3aWR0aD0iOCIgaGVpZ2h0PSI4IiBmaWxsPSIjMDA4MDgwIj48L3JlY3Q+CjxyZWN0IHdpZHRoPSI0IiBoZWlnaHQ9IjQiIGZpbGw9IiMwMDY0NjQiPjwvcmVjdD4KPC9zdmc+');
            color: #000;
            height: 600px;
            width: 800px;
            overflow: hidden;
            position: relative;
            margin: 0 auto;
            border: 2px solid #003399;
            box-shadow: 0 0 20px rgba(0,0,0,0.5);
        }
        
        /* 桌面图标样式 */
        .desktop-icons {
            position: absolute;
            top: 10px;
            left: 10px;
            width: 100%;
            height: 100%;
        }
        
        .desktop-icon {
            width: 80px;
            height: 80px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: absolute;
            color: white;
            text-align: center;
            font-size: 12px;
            text-shadow: 1px 1px 1px #000;
            cursor: pointer;
            user-select: none;
        }
        
        .desktop-icon:hover {
            background-color: rgba(0, 64, 128, 0.5);
            border: 1px dotted white;
        }
        
        .desktop-icon img {
            width: 48px;
            height: 48px;
            margin-bottom: 5px;
        }
        
        /* 任务栏样式 */
        .taskbar {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 40px;
            background: linear-gradient(to bottom, #0A246A, #0055AA);
            border-top: 1px solid #2A4BD7;
            display: flex;
            align-items: center;
            padding: 0 5px;
            z-index: 1000;
        }
        
        .start-button {
            height: 32px;
            padding: 0 10px;
            background: linear-gradient(to bottom, #1D8C1D, #0A7D0A);
            color: white;
            font-weight: bold;
            font-size: 14px;
            border: 1px solid #2A4BD7;
            border-radius: 3px;
            display: flex;
            align-items: center;
            cursor: pointer;
            margin-right: 5px;
        }
        
        .start-button img {
            margin-right: 5px;
            width: 16px;
            height: 16px;
        }
        
        .taskbar-items {
            display: flex;
            flex-grow: 1;
            height: 100%;
        }
        
        .taskbar-item {
            height: 30px;
            padding: 0 15px;
            background: linear-gradient(to bottom, #3A6EA5, #0A246A);
            color: white;
            display: flex;
            align-items: center;
            border-radius: 3px;
            margin: 0 3px;
            cursor: pointer;
            font-size: 12px;
            border: 1px solid #2A4BD7;
        }
        
        .taskbar-item.active {
            background: linear-gradient(to bottom, #7BAFD4, #3A6EA5);
        }
        
        .system-tray {
            display: flex;
            align-items: center;
            padding: 0 5px;
            height: 100%;
            color: white;
            font-size: 12px;
        }
        
        /* 窗口样式 */
        .window {
            position: absolute;
            background: linear-gradient(to bottom, #ECECEC, #D4D0C8);
            border: 2px solid;
            border-top-color: #FFFFFF;
            border-left-color: #FFFFFF;
            border-right-color: #808080;
            border-bottom-color: #808080;
            box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.3);
            min-width: 300px;
            min-height: 200px;
            display: none;
            z-index: 100;
            flex-direction: column;
        }
        
        .window.active {
            display: flex;
            z-index: 200;
        }
        
        .window-header {
            background: linear-gradient(to right, #0A246A, #3A6EA5);
            color: white;
            padding: 4px 8px;
            font-size: 14px;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: move;
            user-select: none;
        }
        
        .window-controls {
            display: flex;
        }
        
        .window-control {
            width: 22px;
            height: 22px;
            margin-left: 4px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(to bottom, #ECECEC, #D4D0C8);
            border: 1px solid;
            border-top-color: #FFFFFF;
            border-left-color: #FFFFFF;
            border-right-color: #808080;
            border-bottom-color: #808080;
            cursor: pointer;
            font-weight: bold;
            color: #000;
        }
        
        .window-content {
            padding: 15px;
            flex-grow: 1;
            overflow: auto;
            font-size: 14px;
            line-height: 1.5;
        }
        
        /* 博客内容样式 */
        .blog-post {
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #C0C0C0;
        }
        
        .blog-post h3 {
            color: #0A246A;
            margin-bottom: 10px;
            font-size: 18px;
        }
        
        .blog-post .date {
            color: #666;
            font-size: 12px;
            margin-bottom: 10px;
        }
        
        .blog-post p {
            margin-bottom: 10px;
        }
        
        /* 开始菜单 */
        .start-menu {
            position: absolute;
            bottom: 40px;
            left: 5px;
            width: 300px;
            background: linear-gradient(to bottom, #ECECEC, #D4D0C8);
            border: 2px solid;
            border-top-color: #FFFFFF;
            border-left-color: #FFFFFF;
            border-right-color: #808080;
            border-bottom-color: #808080;
            display: none;
            z-index: 300;
        }
        
        .start-menu.active {
            display: block;
        }
        
        .start-menu-header {
            background: linear-gradient(to right, #0A246A, #3A6EA5);
            color: white;
            padding: 10px;
            font-weight: bold;
            font-size: 16px;
        }
        
        .start-menu-items {
            padding: 10px;
        }
        
        .start-menu-item {
            padding: 8px;
            display: flex;
            align-items: center;
            cursor: pointer;
        }
        
        .start-menu-item:hover {
            background-color: #0A246A;
            color: white;
        }
        
        .start-menu-item img {
            margin-right: 10px;
            width: 24px;
            height: 24px;
        }
        
        /* 其他UI元素 */
        .clock {
            margin-right: 10px;
        }
        
        .desktop-label {
            position: absolute;
            bottom: 40px;
            right: 10px;
            color: white;
            font-size: 12px;
            text-shadow: 1px 1px 1px #000;
        }
    </style>
</head>
<body>
    <!-- 桌面图标 -->
    <div class="desktop-icons">
        <div class="desktop-icon" style="top: 20px; left: 20px;" onclick="openWindow('blog')">
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCIgdmlld0JveD0iMCAwIDQ4IDQ4Ij48cmVjdCB3aWR0aD0iNDgiIGhlaWdodD0iNDgiIGZpbGw9IiMwMDgwODAiIHN0cm9rZT0iIzAwNjQ2NCIgc3Ryb2tlLXdpZHRoPSIyIi8+PHBhdGggZD0iTTE0IDE0aDIwdjIwSDE0eiIgZmlsbD0iIzAwNjQ2NCIvPjxwYXRoIGQ9Ik0xOCAxOGgxMnYxMkgxOHoiIGZpbGw9IiNmZmYiLz48L3N2Zz4=" alt="博客">
            <span>我的博客</span>
        </div>
        <div class="desktop-icon" style="top: 20px; left: 120px;" onclick="openWindow('about')">
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCIgdmlld0JveD0iMCAwIDQ4IDQ4Ij48Y2lyY2xlIGN4PSIyNCIgY3k9IjI0IiByPSIyMCIgZmlsbD0iIzMxNkFDMCIgc3Ryb2tlPSIjMEM0ODgwIiBzdHJva2Utd2lkdGg9IjIiLz48Y2lyY2xlIGN4PSIyNCIgY3k9IjE3IiByPSIyIiBmaWxsPSIjZmZmIi8+PHBhdGggZD0iTTI0IDIzTDI0IDM1IiBzdHJva2U9IiNmZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIi8+PC9zdmc+" alt="关于">
            <span>关于我</span>
        </div>
        <div class="desktop-icon" style="top: 20px; left: 220px;" onclick="openWindow('photos')">
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCIgdmlld0JveD0iMCAwIDQ4IDQ4Ij48cmVjdCB3aWR0aD0iNDAiIGhlaWdodD0iMzAiIHg9IjQiIHk9IjgiIGZpbGw9IiMzMTZBQzAiIHN0cm9rZT0iIzBDNDg4MCIgc3Ryb2tlLXdpZHRoPSIyIiByeD0iMiIvPjxjaXJjbGUgY3g9IjE1IiBjeT0iMTciIHI9IjUiIGZpbGw9IiNGRkZDMDAiIHN0cm9rZT0iI0Q0QjAwMCIgc3Ryb2tlLXdpZHRoPSIyIi8+PHBhdGggZD0iTTM4IDE4TDI4IDI4TDIyIDIyTDE0IDMwIiBzdHJva2U9IiNmZmYiIHN0cm9rZS13aWR0aD0iMyIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIi8+PC9zdmc+" alt="照片">
            <span>我的相册</span>
        </div>
        <div class="desktop-icon" style="top: 120px; left: 20px;" onclick="openWindow('links')">
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCIgdmlld0JveD0iMCAwIDQ4IDQ4Ij48cGF0aCBkPSJNMjQgNEMxMi45NSA0IDQgMTIuOTUgNCAyNHM4Ljk1IDIwIDIwIDIwIDIwLTguOTUgMjAtMjBTMzUuMDUgNCAyNCA0em0wIDM2Yy04LjgyIDAtMTYtNy4xOC0xNi0xNlMxNS4xOCA4IDI0IDhzMTYgNy4xOCAxNiAxNi03LjE4IDE2LTE2IDE2eiIgZmlsbD0iIzMxNkFDMCIvPjxwYXRoIGQ9Ik0yNiAxNGgtNGMtMS4xIDAtMiAuOS0yIDJ2MTZjMCAxLjEuOSAyIDIgMmg0YzEuMSAwIDItLjkgMi0yVjE2YzAtMS4xLS45LTItMi0yem0tMiAxNnYtMTJoMnYxMnoiIGZpbGw9IiNmZmYiLz48L3N2Zz4=" alt="链接">
            <span>友情链接</span>
        </div>
        <div class="desktop-icon" style="top: 120px; left: 120px;" onclick="openWindow('guestbook')">
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0OCIgaGVpZ2h0PSI0OCIgdmlld0JveD0iMCAwIDQ4IDQ4Ij48cGF0aCBkPSJNMzAgNEgxMGMtMi4yMSAwLTQgMS43OS00IDR2MzZjMCAyLjIxIDEuNzkgNCA0IDBoMjhjMi4yMSAwIDQtMS43OSA0LTRWOGMwLTIuMjEtMS43OS00LTQtNHptMCAzMkgxMFY4aDIwdjI4eiIgZmlsbD0iIzMxNkFDMCIvPjxwYXRoIGQ9Ik0yMiAyMGg4djRoLTh6TTIyIDI4aDEydjRoLTEyeiIgZmlsbD0iI2ZmZiIvPjwvc3ZnPg==" alt="留言">
            <span>留言板</span>
        </div>
    </div>
    
    <!-- 桌面标签 -->
    <div class="desktop-label">2005年7月30日</div>
    
    <!-- 博客窗口 -->
    <div class="window" id="blog-window">
        <div class="window-header">
            <span>我的博客</span>
            <div class="window-controls">
                <div class="window-control" onclick="minimizeWindow('blog')">_</div>
                <div class="window-control" onclick="closeWindow('blog')">×</div>
            </div>
        </div>
        <div class="window-content">
            <h2 style="color: #0A246A; margin-bottom: 15px;">欢迎来到我的私人博客</h2>
            
            <div class="blog-post">
                <h3>1</h3>
                <div class="date">2005年7月28日</div>
                <p></p>
                <p>个人主页、留言板、QQ聊天室、Flash小游戏，这些构成了我们最初的互联网记忆。那时候的网页设计简单直接，没有太多花哨的效果，却充满了真诚。</p>
            </div>
            
            <div class="blog-post">
                <h3>Windows XP - 一个时代的经典</h3>
                <div class="date">2005年7月20日</div>
                <p>蓝天白云的壁纸，绿色的开始按钮，还有那个经典的月神主题。Windows XP不仅仅是一个操作系统，它是一个时代的象征。</p>
                <p>2001年发布的XP系统，以其稳定性和友好的界面迅速征服了全球用户。直到今天，仍有很多人怀念它的简洁和高效。</p>
                <p>你还记得第一次听到XP启动音时的感受吗？对我来说，那代表着无限的可能性。</p>
            </div>
            
            <div class="blog-post">
                <h3>我的新电脑配置</h3>
                <div class="date">2005年7月15日</div>
                <p>终于升级了我的电脑！现在的配置是：</p>
                <ul>
                    <li>CPU: Pentium 4 3.0GHz</li>
                    <li>内存: 1GB DDR</li>
                    <li>硬盘: 160GB</li>
                    <li>显卡: GeForce FX 5700</li>
                    <li>显示器: 17寸 CRT</li>
                </ul>
                <p>这样的配置在当时算是相当不错了，玩《魔兽世界》和《半条命2》都很流畅！</p>
            </div>
        </div>
    </div>
    
    <!-- 关于窗口 -->
    <div class="window" id="about-window">
        <div class="window-header">
            <span>关于我</span>
            <div class="window-controls">
                <div class="window-control" onclick="minimizeWindow('about')">_</div>
                <div class="window-control" onclick="closeWindow('about')">×</div>
            </div>
        </div>
        <div class="window-content">
            <h2 style="color: #0A246A; margin-bottom: 15px;">关于博主</h2>
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMDAiIGhlaWdodD0iMTAwIiB2aWV3Qm94PSIwIDAgMTAwIDEwMCI+PGNpcmNsZSBjeD0iNTAiIGN5PSIzMCIgcj0iMjAiIGZpbGw9IiMzMTZBQzAiLz48cGF0aCBkPSJNNTAgNjhjLTIyIDAtNDAtMTgtNDAtNDBzMTgtNDAgNDAtNDAgNDAgMTggNDAgNDAtMTggNDAtNDAgNDB6IiBmaWxsPSJub25lIiBzdHJva2U9IiMwQzQ4ODAiIHN0cm9rZS13aWR0aD0iNCIvPjxwYXRoIGQ9Ik0yMCA4MGg2MHYxMEgyMHoiIGZpbGw9IiMzMTZBQzAiLz48L3N2Zz4=" alt="头像" style="float: left; margin-right: 15px; width: 80px;">
            <p><strong>姓名：</strong>张明</p>
            <p><strong>年龄：</strong>25岁</p>
            <p><strong>职业：</strong>网页设计师</p>
            <p><strong>所在地：</strong>北京</p>
            <p><strong>兴趣爱好：</strong>网页设计、电脑游戏、收集老式硬件、听周杰伦的歌</p>
            <p><strong>联系方式：</strong>zhangming@hotmail.com</p>
            <p style="margin-top: 15px;">我是2000年代互联网文化的爱好者，这个博客记录了我的兴趣、想法和回忆。欢迎你来到我的网络小天地！</p>
        </div>
    </div>
    
    <!-- 任务栏 -->
    <div class="taskbar">
        <div class="start-button" onclick="toggleStartMenu()">
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgaGVpZ2h0PSIxNiIgdmlld0JveD0iMCAwIDE2IDE2Ij48cGF0aCBkPSJNOCAwTDE0LjIgNC44TDEyLjggNi44TDggMy40TDMuMiA2LjhMMS44IDQuOHoiIGZpbGw9IiNmZmYiLz48cGF0aCBkPSJNOCA0TDE0LjIgOC44TDEyLjggMTAuOEw4IDcuNEwzLjIgMTAuOEwxLjggOC44eiIgZmlsbD0iI2ZmZiIvPjxwYXRoIGQ9Ik04IDhMMTQuMiAxMi44TDEyLjggMTQuOEw4IDExLjRMMy4yIDE0LjhMMS44IDEyLjh6IiBmaWxsPSIjZmZmIi8+PC9zdmc+" alt="开始">
            开始
        </div>
        <div class="taskbar-items">
            <div class="taskbar-item active" onclick="openWindow('blog')">
                我的博客
            </div>
        </div>
        <div class="system-tray">
            <div class="clock">16:45</div>
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgaGVpZ2h0PSIxNiIgdmlld0JveD0iMCAwIDE2IDE2Ij48cGF0aCBkPSJNOCAxQzQuMSAxIDEgNC4xIDEgOHMzLjEgNyA3IDcgNy0zLjEgNy03cy0zLjEtNy03LTd6bTAgMTNjLTMuMyAwLTYtMi43LTYtNnMyLjctNiA2LTYgNiAyLjcgNiA2LTIuNyA2LTYgNnoiIGZpbGw9IiNmZmYiLz48cGF0aCBkPSJNOC41IDRIN3Y1bDMuNiAyLjIuOC0xLjItMy0xLjZWNHoiIGZpbGw9IiNmZmYiLz48L3N2Zz4=" alt="音量" style="margin: 0 5px;">
            <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgaGVpZ2h0PSIxNiIgdmlld0JveD0iMCAwIDE2IDE2Ij48cGF0aCBkPSJNMTMgM0gzdjFoMTBWM3ptMCA0SDN2MWgxMFY3em0wIDRIM3YxaDEwdi0xem0wIDRIM3YxaDEwdi0xeiIgZmlsbD0iI2ZmZiIvPjwvc3ZnPg==" alt="网络" style="margin: 0 5px;">
        </div>
    </div>
    
    <!-- 开始菜单 -->
    <div class="start-menu" id="start-menu">
        <div class="start-menu-header">张明的个人博客</div>
        <div class="start-menu-items">
            <div class="start-menu-item" onclick="openWindow('blog')">
                <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBkPSJNMTQgMkg2Yy0xLjEgMC0xLjk5LjktMS45OSAyTCA0IDIwdjBjMCAxLjEuODkgMiAyIDJoMTJjMS4xIDAgMi0uOSAyLTJWN0wxNCAyeiIgZmlsbD0iIzMxNkFDMCIvPjxwYXRoIGQ9Ik0yMCA4aC00Yy0xLjEgMC0xLjk5LS45LTEuOTktMkwxNCAzbDQgNXoiIGZpbGw9IiMwQzQ4ODAiLz48cGF0aCBkPSJNNiA4aDEydjEwSDZWOXoiIGZpbGw9IiNmZmYiLz48L3N2Zz4=" alt="文档">
                <span>我的博客</span>
            </div>
            <div class="start-menu-item" onclick="openWindow('photos')">
                <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBkPSJNMTkgM0g1Yy0xLjEgMC0yIC45LTIgMnYxNGMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjVjMC0xLjEtLjktMi0yLTJ6IiBmaWxsPSIjMzE2QUMwIi8+PHBhdGggZD0iTTE0IDE0bC0zLTNsLTQgNGgxNGwtNC00eiIgZmlsbD0iI0ZGRkMwMCIvPjxjaXJjbGUgY3g9IjguNSIgY3k9IjguNSIgcj0iMS41IiBmaWxsPSIjZmZmIi8+PC9zdmc+" alt="照片">
                <span>我的相册</span>
            </div>
            <div class="start-menu-item" onclick="openWindow('guestbook')">
                <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBkPSJNMjAgMkg0Yy0xLjEgMC0yIC45LTIgMnYxOGw0LTRoMTRjMS4xIDAgMi0uOSAyLTJWNGMwLTEuMS0uOS0yLTItMnoiIGZpbGw9IiMzMTZBQzAiLz48cGF0aCBkPSJNMTggMTRINnYyaDEydi0yem0wLTNINnYyaDEydi0yem0wLTNINnYyaDEyVjh6IiBmaWxsPSIjZmZmIi8+PC9zdmc+" alt="留言">
                <span>留言板</span>
            </div>
            <div class="start-menu-item">
                <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBkPSJNMTkgM0g1Yy0xLjEgMC0yIC45LTIgMnYxNGMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjVjMC0xLjEtLjktMi0yLTJ6IiBmaWxsPSIjMzE2QUMwIi8+PHBhdGggZD0iTTE5IDE5SDRjLS41NSAwLTEtLjQ1LTEtMVY2YzAtLjU1LjQ1LTEgMS0xaDE0Yy41NSAwIDEgLjQ1IDEgMXYxMmMwIC41NS0uNDUgMS0xIDF6IiBmaWxsPSIjZmZmIi8+PHBhdGggZD0iTTcgMTBoMTB2MUg3em0wIDJoMTB2MUg3em0wIDJoMTB2MUg3eiIgZmlsbD0iIzMxNkFDMCIvPjwvc3ZnPg==" alt="帮助">
                <span>帮助和支持</span>
            </div>
            <div class="start-menu-item">
                <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBkPSJNMTIgMkM2LjQ4IDIgMiA2LjQ4IDIgMTJzNC40OCAxMCAxMCAxMCAxMC00LjQ4IDEwLTEwUzE3LjUyIDIgMTIgMnptMCAxOGMtNC40MSAwLTgtMy41OS04LThzMy41OS04IDgtOCA4IDMuNTkgOCA4LTMuNTkgOC04IDh6IiBmaWxsPSIjMzE2QUMwIi8+PHBhdGggZD0iTTEyIDdjLS4yOCAwLS41LjIyLS41LjV2N2MwIC4yOC4yMi41LjUuNXMuNS0uMjIuNS0uNVY3LjVjMC0uMjgtLjIyLS41LS41LS41eiIgZmlsbD0iI2ZmZiIvPjxjaXJjbGUgY3g9IjEyIiBjeT0iMTYiIHI9IjEiIGZpbGw9IiNmZmYiLz48L3N2Zz4=" alt="运行">
                <span>运行...</span>
            </div>
            <div class="start-menu-item">
                <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij48cGF0aCBkPSJNMTAgMTd2LTdIMnY3aDh6bTItNUg0di0xaDh2MXptOCA1di03aC04djdIOFYyMmgxNHYtNUgxMnoiIGZpbGw9IiMzMTZBQzAiLz48cGF0aCBkPSJNMjAgMTBoLTJ2OWgydjdoLTZ2LTdoMnYtOWgtMnYtMmg2djJoLTJ6TTQgMTBoLTJ2OUgwdjdINnYtN0g0di05SDJWN2g2djNINHoiIGZpbGw9IiNmZmYiLz48L3N2Zz4=" alt="关机">
                <span>关闭计算机</span>
            </div>
        </div>
    </div>

    <script>
        // 窗口管理
        function openWindow(windowId) {
            // 关闭开始菜单
            document.getElementById('start-menu').classList.remove('active');
            
            // 打开窗口
            document.getElementById(windowId + '-window').classList.add('active');
            
            // 更新任务栏
            updateTaskbar(windowId);
        }
        
        function closeWindow(windowId) {
            document.getElementById(windowId + '-window').classList.remove('active');
            removeTaskbarItem(windowId);
        }
        
        function minimizeWindow(windowId) {
            document.getElementById(windowId + '-window').classList.remove('active');
            removeTaskbarActive(windowId);
        }
        
        // 开始菜单切换
        function toggleStartMenu() {
            const menu = document.getElementById('start-menu');
            menu.classList.toggle('active');
        }
        
        // 任务栏管理
        function updateTaskbar(windowId) {
            const taskbar = document.querySelector('.taskbar-items');
            const existing = document.querySelector(`.taskbar-item[data-window="${windowId}"]`);
            
            if (!existing) {
                const item = document.createElement('div');
                item.className = 'taskbar-item';
                item.setAttribute('data-window', windowId);
                item.textContent = getWindowName(windowId);
                item.onclick = () => openWindow(windowId);
                taskbar.appendChild(item);
            }
            
            // 设置当前窗口为活动状态
            document.querySelectorAll('.taskbar-item').forEach(el => {
                el.classList.remove('active');
            });
            
            const current = document.querySelector(`.taskbar-item[data-window="${windowId}"]`);
            if (current) current.classList.add('active');
        }
        
        function removeTaskbarItem(windowId) {
            const item = document.querySelector(`.taskbar-item[data-window="${windowId}"]`);
            if (item) item.remove();
        }
        
        function removeTaskbarActive(windowId) {
            const item = document.querySelector(`.taskbar-item[data-window="${windowId}"]`);
            if (item) item.classList.remove('active');
        }
        
        function getWindowName(windowId) {
            const names = {
                'blog': '我的博客',
                'about': '关于我',
                'photos': '我的相册',
                'links': '友情链接',
                'guestbook': '留言板'
            };
            return names[windowId] || windowId;
        }
        
        // 初始化页面时打开博客窗口
        window.onload = function() {
            openWindow('blog');
            
            // 更新时间
            function updateClock() {
                const now = new Date();
                const hours = String(now.getHours()).padStart(2, '0');
                const minutes = String(now.getMinutes()).padStart(2, '0');
                document.querySelector('.clock').textContent = `${hours}:${minutes}`;
            }
            
            updateClock();
            setInterval(updateClock, 60000);
        };
    </script>
</body>
</html>
