# JellySkin-SC

### 人性化的Jellyfin CSS主题。

### 适配简繁中文、日语和韩语。This repo is just adapted to Chinese, Japanese and Korean.

### Fork自@prayag17。Forked from @prayag17.
### 已合并v12.5.0代码，适配Jellyfin 10.9.x

# ℹ️ 使用方法

> [!important]
> JellySkin需要Chrome 105、Edge 105、Safari 15.4、Firefox 121、Opera 91及以上版本和其他支持基线（Baseline）2023 css功能的浏览器以正常显示。

- 将以下代码粘贴至"设置->控制台->常规->自定义CSS代码"中，然后点击保存，JellySkin会在几分钟内自动应用，并覆盖所有用户的自定义CSS。如果要停止使用JellySkin，清除“自定义CSS代码”然后点击保存即可。

<b>注意：JellySkin可能不会在使用Nginx反向代理时正常应用。你可以滚动至页面下方查看解决方法。

  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/main.css");
  ```
- 若要启用剧集和电影的Logo图像，请将以下代码附加在下一行:

  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/logo.css");
  ```
- 由于jsdelivr在中国大陆的链接性较差，如果在正确添加代码后仍然没有任何改变，你可以自行使用其他cdn。——译者注
- 此中文适配版不会发布在年久失修的Jellyfin Skin Manager上。——译者注
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
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/improvePerformance/removeBackdropFilter.css");
  ```
- ## 紧凑型海报

  Want to use compact posters instead of normal cards, add this to your custom css:

  若要将普通卡片替换为紧凑型海报（墙），请附加以下代码。


  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/compactPosters.css");
  ```

  示例:
![image](https://user-images.githubusercontent.com/55829513/200132447-5307c19f-97e5-4022-ab42-c5b8bf632d6b.png)

  > 警告：在某些尺寸的屏幕上显示时，其显示效果可能不尽如人意。

- ## 可水平滚动的“我的媒体”

  附加以下代码，将水平滚动的“我的媒体”（初始主题样式）带回JellySkin。


  ```css
  @import url("https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/addons/horizontalMyMedia.css");
  ```
- ## 使用或切换不同的渐变色

  附加以下代码，更改主题渐变色：


  > **注意**：请务必将此更改渐变色代码置于main.css代码的下方。此代码不会更改登录界面的背景颜色。

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

  ![Home Page](https://github.com/prayag17/JellySkin/assets/55829513/075d844b-ca43-4f61-b54a-cb75110e77ed)
- ### 媒体库

  ![Library](https://github.com/prayag17/JellySkin/assets/55829513/c3ef8e48-df17-44f0-9708-e10dfa448237)
- ### 带Logo的详情页

  ![Title page](https://github.com/prayag17/JellySkin/assets/55829513/270bb0bb-a755-449d-a57d-9da4e31d6082)
- ### 剧集总览

  ![Episodes](https://github.com/prayag17/JellySkin/assets/55829513/eaded068-5930-47fd-b5d0-03cf89e1da44)

# ❓ 常见问题及修复方法

- ### Firefox浏览器看不见模糊背景效果。

  自 Firefox 70 版本后失效：此选项在 `layout.css.backdrop-filter.enabled` 和 `gfx.webrender.all` 选项均设置为打开（true）后可见。要在 Firefox 中更改首选项，请访问 `about:config`。

- ### 启用 `logo.css` 后，Logo仍不可见。

  这是媒体库元数据获取出错导致的问题。一般地，TMDB上包含绝大多数媒体的Logo，请检查媒体库元数据获取来源是否设置有误。
  如果默认设置下，大部分影片都没有Logo，可以尝试开启Fanart插件。
  - 获取 Fanart 插件。控制台 -> 插件 -> 目录
  - 在媒体库设置中启用 Fanart 作为库的元数据提供程序。控制台 -> 媒体库 -> 单击库上的 3 个点 -> 管理媒体库 -> 滚动以查找图片提供程序，并在所有媒体库中启用 Fanart。
  - 在缺少logo的剧集中，点击剧集内的三个点 -> 修改图片 -> 点击左上角的搜索图标 -> 类型选择商标 -> 勾选“所有语言” -> 选择喜欢的logo -> 点击下载图标，之后logo便会自动刷新。当然，你也可以重新扫描需要更新logo的剧集，不要忘记勾选“覆盖所有图片”选项。
  
  （译者注：原文第三步为更新所有媒体库，这是不必要的，只需下载logo或更新没有logo的剧集即可。）
- ### 无背景。

  - 在 设置->显示 中勾选 `背景` 选项。
- ### 解决Nginx反向代理问题。

  当使用 <a href="https://jellyfin.org/docs/general/networking/nginx.html">Jellyfin 文档</a> 中的 Nginx 反向代理默认配置时，该主题可能无法正常工作。（如果你使用的是 subpath 配置，则可以忽略以下内容。）
  此配置包括一个 CSP（内容安全策略），其标头不允许加载未在此处定义的外部内容。
  在 nginx 配置中，您应该添加通过“自定义 CSS 代码”框导入的所有 CSS 文件的 URL。将：
  ```shell
  add_header Content-Security-Policy "default-src https: data: blob: http://image.tmdb.org; style-src 'self' 'unsafe-inline'; script-src 'self' 'unsafe-inline' https://www.gstatic.com/cv/js/sender/v1/cast_sender.js https://www.youtube.com blob:; worker-src 'self' blob:; connect-src 'self'; object-src 'none'; frame-ancestors 'self'";
  ```
  更改为（仅添加默认样式）：
  ```shell
  add_header Content-Security-Policy "default-src https: data: blob: http://image.tmdb.org; style-src 'self' 'unsafe-inline' https://cdn.jsdelivr.net/npm/jellyskin-sc@latest/dist/main.css; script-src 'self' 'unsafe-inline' https://www.gstatic.com/cv/js/sender/v1/cast_sender.js https://www.youtube.com blob:; worker-src 'self' blob:; connect-src 'self'; object-src 'none'; frame-ancestors 'self'";
  ```
  如果不这样做，主题将根本无法加载（恢复为默认主题），浏览器控制台会报错。即使你粘贴了所有 CSS，字体仍然不会加载，因为它是从非法外部来源加载的。
- ### 如何反馈问题或提出改进建议?

  - 由于SC版本仅更改了fontfamily，未更改其他任何代码。若有相关建议请前往原仓库issues区 [https://github.com/prayag17/JellySkin/issues](https://github.com/prayag17/JellySkin/issues) 提出。
  - 点击 `New Issue` 按钮。
  - 选择适当的模板。
  
- ### 如何做出贡献？

  - Fork**原仓库。**
  - 添加补丁或新功能。
  - 对**原仓库。**发起pull request。
