# dog

Tiny Core Linux 15.0 中文迷你图形系统（100 MB raw 磁盘镜像）。

- **在线体验**：<https://etqwfd.github.io/dog/> （浏览器内 v86 模拟器直接启动）
- 系统：Tiny Core Linux 15.0（x86），中文 locale（zh_CN.UTF-8）+ 图形桌面（Xvesa + FLWM）+ 文泉驿中文字体，开机自动进入中文桌面（rxvt 中文终端）。
- 本地 QEMU 启动：`qemu-system-i386 -drive file=dog.img,format=raw,if=ide -m 512`
- 文件：
  - `dog.img` —— 100 MB 原始磁盘镜像（SYSLINUX 引导 + FAT16 + Tiny Core）
  - `dog.img.zst` —— 镜像的 zstd 压缩版（约 43 MB，网页默认加载，边下边启动）
  - `index.html` + `v86.js` / `v86.wasm` / `seabios.bin` / `vgabios.bin` —— 网页模拟器（v86）

页面支持：
- 点击屏幕进入虚拟机（鼠标锁定），按 **Ctrl+Alt** 释放鼠标。
- 把本机文件**拖进**模拟器窗口 → 自动挂载为软驱 A:（系统内 `mount /dev/fd0 /mnt` 查看）。
