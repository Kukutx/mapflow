# Mapflow V28

个人使用的旅行路线动画编辑器。V28 保持 V27 已校准的 Balanced 节奏、轻度点到点纵深和镜头曲线，重点完善版本恢复、项目检查与导出体验。

## 运行

推荐使用 Chrome 或 Edge：

```bash
python3 -m http.server 8080
```

然后打开 `http://localhost:8080`。也可直接打开 `index.html`，但本地服务器对纹理和浏览器编码兼容性更好。

Windows 可运行 `start_windows.bat`；macOS / Linux 可运行：

```bash
chmod +x start_mac_linux.sh
./start_mac_linux.sh
```

## V28 新增

- 本地版本历史，自动保存最多 12 个恢复点。
- 手动创建、恢复和删除检查点。
- 大型照片项目自动使用“路线与设置恢复”，防止浏览器存储超限。
- Journey preflight：检查地点数量、重叠地点、隐藏路段、标签重叠风险和高负载导出参数。
- 可直接执行修复：显示隐藏路段、开启标签避让、切换安全导出设置等。
- Draft、Social vertical、Full HD 三个导出预设。
- 导出前显示帧数、预计文件大小和浏览器负载。
- 移动端导出窗口改为内部滚动，底部操作始终可见。
- Version history 与 Journey preflight 同时加入 Options → Project，手机端也可访问。

## 快捷键

- `Space`：播放 / 暂停
- `F`：显示完整路线
- `Ctrl/⌘ + Z`：撤销
- `Ctrl/⌘ + Shift + Z`：重做
- `Ctrl/⌘ + Shift + H`：版本历史
- `I`：Journey preflight
- Preview 中 `J / K / L`：后退 5 秒 / 播放暂停 / 前进 5 秒
- Preview 中 `[ / ]`：上一地点 / 下一地点

## 文件

- `index.html`：完整单文件应用
- `earth-texture.jpg`：离线地球纹理
- `sample-preview.mp4`：示例成片
- `QA.md`：交互回归结果
- `PERFORMANCE.md`：性能检查结果
