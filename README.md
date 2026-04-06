# Simple Su Brute-forcer

一个专为 Linux 环境设计的轻量级本地账户暴力破解脚本。

## 🚀 功能特性

* **极高兼容性**：完美兼容 **Alpine Linux** 和 **BusyBox** 环境（仅依赖 `sh`, `su`, `timeout`, `wc`）。
* **轻量级**：纯 Shell 脚本，无 Python/Go 等运行时依赖。
* **进度实时显示**：动态刷新当前尝试的进度 `[已尝试/总数]`。
* **并发加速**：内置简单的并发处理逻辑，每 16 组尝试进行一次同步。

## 🛠️ 使用方法

### 1. 准备
确保脚本具有执行权限，并准备好密码字典（如 `pass.txt`）。

```bash
chmod +x brute.sh
```

### 2. 执行
脚本接受两个可选参数：`用户名` 和 `字典路径`。

```bash
# 默认: 用户 root, 字典 dict.txt
./brute.sh

# 自定义参数
./brute.sh myuser my_passwords.txt
```