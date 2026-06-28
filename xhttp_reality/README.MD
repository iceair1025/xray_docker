## xray_docker_xhttp_reality（已合并至 reality）

> ⚠️ **本镜像已停止独立维护。** 自 `reality` 镜像 0.1.0 起，xhttp 模式已整合进统一的 `wulabing/xray_docker_reality` 镜像

## 如何迁移

只需改用 `reality` 镜像并设置 `NETWORK=xhttp`，其余参数（UUID/DEST/SERVERNAMES/PRIVATEKEY/XHTTP_PATH）保持一致即可：

```
docker pull wulabing/xray_docker_reality:latest
docker run -d --name xray_xhttp_reality --restart=always --log-opt max-size=100m --log-opt max-file=3 \
  -p 443:443 -e NETWORK=xhttp \
  -v "./wulabing_xray_config:/data" \
  wulabing/xray_docker_reality:latest
```

旧的持久化文件（`xhttp_reality_state.json` / `xhttp_reality_config_info.txt`）会被新镜像自动兼容读取，连接信息保持不变。

完整使用说明请见 👉 [xray_docker_reality](https://github.com/wulabing/xray_docker/tree/master/reality)

## 捐赠

您可以使用我的 搬瓦工 AFF 购买 VPS

https://bandwagonhost.com/aff.php?aff=63939

您可以使用我的 JustMySocks AFF 购买搬瓦工提供的代理

https://justmysocks.net/members/aff.php?aff=17621

您可以使用我的 DMIT AFF 购买 VPS

https://www.dmit.io/aff.php?aff=3957

您可以使用我的 Vultr AFF 创建新的 Vultr 账号并使用

https://www.vultr.com/?ref=6881279

您可以使用我的 nube AFF 购买按量付费VPS

https://nube.sh/invite/5986088028ENM0

您可以通过 USDT 支持我，感谢您的支持
TRC20: TU8mLTPfa5Y9nmszyfyt2VRAtuZhdLexL8
