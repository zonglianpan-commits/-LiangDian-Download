# 靓点连点器 Android 下载官网

这是靓点连点器的 **独立公开下载网站**，源代码工程仍保存在私有仓库 Bruce 中。

## 访问地址

仓库名称以连字符开头，URL 中必须保留：

https://zonglianpan-commits.github.io/-LiangDian-Download/

页面仅在 GitHub Pages 启用并部署成功后生效。

## 如何启用 GitHub Pages

1. 打开仓库 Settings → Pages。
2. 在 Build and deployment 中，Source 选择 **Deploy from a branch**。
3. Branch 选 **main**，Folder 选 **/(root)**，点击 Save。
4. 等 Pages 部署后访问上述网站，建议用匿名浏览器确认可以正常打开。

## 如何发布 APK 并自动启用下载按钮

1. 在私有仓库 Bruce 的 Android Actions 里选择最新**成功**构建，下载 `AutoTap-debug-apk` ZIP，解压获得 `app-debug.apk`，并在测试手机验证它确实能运行。
2. 在本公开仓库打开 [Releases](https://github.com/zonglianpan-commits/-LiangDian-Download/releases) → `Draft a new release`，建立版本标签（如 `v2.3.0`）。
3. 将真实 APK 上传到 Release Assets，建议文件名 `LiangDian-v2.3.0.apk`；填好说明，点击 **Publish release**（不要保留 Draft 或标记为 Prerelease）。
4. 网站会通过 GitHub 公开 API **自动识别最新正式 Release 的 .apk 文件**并启用下载按钮。无需修改 `config.js`。
5. 用未登录 GitHub 的浏览器打开网站并下载验证。

如果确实需要手动指定 APK 链接，可在 `config.js` 的 `apkUrl` 填写已发布 APK 的 HTTPS 下载网址。未发布前保持空字符串，按钮自动禁用。

## 注意

- 原 Android 工程没有公开；只公开了这个网站的静态 HTML/CSS/JS 和图标。
- 网站不负责 APK 编译、签名与上传。
- 公共分发前建议构建并测试正式签名 APK，不建议直接长期分发调试签名版本。
- 若新 APK 使用了另一签名证书，可能无法覆盖原版安装。需要安全地备份已有配置。
- 应用使用无障碍服务，不代表能绕过手机的受限设置保护。
