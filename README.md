# Pepper Extreme Distribution Company Website

这是 Pepper Extreme Distribution Company (PPR) 的企业网站代码，参考BSS Distribution网站风格设计。

## 网站结构

- `index.html` - 首页
- `distribution.html` - 代理品牌页面
- `about.html` - 关于我们页面
- `contact.html` - 联系方式页面
- `styles.css` - 样式表
- `script.js` - JavaScript脚本
- `images/` - 图片文件夹

## 如何自定义

### 添加公司和品牌Logo

1. 在HTML文件中搜索 `<!-- Logo placeholder - will be replaced -->` 注释，将其替换为公司Logo图片：

```html
<div class="logo-container">
    <a href="index.html">
        <img src="images/ppr-logo.png" alt="PPR Logo" class="logo">
    </a>
</div>
```

2. 在品牌展示部分，替换占位符为实际品牌Logo：

```html
<div class="brand-logo">
    <img src="images/thehash-logo.png" alt="TheHash Logo">
</div>
```

### 添加背景图片

1. 将所需图片添加到 `images/` 文件夹。
2. 更新CSS中的背景图片路径，例如：

```css
.hero {
    background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('images/hero-bg.jpg');
}
```

### 添加产品图片

在`distribution.html`页面中，将品牌Logo占位符替换为实际Logo：

```html
<div class="brand-image">
    <img src="images/fox-products.jpg" alt="FOX产品">
</div>
```

### 添加团队照片

在`about.html`页面中，替换团队照片占位符：

```html
<div class="team-photo">
    <img src="images/team-member1.jpg" alt="张明照片">
</div>
```

### 添加地图

在`contact.html`页面中，替换地图占位符为实际地图嵌入代码：

```html
<div class="map-container">
    <iframe src="https://maps.google.com/maps?q=上海市静安区南京西路1788号&t=&z=15&ie=UTF8&iwloc=&output=embed" frameborder="0" style="width: 100%; height: 400px;" allowfullscreen></iframe>
</div>
```

## 联系表单配置

要使联系表单功能正常工作，您需要添加后端处理逻辑。目前，表单只有一个简单的前端验证，提交后会显示一个感谢消息，但不会发送数据。

要连接到实际后端：

1. 在`contact.html`中更新表单的action属性：

```html
<form id="contactForm" action="your-backend-endpoint" method="post">
```

2. 根据需要修改JavaScript处理代码。

## 颜色主题修改

主要颜色在`styles.css`中定义，您可以修改颜色代码来匹配您的品牌色彩：

- 主色：`#e74c3c`（红色）
- 背景色：`#f8f8f8`（浅灰色）
- 文本色：`#333`（深灰色）

## 注意事项

- 网站已针对移动设备进行了响应式设计
- 对于生产环境，建议压缩CSS和JavaScript文件以提高性能
- 添加适当的SEO元标签和分析跟踪代码 