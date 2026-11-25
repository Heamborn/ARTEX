# norma（第三方依赖副本）

本目录是 `github.com/Autumn-27/norma` v0.4.3 的源码副本，由 `go.mod` 的 `replace` 指令引用：

```
replace github.com/Autumn-27/norma => ./third_party/norma
```

## 为什么要内置

`norma` 是 ARTEX 原作者自有的模块，提供 agent 运行时的底层能力（`agentcore` / `tool` / `permission` / `harness` / `memory` / `transcript`）。2026-10 原作者将 ARTEX 及其相关仓库一并下架，该模块不再有可维护的上游。

Go 模块代理仍能取到缓存副本，但缓存并非永久保证。内置一份源码后，本仓库的构建不再依赖上游是否可访问。

## 来源与校验

- 版本：v0.4.3
- 取自：Go module proxy 缓存副本 `proxy.golang.org/github.com/!autumn-27/norma/@v/v0.4.3.zip`
- `go.sum` 中的校验值：`h1:DnmOhJPL6OZSMnCVYO5Ujh4yVINuDarEickVi9jx1hI=`
- 内容未作任何修改

## 许可

上游副本未附带 LICENSE 文件，是否授权再分发无法从仓库本身判断。此处仅作为构建依赖留存，不主张任何额外权利。若权利人提出异议，删除本目录并将 `go.mod` 的 `replace` 指向其他可用来源即可，不影响仓库其余部分。

## 维护提示

升级该依赖时，替换本目录内容并同步 `go.mod` 中的版本号与 `go.sum`。`go.sum` 只在使用模块代理时才参与校验，`replace` 到本地路径后不再校验哈希，因此改动本目录内容不会被 `go mod verify` 发现——升级时请自行核对来源。
