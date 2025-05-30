# [O-tab](https://github.com/Ozif/O-tab) - 优雅的浏览器起始页

## 🌟 项目特点
- 极简设计：清爽的时间显示 + 磨砂玻璃效果搜索框
- 动态背景：内置芙宁娜主题动态视频背景（亮度自动调节）
- 防呆设计：自动解决浏览器重复打开页面的问题
- 高效开发：核心页面人工手写，插件部分AI生成（总耗时4小时）

## 🛠️ 安装指南

### 常规安装
1. 解压下载的压缩包（废话，能看到这个说明你已经解压了 😏）
2. 打开Chrome浏览器，地址栏输入：
   ```
   chrome://extensions
   ```
3. 开启右上角 **开发者模式**（那个小开关往右扒拉就完事了）
4. 点击 **加载已解压的扩展程序**，选择解压出来的`O-tab`文件夹

### 常见问题
- 报错不用管！这玩意儿作者也没系统学过插件开发，能跑就行 🤪
- 首次安装可能会问你要权限，直接点 **保持现状** 按钮

## 🎨 功能说明
- **智能时间显示**：精确到秒的本地化时间（自动适配中文环境）
- **Bing搜索集成**：输入内容直接跳转Bing搜索
- **防重复机制**：通过`background.js`确保只打开一个实例

## 🔧 自定义建议
1. 替换背景视频：把新视频放到`bgvideo`文件夹，改名为`芙宁娜furina.mp4`
2. 修改搜索引擎：编辑`index.html`第23行，改`action`属性值
3. 调整样式：修改`index.css`中的颜色和滤镜参数

## 📞 联系作者
- 作者：0Z1F（一个被Chrome逼疯的开发者）
- B站主页：[点击传送](https://space.bilibili.com/646734220)
- 特别声明：本插件完全免费，禁止倒卖！发现直接律师函警告 ⚠️

> 温馨提示：用着爽的话可以给作者点个Star，或者去B站三连支持下~ 谢谢！