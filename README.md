# rendering-principles-of-the-browser
## 浏览器渲染原理与全链路性能优化

- Use HTTP/2 与HTTP/1.1相比，HTTP/2提供了许多优点，包括二进制报头和多路复用
- Defer offscreen images 考虑在所有关键资源加载完毕后延迟加载屏幕外和隐藏的图像
- Serve images in next-gen formats 提供下一代格式的图像
- Remove unused JavaScript 删除不必要的js
- Properly size images 节省图片资源大小
- Enable text compression 启用文本压缩
- Ensure text remains visible during webfont load 确保字体加载时可见
- Does not use passive listeners to improve scrolling performance  没有使用被动侦听器来提高滚动性能
- Image elements do not have explicit width and height 图片元素无宽高
- Serve static assets with an efficient cache policy 静态资源无缓存
- Minimize main-thread work 减少主线程的工作
- Background and foreground colors do not have a sufficient contrast ratio 背景和前景颜色没有足够的对比度
- <dl>'s do not contain only properly-ordered <dt> and <dd> groups, <script>, <template> or <div> elements dl中没有包含 dt dt
- <frame> or <iframe> elements do not have a title  iframe没有title
- Image elements do not have [alt] attributes 图片没有alt属性
- Heading elements are not in a sequentially-descending order 标题元素没有按顺序降序排列的
- <html> element does not have a [lang] attribute html没有语言属性
- [user-scalable="no"] is used in the <meta name="viewport"> element or the [maximum-scale] attribute is less than 5.   禁用缩放是有问题的
- Displays images with incorrect aspect ratio  显示宽高比不正确的图像