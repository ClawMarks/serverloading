<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>弹性布局背景页</title>
    <!-- 引入Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
        }
    </style>
</head>
<body class="min-h-screen flex flex-col m-0 p-0">
    <!-- 隐藏的音乐播放器 - 自动播放且无控制功能 -->
    <audio id="backgroundMusic" autoplay loop class="hidden">
        <!-- 这里使用示例音乐链接，实际使用时请替换为您自己的音乐文件 -->
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        您的浏览器不支持音频播放
    </audio>

    <!-- 主容器 - 弹性布局，仅包含背景图 -->
    <div class="flex-1 relative overflow-hidden">
        <!-- 背景图 - 占据整个屏幕 -->
        <div class="absolute inset-0 z-0">
            <img src="https://picsum.photos/id/1058/1920/1080" alt="自然风景背景图，有山脉、湖泊和森林" 
                 class="w-full h-full object-cover">
        </div>
    </div>

    <script>
        // 音乐播放逻辑 - 尝试自动播放
        document.addEventListener('DOMContentLoaded', function() {
            const audio = document.getElementById('backgroundMusic');
            
            // 尝试播放音乐，处理浏览器自动播放限制
            function tryPlayAudio() {
                audio.play().catch(error => {
                    console.log('自动播放需要用户交互:', error);
                    // 监听首次用户交互后再尝试播放
                    document.body.addEventListener('click', () => {
                        audio.play();
                    }, { once: true });
                });
            }
            
            // 初始尝试播放
            tryPlayAudio();
        });
    </script>
</body>
</html>
    
