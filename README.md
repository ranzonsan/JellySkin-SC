# JellySkin-SC

### 拥有大量动画、活力十足的极简主义Jellyfin CSS主题。

### 适配简繁中文、日语和韩语。

### 一切的功劳来自于@prayag17及其他原仓库开发者们，向无私奉献的开发者们致敬。All the contributions are from @prayag17 and other developers. Respect to those selfless developers.

# ℹ️ 使用方法

- 将以下代码粘贴至"设置->控制台->常规->自定义CSS代码"中，然后点击保存，JellySkin会在几分钟内自动应用，并覆盖所有用户的自定义CSS。如果要停止使用JellySkin，清除“自定义CSS代码”然后点击保存即可。

  注意：JellySkin可能不会在使用Nginx反向代理时正常应用。你可以滚动至页面下方查看解决方法。

  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/main.css");
  ```
- 若要启用剧集和电影的Logo图像，请将以下代码附加在下一行:

  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/logo.css");
  ```

# 🧩 附加内容

- ## 提高性能
- ### 移除背景滤镜

  附加以下代码，移除背景的毛玻璃效果。


  ```
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/improvePerformance/removeBackdropFilter.css");
  ```
- ### 移除顶栏特效

  附加以下代码，移除顶部菜单的渐变虚化效果。


  ```
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/improvePerformance/removeFadingScroll.css");
  ```
- ## 紧凑型海报

  Want to use compact posters instead of normal cards, add this to your custom css:

  若要将普通卡片替换为紧凑型海报（墙），请附加以下代码。


  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/compactPosters.css");
  ```

  实例:![image](https://user-images.githubusercontent.com/55829513/200132447-5307c19f-97e5-4022-ab42-c5b8bf632d6b.png)

  > 警告：在某些尺寸的屏幕上显示时，其显示效果可能不尽如人意。
  >
- ## 可水平滚动的“我的媒体”

  附加以下代码，将水平滚动的“我的媒体”（初始主题样式）带回JellySkin。


  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/horizontalMyMedia.css");
  ```
- ## 使用或切换不同的渐变色

  附加以下代码，更改主题渐变色：


  > **注意**：请务必将此更改渐变色代码置于main.css代码的下方。此代码不会更改登录界面的背景颜色。
  >

  - ### Mauve-鱼鳍紫红


    ```css
    @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/gradients/mauve.css");
    ```

    示例：![image](https://user-images.githubusercontent.com/55829513/200132732-d188392a-5642-47f7-bb62-f204a85d992e.png)
  - ### NightSky-午夜极光


    ```css
    @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/gradients/nightSky.css");
    ```

    示例：![image](https://user-images.githubusercontent.com/55829513/200132808-5b02c8e9-29c1-4a6b-ad3c-514588cf717a.png)
  - ### Sea-静海深蓝


    ```css
    @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/gradients/sea.css");
    ```

    示例：![image](https://user-images.githubusercontent.com/55829513/200132840-984deaf3-c228-4092-be8f-44c325d57782.png)
  - ### 自定义

    如果你想添加自定义渐变色：


    ```css
    :root {
      --accent1-light: YOUR ACCENT COLOR 1(LIGHTER SHADE);
      --accent1-dark: YOUR ACCENT COLOR 1(DARKER SHADE);
      --accent1-light-opacity1: YOUR ACCENT COLOR 1(WITH OPACITY 0.4);
      --accent2-light: YOUR ACCENT COLOR 2(LIGHTER SHADE);
      --accent2-dark: YOUR ACCENT COLOR 2(DARKER SHADE);
    }
    ```

# 💻 主题截图

- ### 登录界面

  ![Login_Page](https://github.com/prayag17/JellySkin/assets/55829513/9ca0d0c2-9ada-4e41-93b9-e4281be20d1d)
- ### 主页

  ![Home Screen](https://user-images.githubusercontent.com/55829513/200134098-6463a6e7-95bb-4af6-a451-b6ac5ef7abad.png)
- ### 媒体库

  ![LibView](https://user-images.githubusercontent.com/55829513/200133209-413d6e6c-3569-4aaf-9db7-f576c141f519.png)
- ### 带Logo的详情页

  ![TitleView](https://user-images.githubusercontent.com/55829513/200133240-075f604d-ae7f-48cb-9a42-445d8f3ef427.png)
- ### 剧集总览

  ![EpisodeView](https://user-images.githubusercontent.com/55829513/200133258-4eabfc3d-475f-4b42-a496-bc2de60c11a5.png)
- ### 设置

  ![SettingsView](https://user-images.githubusercontent.com/55829513/200133273-3ff7ba73-bad2-4f7c-88b1-e8298d246587.png)
- ### 控制台

  ![DashboardView](https://user-images.githubusercontent.com/55829513/200133302-5d7e7ac1-201b-4cb4-a839-ee53c5c6a6f2.png)
- ### 弹窗

  ![DialogView](https://user-images.githubusercontent.com/55829513/200133331-ee7838d0-6318-4175-b969-c06647bf65a0.png)

# ❓ 常见问题及修复方法

- ### Firefox浏览器看不见模糊背景效果。

  此段不作翻译，若有需要请看[原仓库英文](https://github.com/prayag17/JellySkin/tree/master?tab=readme-ov-file#unable-to-see-blured-background-in-firefox)。
- ### 启用 `logo.css` 后，Logo仍不可见。

  媒体库元数据获取问题。一般地，TMDB上包含绝大多数媒体的Logo，请检查媒体库元数据获取来源是否设置有误。
  此段不作翻译，若有需要请看[原仓库英文](https://github.com/prayag17/JellySkin/tree/master?tab=readme-ov-file#logos-are-not-visible-even-with-logocss)。
- ### 无背景。

  - 在 设置->显示 中勾选 `背景` 选项。
- ### 解决Nginx反向代理问题。

  此段不作翻译，若有需要请看[原仓库英文](https://github.com/prayag17/JellySkin/tree/master?tab=readme-ov-file#fix-for-nginx-reverse-proxy)。
- ### 如何反馈问题或提出改进建议?

  - 由于SC版本仅更改了fontfamily，未更改其他任何代码。若有相关建议请前往原仓库issues区 [https://github.com/prayag17/JellySkin/issues](https://github.com/prayag17/JellySkin/issues) 提出。
  - 点击 `New Issue` 按钮。
  - 选择适当的模板。
- ### 如何做出贡献？

  - Fork**原仓库。**
  - 添加补丁或新功能。
  - 发起pull request。
