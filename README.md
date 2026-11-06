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

## 如何发布 APK 并开启下载按钮

1. 从私有 Bruce 仓库 Android GitHub Actions 获取最新版 **成功构建** 的 APK，并先在测试手机上验证。
2. 进入本公开仓库的 Releases → Draft a new release，创建标签 `v2.3.0`。
3. 上传真实 APK，建议重命名为 `LiangDian-v2.3.0.apk` 后发布。
4. 复制该 APK 在公开 Release Assets 中的**真实下载 URL**，用无痕浏览器测试能否下载。
5. 将 `config.js` 中的 `apkUrl: ""` 替换为真实 URL，提交后网站下载按钮才会启用。

例如，若确实存在同名 Release asset，它的 URL 可能是：

`https://github.com/zonglianpan-commits/-LiangDian-Download/releases/download/v2.3.0/LiangDian-v2.3.0.apk`

不要在未上传 APK 前填写这一 URL；网站会将按钮保持为「APK 尚未发布」。

## 注意

- 原 Android 工程没有公开；只公开了这个网站的静态 HTML/CSS/JS 和图标。
- 网站不负责 APK 编译、签名与上传。
- 公共分发前建议构建并测试正式签名 APK，不建议直接长期分发调试签名版本。
- 若新 APK 使用了另一签名证书，可能无法覆盖原版安装。需要安全地备份已有配置。
- 应用使用无障碍服务，不代表能绕过手机的受限设置保护。
