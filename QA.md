# V28 QA

测试环境：Chromium Headless + SwiftShader，桌面 1440×900、移动端 390×844。由于当前沙盒阻止浏览器导航到 localhost / file URL，测试通过 `page.set_content()` 加载完整 HTML，并内嵌同一份地球纹理；应用代码和交互路径保持一致。

## 通过项目

| 检查 | 结果 |
|---|---|
| 页面加载与版本识别 | V28.0 |
| JavaScript 运行错误 | 0 |
| 控制台警告 | 0 |
| 自动恢复点 | 通过 |
| 手动创建检查点 | 通过 |
| 恢复旧版本 | 通过 |
| 删除恢复点 | 通过 |
| 隐藏路段检查与一键修复 | 通过 |
| Journey preflight 正常状态 | 通过 |
| 三个导出预设 | 通过 |
| Social vertical 参数 | 9:16 / 1080p / 30 FPS / Balanced |
| 帧数、文件大小与负载估算 | 通过 |
| Preview 进入与退出 | 通过 |
| 移动端导出窗口 | 底部操作可见 |
| 390px 横向溢出 | 0px |
| ZIP 完整性 | 通过 |

## 回归路径

1. 打开项目并确认默认三地点路线。
2. 打开 Version history，创建手动检查点。
3. 修改项目标题，自动创建新恢复点，再恢复旧版本。
4. 将路段设为 hidden，打开 Journey preflight，使用 Fix 改为 line only。
5. 打开 Export video，依次验证 Draft / Social vertical / Full HD。
6. 进入 Preview，验证播放与退出。
7. 在 390×844 视口验证编辑器和长导出窗口。
