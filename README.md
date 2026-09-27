# dog

KolibriOS 可启动磁盘镜像（100 MB raw）。

- **在线体验**：<https://etqwfd.github.io/dog/> （浏览器内 v86 模拟器直接启动）
- 本地 QEMU 启动：`qemu-system-i386 -drive file=dog.img,format=raw,if=ide -m 256`
- 文件：
  - `dog.img` —— 100 MB 原始磁盘镜像（SYSLINUX 引导 + FAT16 + KolibriOS）
  - `dog.img.zst` —— 镜像的 zstd 压缩版（约 1.4 MB，供快速下载）
  - `index.html` + `v86.js` / `v86.wasm` / `seabios.bin` / `vgabios.bin` —— 网页模拟器（v86）
