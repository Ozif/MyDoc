# [WakeLock 锁](https://github.com/Ozif/time)使用说明

## 1. 啥是 WakeLock 锁？ 🤔
WakeLock 是浏览器提供的一个 API，用来防止设备屏幕自动休眠。简单说就是能让你的网页保持屏幕常亮，特别适合需要长时间展示内容的场景（比如这个时钟应用）。

## 2. 代码实现 🔧
在 <mcfile name="index.html" path="c:\Users\flykid\Desktop\time-main\index.html"></mcfile> 中已经实现了 WakeLock 功能：

```javascript:c:\Users\flykid\Desktop\time-main\index.html
// 获取 WakeLock 锁的函数
async function acquireScreenWakeLock() {
    try {
        // 请求屏幕唤醒锁
        const wakeLock = await navigator.wakeLock.request('screen');
        alert('Screen Wake Lock is ok:');
    } catch (error) {
        // 错误处理
        alert('Error acquiring Screen Wake Lock');
    }
}

// 调用函数
acquireScreenWakeLock();
```

## 3. 使用说明 📝
1. **浏览器支持**：目前 Chrome、Edge 等基于 Chromium 的浏览器支持
2. **权限要求**：需要 HTTPS 环境或 localhost 才能使用
3. **自动释放**：当用户切换标签页或最小化浏览器时，锁会自动释放
4. **手动释放**：可以调用 `wakeLock.release()` 手动释放

## 4. 注意事项 ⚠️
1. 这玩意儿必须用在正经地方，别瞎搞！🙅‍♂️
2. 长时间占用 WakeLock 可能会影响设备电池寿命
3. 记得做好错误处理，不是所有浏览器都支持

## 5. 扩展功能 💡
如果想更高级的控制，可以监听锁的状态变化：

```javascript
wakeLock.addEventListener('release', () => {
    console.log('Wake Lock 被释放了！');
});
```