# micro-os
用rust从零开始编写

参照文章：

1. https://zhuanlan.zhihu.com/p/53064186

2. https://zhuanlan.zhihu.com/p/56433770

# 准备工作

1. 切换rust版本

```bash
rustup override add nightly
```
2. 安装Rust的源代码
如果需要自主build std ，基本库则需要安装rust-src，移除.cargo/config
```bash
rustup component add rust-src
```

3. 安装xbuild(可选)

如果需要自主build std ，基本库则需要安装xbuild，移除.cargo/config
```
[unstable]
build-std = ["core", "compiler_builtins"]
```

```bash
cargo install cargo-xbuild
````

4. 安装bootimage 

注意bootimage要和```bootloader``` 版本对应

```bash
cargo install bootimage 
```