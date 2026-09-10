物值 PWA v1.0

这是从“物值”HTML 原型改成的第一版 PWA。

已经完成：
1. 可安装的 manifest
2. Service Worker 离线缓存
3. IndexedDB 本地数据库（替代 localStorage）
4. 尝试申请浏览器持久化存储
5. 桌面/安卓 PWA 安装入口
6. 独立窗口 + 应用图标
7. 保留 CSV 导入导出、JSON 完整备份恢复
8. 保留浅色绿色主题与黑白深色主题

重要：
- 直接双击 index.html（file://）时，Service Worker/PWA 安装不会正常工作。
- PWA 需要通过 localhost 或 HTTPS 打开。
- 真正放到安卓手机安装，推荐下一步部署到 GitHub Pages。
- 资产数据保存在“当前浏览器 + 当前网站”的 IndexedDB 中，不会上传到网站服务器。
- 即使使用 IndexedDB，用户主动“清除该网站全部数据”仍可能删除数据库，所以 JSON 备份仍然重要。

电脑本地测试（如果电脑有 Python）：
  进入本文件夹后运行：
  python -m http.server 8080

然后浏览器打开：
  http://localhost:8080

下一步建议：
部署到 GitHub Pages → 安卓 Chrome 打开网址 → 安装“物值”到桌面 → 测试完全离线使用。
