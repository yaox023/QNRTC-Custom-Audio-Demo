# Custom Audio Track in Qiniu RTC

逻辑分为下面几步：
- 加入房间
- 监听远端 track 发布
- 订阅该 track（音频）
- 从该 track 创建音频数据 sourceNode
- sourceNode 连接 scriptNode
- scriptNode 中做逻辑（详细见代码注释）
- scriptNode 连接 destination
- destination 中拿到输出 track
- 根据输出 track 创建 Qiniu custom track
- track 发布到房间