# 清华日报与紫荆码填报

当前填报情况： [![Daily Report](../../actions/workflows/daily.yml/badge.svg?event=schedule)](../../actions/workflows/daily.yml)
[![Zijing Code Report](../../actions/workflows/zijing_code.yml/badge.svg?event=schedule)](../../actions/workflows/zijing_code.yml)

---

## 声明

**本项目仅是为了免除重复申报【健康状态正常的数据】的繁复操作。当你的身体出现不适时，请立即停止所有的定时任务 (Actions 里点击 `Disable workflow`) 并如实向辅导员反馈你的身体状况。使用者造成的任何后果与本项目无关！**

## 简介

**学生每日健康和出行情况报告** + **紫荆码体温** 定时填报脚本。

整合自以下项目：

> [xmk2222/TsinghuaDailyReport](https://github.com/xmk2222/TsinghuaDailyReport)
>
> [Konano/report_temp.py](https://gist.github.com/Konano/b1576acfe61e0fdf2b3b60ab535ef6ae)

## 使用方式

建议使用第二种方式，简单易行.

### a. 计划任务

- pip install -r requirements.txt
- 配置 conf.ini 输入清华 info 用户名与密码
- python report.py
- python report_zijing_code.py
- 创建定时任务 Windows/Linux
  > [Windows 创建定时任务](https://www.cnblogs.com/wensiyang0916/p/5773828.html)

### b. GitHub Actions

> 如果你没有服务器，或者自己电脑也不能保证都开启，那么使用 GitHub Actions 可以作为你的服务器，并且非常安全。

- 创建 GitHub 账户
- fork 该仓库
- 在 fork 的仓库页面，进入 Settings -> Secrets-> 添加 USER_NAME 与 USER_PASS 为你的清华账号的用户名与密码
  ![添加Secrets](results/c.png)
- **注意 fork 的仓库的 GitHub Actions 是默认禁用的，需要进入 Actions 手动打开。** 成功启用后，本文档顶部的 badge 方可正常显示。

说明:
- Github Actions 的配置文件 (`.github/workflows` 下的 `daily.yml` 和 `zijing_code.yml`) 中分别配置了日报和紫荆码的填报时间，届时（实测会比设定时间晚几十分钟）会自动运行。
- 本文档顶部的 badge 显示了当前的填报情况（新 fork 的仓库尚未执行过填报任务，显示 `no status` 为正常现象）

## 效果

- ![效果图1](results/a.png)
- ![效果图2](results/b.png)
- 假装这里还有个紫荆码的效果图...
