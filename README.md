# valve-inspection-bot-updates

该仓库仅用于公开托管 `valve-inspection-bot` 在线更新所需的最小文件集，不包含源码。

## 目录说明

- `update.yaml`：客户端默认读取的更新元数据
- `stable/win-amd64/`：当前稳定版本的 Windows 更新文件
- `archive/vX.Y.Z/win-amd64/`：历史归档版本，用于回滚与追溯

## 发布来源

所有构建与发布均由私有主仓库 `Cody292/valve-inspection-bot` 的 GitHub Actions 完成；本仓库不需要 `windows-build.yml`。

## 回滚方式

优先回退根目录 `update.yaml` 到上一稳定版本；必要时再把 `stable/` 覆盖回对应归档版本。
