<?php
// 获取远程m3u文件内容
$m3u_url = "https://aktv.space/live.m3u";
$m3u_content = @file_get_contents($m3u_url);

$channels = [];
if ($m3u_content) {
    // 解析m3u文件
    $lines = explode("\n", $m3u_content);
    $current_channel = null;
    
    foreach ($lines as $line) {
        $line = trim($line);
        if (empty($line)) continue;
        
        if (strpos($line, '#EXTINF:') === 0) {
            // 提取频道名称
            $parts = explode(',', $line);
            $current_channel = [
                'name' => end($parts),
                'url' => null
            ];
        } elseif ($current_channel && !$current_channel['url'] && filter_var($line, FILTER_VALIDATE_URL)) {
            // 提取URL
            $current_channel['url'] = $line;
            $channels[] = $current_channel;
            $current_channel = null;
        }
    }
}
?>
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Windows XP风格视频播放器</title>
    <link href="https://cdn.jsdelivr.net/npm/hls.js@latest" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/hls.js@latest"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Tahoma", "Microsoft Sans Serif", sans-serif;
        }
        
        body {
            background-color: #008080;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="4" height="4" viewBox="0 0 4 4"><rect width="4" height="4" fill="%2300a0a0"/><path d="M0 0L4 4M4 0L0 4" stroke="%23007070" stroke-width="0.5"/></svg>');
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }
        
        .window {
            width: 800px;
            height: 600px;
            background: #c0c0c0;
            border: 2px solid;
            border-top-color: #ffffff;
            border-left-color: #ffffff;
            border-right-color: #808080;
            border-bottom-color: #808080;
            box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.5);
            display: flex;
            flex-direction: column;
            position: relative;
        }
        
        .title-bar {
            background: linear-gradient(to right, #000080, #1084d0);
            color: white;
            padding: 4px 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: bold;
            font-size: 14px;
            height: 22px;
        }
        
        .window-title {
            display: flex;
            align-items: center;
            gap: 6px;
        }
        
        .window-icon {
            width: 16px;
            height: 16px;
            background-color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            color: #000080;
            font-size: 12px;
        }
        
        .window-controls {
            display: flex;
            gap: 2px;
        }
        
        .window-btn {
            width: 20px;
            height: 20px;
            background: #c0c0c0;
            border: 1px solid;
            border-top-color: #ffffff;
            border-left-color: #ffffff;
            border-right-color: #808080;
            border-bottom-color: #808080;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            font-size: 12px;
            color: #000;
            cursor: pointer;
        }
        
        .window-btn:active {
            border-top-color: #808080;
            border-left-color: #808080;
            border-right-color: #ffffff;
            border-bottom-color: #ffffff;
        }
        
        .menu-bar {
            background: #c0c0c0;
            border-top: 1px solid #808080;
            padding: 2px 4px;
            display: flex;
            gap: 15px;
            font-size: 13px;
        }
        
        .menu-item {
            padding: 2px 8px;
            cursor: default;
        }
        
        .menu-item:hover {
            background: #000080;
            color: white;
        }
        
        .content {
            display: flex;
            flex: 1;
            padding: 10px;
            gap: 10px;
            overflow: hidden;
        }
        
        .video-container {
            flex: 3;
            background: #000;
            border: 2px solid;
            border-top-color: #808080;
            border-left-color: #808080;
            border-right-color: #ffffff;
            border-bottom-color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }
        
        #videoPlayer {
            width: 100%;
            height: 100%;
            background: #000;
        }
        
        .channel-list {
            flex: 1;
            background: #c0c0c0;
            border: 2px solid;
            border-top-color: #ffffff;
            border-left-color: #ffffff;
            border-right-color: #808080;
            border-bottom-color: #808080;
            overflow-y: auto;
        }
        
        .channel-list-title {
            background: #000080;
            color: white;
            padding: 4px 8px;
            font-weight: bold;
            font-size: 14px;
        }
        
        .channel-items {
            list-style: none;
            padding: 4px 0;
        }
        
        .channel-item {
            padding: 6px 10px;
            cursor: pointer;
            font-size: 13px;
            border-bottom: 1px solid #808080;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        
        .channel-item:hover {
            background: #000080;
            color: white;
        }
        
        .channel-item.active {
            background: #000080;
            color: white;
            font-weight: bold;
        }
        
        .status-bar {
            height: 22px;
            background: #c0c0c0;
            border-top: 1px solid #808080;
            display: flex;
            align-items: center;
            padding: 0 8px;
            font-size: 12px;
            color: #000;
        }
        
        .loading {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 18px;
            z-index: 10;
            display: none;
        }
        
        .no-content {
            color: #808080;
            text-align: center;
            padding: 20px;
            font-style: italic;
        }
        
        .watermark {
            position: absolute;
            bottom: 10px;
            right: 10px;
            color: rgba(255, 255, 255, 0.3);
            font-size: 12px;
        }
        
        .btn {
            padding: 4px 12px;
            background: #c0c0c0;
            border: 2px solid;
            border-top-color: #ffffff;
            border-left-color: #ffffff;
            border-right-color: #808080;
            border-bottom-color: #808080;
            cursor: pointer;
            font-size: 12px;
            margin-right: 5px;
        }
        
        .btn:active {
            border-top-color: #808080;
            border-left-color: #808080;
            border-right-color: #ffffff;
            border-bottom-color: #ffffff;
        }
    </style>
</head>
<body>
    <div class="window">
        <div class="title-bar">
            <div class="window-title">
                <div class="window-icon">W</div>
                <span>Windows XP 视频播放器</span>
            </div>
            <div class="window-controls">
                <div class="window-btn">_</div>
                <div class="window-btn">□</div>
                <div class="window-btn">×</div>
            </div>
        </div>
        
        <div class="menu-bar">
            <div class="menu-item">文件(F)</div>
            <div class="menu-item">编辑(E)</div>
            <div class="menu-item">查看(V)</div>
            <div class="menu-item">帮助(H)</div>
        </div>
        
        <div class="content">
            <div class="video-container">
                <div class="loading" id="loadingIndicator">正在加载视频...</div>
                <video id="videoPlayer" controls></video>
                <div class="watermark">Windows XP Video Player</div>
            </div>
            
            <div class="channel-list">
                <div class="channel-list-title">频道列表</div>
                <ul class="channel-items">
                    <?php if (!empty($channels)): ?>
                        <?php foreach ($channels as $index => $channel): ?>
                            <li class="channel-item <?= $index === 0 ? 'active' : '' ?>" 
                                data-url="<?= htmlspecialchars($channel['url']) ?>">
                                <?= htmlspecialchars($channel['name']) ?>
                            </li>
                        <?php endforeach; ?>
                    <?php else: ?>
                        <li class="no-content">无法加载频道列表</li>
                    <?php endif; ?>
                </ul>
            </div>
        </div>
        
        <div class="status-bar">
            <span id="statusText">就绪</span>
            <div style="flex:1"></div>
            <button class="btn" id="reloadBtn">重新加载列表</button>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const video = document.getElementById('videoPlayer');
            const loadingIndicator = document.getElementById('loadingIndicator');
            const statusText = document.getElementById('statusText');
            const reloadBtn = document.getElementById('reloadBtn');
            const channelItems = document.querySelectorAll('.channel-item');
            
            let hls = null;
            let currentChannel = null;
            
            // 初始化播放器
            function initPlayer() {
                if (Hls.isSupported()) {
                    hls = new Hls();
                    hls.on(Hls.Events.MANIFEST_PARSED, function() {
                        statusText.textContent = '正在播放: ' + (currentChannel ? currentChannel.textContent : '');
                    });
                    
                    hls.on(Hls.Events.ERROR, function(event, data) {
                        console.error('播放错误:', data);
                        if (data.fatal) {
                            statusText.textContent = '播放错误: ' + data.details;
                            
                            // 尝试恢复播放
                            if (data.type === Hls.ErrorTypes.NETWORK_ERROR) {
                                statusText.textContent = '网络错误，正在重试...';
                                setTimeout(() => loadChannel(currentChannel), 2000);
                            } else {
                                hls.destroy();
                            }
                        }
                    });
                } else if (video.canPlayType('application/vnd.apple.mpegurl')) {
                    // 原生HLS支持 (Safari)
                    video.addEventListener('loadedmetadata', function() {
                        statusText.textContent = '正在播放: ' + (currentChannel ? currentChannel.textContent : '');
                    });
                } else {
                    statusText.textContent = '错误: 您的浏览器不支持播放m3u8视频';
                }
            }
            
            // 加载频道
            function loadChannel(channelElement) {
                if (!channelElement || !channelElement.dataset.url) return;
                
                // 更新UI
                channelItems.forEach(item => item.classList.remove('active'));
                channelElement.classList.add('active');
                currentChannel = channelElement;
                
                const url = channelElement.dataset.url;
                statusText.textContent = '正在加载: ' + channelElement.textContent;
                loadingIndicator.style.display = 'flex';
                
                // 播放视频
                if (hls) {
                    hls.destroy();
                    hls.loadSource(url);
                    hls.attachMedia(video);
                    video.play().catch(e => {
                        console.error('自动播放失败:', e);
                        statusText.textContent = '点击播放按钮开始播放';
                    });
                } else if (video.canPlayType('application/vnd.apple.mpegurl')) {
                    video.src = url;
                    video.play().catch(e => {
                        console.error('自动播放失败:', e);
                        statusText.textContent = '点击播放按钮开始播放';
                    });
                }
                
                // 隐藏加载指示器
                video.addEventListener('canplay', function() {
                    loadingIndicator.style.display = 'none';
                });
            }
            
            // 事件监听
            channelItems.forEach(item => {
                item.addEventListener('click', function() {
                    loadChannel(this);
                });
            });
            
            reloadBtn.addEventListener('click', function() {
                statusText.textContent = '重新加载频道列表...';
                setTimeout(() => {
                    window.location.reload();
                }, 1000);
            });
            
            // 窗口控制按钮
            document.querySelectorAll('.window-btn')[0].addEventListener('click', function() {
                document.querySelector('.window').style.display = 'none';
            });
            
            document.querySelectorAll('.window-btn')[2].addEventListener('click', function() {
                if (confirm('确定要关闭播放器吗？')) {
                    window.close();
                }
            });
            
            // 初始化
            initPlayer();
            
            // 自动播放第一个频道
            if (channelItems.length > 0 && channelItems[0].classList.contains('active')) {
                loadChannel(channelItems[0]);
            }
        });
    </script>
</body>
</html>
