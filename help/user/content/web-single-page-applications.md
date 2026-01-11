---
title: 单页应用程序
description: 为单页应用程序(SPA)创建Web体验 — 在Journey Optimizer B2B edition中配置视图跟踪、处理动态内容和管理客户端导航。
feature: Channels, Personalization
role: User
badgeBeta: label="Beta 版" type="informative" tooltip="此功能当前为有限测试版"
source-git-commit: e50b6830736bf763d3aae6a58595e868bbac36e0
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# 单页应用程序

单页应用程序(SPA)可动态更新页面内容而无需重新加载整页，因此它们给Web个性化带来了独特的挑战。 Journey Optimizer B2B edition提供了专用工具来有效处理SPA个性化。

## 了解SPA

传统的多页面网站每次导航都会触发整个页面加载，而SPA会使用JavaScript动态更新内容，同时维护单个HTML页面。 此方法为Web体验创建了几个注意事项：

* **无页面重新加载** — 内容发生更改时不会触发传统的页面加载事件。
* **虚拟视图** - SPA中需要作为单独页面跟踪的不同&#x200B;_视图_&#x200B;或&#x200B;_屏幕_。
* **客户端路由** - JavaScript路由器(如React Router、Vue Router和Angular Router)处理导航而不是服务器请求。
* **动态DOM** — 页面元素可在初始页面加载后创建、修改或删除。

## 配置SPA支持

为了有效地个性化SPA，您需要配置视图跟踪，以便Journey Optimizer B2B edition能够识别用户在虚拟视图之间导航的时间。

### 设置查看声明

与开发团队合作，使用Adobe Web SDK实施视图声明。 使用这些视图声明涉及在SPA导航到新视图时调用包含视图信息的`sendEvent`命令。

**示例实施：**

```javascript
// When a new view is rendered in your SPA
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webPageDetails": {
        "viewName": "product-detail",
        "URL": window.location.href
      }
    }
  },
  "data": {
    "__adobe": {
      "target": {
        "viewName": "product-detail"
      }
    }
  }
});
```

### 查看命名约定

使用与应用程序的逻辑结构匹配的一致描述性视图名称：

| 视图 | 示例名称 |
| ---- | ------------ |
| 主页 | `home` |
| 产品列表 | `product-list` |
| 产品详细信息 | `product-detail` |
| 购物车 | `cart` |
| 结帐 | `checkout` |
| 帐户信息板 | `account-dashboard` |

>[!NOTE]
>
>视图名称区分大小写。 在您的实施中使用一致的命名约定（建议使用带连字符的小写）。

## 为SPA创建Web体验

在创建SPA Web体验时，请考虑以下最佳实践：

### Target特定视图

* 在[Web渠道配置](../admin/configure-channels-web.md)中，设置与SPA路由结构一致的URL匹配规则。

* 创建修改时，请指定应用修改的视图。

* 使用以每个视图特定的元素为目标的CSS选择器。

### 处理动态内容

SPA通常在初始页面渲染后动态加载内容。 可使用以下技术确保正确应用修改：

#### 等待元素

配置修改以等待目标元素存在后再应用：

1. 在非可视编辑器中，使用CSS选择器添加修改。

1. 启用&#x200B;**[!UICONTROL 等待元素]**&#x200B;并指定最长等待时间。

1. 一旦目标元素出现在DOM中，修改即适用。

#### 使用突变观察器

对于高度动态的内容，Web SDK包含内置的变异观察器，可检测何时将新元素添加到页面。 这些观察者可确保即使异步加载元素时也会应用修改。

### SPA框架

Journey Optimizer B2B edition Web体验可与流行的SPA框架配合使用：

| 框架 | 注意事项 |
| --------- | -------------- |
| **React** | 在React将组件呈现到DOM后会应用修改。 使用类名或数据属性进行定位。 |
| **Angular** | Angular更改检测运行后的Target元素。 避免在呈现元素之前使用`*ngIf`来定位元素。 |
| **Vue.js** | 等待Vue的`nextTick`，以确保元素位于DOM中。 使用引用或自定义属性以实现稳定定位。 |
| **Next.js / Nuxt.js** | 对于SSR/SSG页面，请确保在预期修改之前完成Web SDK水合。 |

## SPA个性化的最佳实践

### 使用稳定的选择器

SPA通常会生成动态类名或ID（特别是对于CSS-in-JS解决方案）。 作为替代方法，您可以使用：

* **数据属性** — 将自定义数据属性（`data-testid`、`data-section`等）添加到要定位的元素。
* **语义HTML** — 基于HTML结构和语义元素的Target。
* **ID属性** — 尽可能使用稳定的ID属性。

**示例：**

```html
<!-- Instead of targeting dynamic class names -->
<button class="css-1a2b3c4d">Sign Up</button>

<!-- Add a stable data attribute -->
<button class="css-1a2b3c4d" data-action="signup">Sign Up</button>
```

**CSS选择器：** `[data-action="signup"]`

### 测试视图

测试SPA Web体验时：

1. 浏览所有应用修改的视图。

1. 测试完整的用户流，包括：
   * 直接导航到视图（深层链接）
   * 从SPA内的其他视图导航
   * 浏览器向后和向前导航

1. 验证在返回到先前访问的视图时重新应用修改。

### 处理视图过渡

某些SPA使用视图之间的动画或过渡。 请考虑：

* **计时** — 确保在过渡动画完成后应用修改。
* **元素可见性** — 元素可能存在，但在转换期间是隐藏的。
* **闪烁** — 尽早应用修改以避免可见的内容更改。

## 故障排除

在查看SPA设计更改时，请使用以下建议来解决一些常见问题：

* **未显示修改** — 如果修改未显示在SPA上：

   1. **检查视图跟踪** — 验证`sendEvent`调用是否包含正确的视图名称。

   1. **验证元素是否存在** — 应用修改时，请确保目标元素位于DOM中。

   1. **查看选择器** — 确认CSS选择器与实际的DOM结构匹配。

   1. **检查控制台** — 查找可能阻止修改的JavaScript错误。

* **修改会短暂出现然后消失** — 此问题通常发生在SPA重新渲染并替换修改的元素时：

   1. 使用在渲染中保持稳定的更具体的CSS选择器。

   1. 使变异观察器在重新创建元素时重新应用修改。

   1. 与开发团队合作，向目标元素添加稳定属性。

* **重复修改** — 如果修改出现多次：

   1. 选中每个视图过渡仅触发一次视图跟踪事件。

   1. 验证修改是否限定在特定视图的范围内，而不是全局应用。

## 相关主题

* [Web体验概述](./web-experiences.md)
* [Web体验设计](./web-experience-design.md)
* [Web渠道配置](../admin/configure-channels-web.md)