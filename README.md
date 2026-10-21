# tiaoji_Monitor
调剂监控。QQ发送。

配置写在 `.env`（参考 `.env.example`）：`TARGET_QQ` / `SERVER_IP` / `LANGBOT_PORT` / `NAPCAT_TOKEN`。
NapCat 与脚本同机时 `SERVER_IP` 留默认 `127.0.0.1`，没设 HTTP 鉴权就 `NAPCAT_TOKEN` 留空。

## 相关项目

「任务完成后推一条 QQ 提醒」的通用能力（供 Qoder / WorkBuddy / DeepSeek harness 等 agent 调用的
CLI 与 skill 封装）已独立成 [ChangAkira/qq-notify](https://github.com/ChangAkira/qq-notify)。
本仓库只保留高校研招网监控，`monitor.py` 里的 `send_qq_msg` 是它自己的推送逻辑。
