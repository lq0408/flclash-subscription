# 上次构建失败：2026-11-28 15:03 UTC

```
运行环境: python 3.12.16 | Linux x86_64 | 工作目录 /home/runner/work/flclash-subscription/flclash-subscription
参数: workers=128 rounds=2 timeout=3000ms max_delay=3000ms 输出=out/flclash-free-nodes.yaml
[1/9] 复测上一版订阅（老节点优先）
  从 flclash-free-nodes.yaml 读到 60 个老节点，复测后上海 RTT ≤150ms 才保留
[2/9] 抓取节点源
  [ok]   alireza786786/V2RAY-BREACHING-THE-BARRIERS   1143 KB  (raw.githubusercontent.com)
  [ok]   alireza786786/V2RAY-BREACHING-THE-BARRIERS   1748 KB  (raw.githubusercontent.com)
  [ok]   Barabama/FreeNodes                       1023 KB  (raw.githubusercontent.com)
  [ok]   anaer/Sub                                 580 KB  (raw.githubusercontent.com)
  [ok]   looomix/Node-Configs                      621 KB  (raw.githubusercontent.com)
  [ok]   dongchengjie/airport                      717 KB  (raw.githubusercontent.com)
  [ok]   asgharkapk/Sub-Config-Extractor           917 KB  (raw.githubusercontent.com)
  [ok]   Au1rxx/free-vpn-subscriptions             601 KB  (raw.githubusercontent.com)
  [ok]   yy1588133/proxy-pool                      360 KB  (raw.githubusercontent.com)
  [ok]   10ium/VpnClashFaCollector                 214 KB  (raw.githubusercontent.com)
  [ok]   10ium/VpnClashFaCollector                1061 KB  (raw.githubusercontent.com)
  [ok]   asgharkapk/Sub-Config-Extractor           367 KB  (raw.githubusercontent.com)
  [ok]   yuan2pro/sub_merge                         31 KB  (raw.githubusercontent.com)
  [ok]   ts-sf/fly                                 244 KB  (raw.githubusercontent.com)
  [ok]   asgharkapk/Sub-Config-Extractor            45 KB  (raw.githubusercontent.com)
  [ok]   yuan2pro/sub_merge                         41 KB  (raw.githubusercontent.com)
  [ok]   clashnode.me                              138 KB  (clashnode.me/20261128)
  抓取完成: 成功 17 / 17，用时 1.1s
[3/9] 解析 / 清洗 / 去重
  10ium_VpnClashFaCollector__sub_final_all 新增   66
  10ium_VpnClashFaCollector__sub_final_all 新增  607
  Au1rxx_free-vpn-subscriptions__output_cl 新增  816
  Barabama_FreeNodes__nodes_merged.yaml.ya 新增 2468
  alireza786786_V2RAY-BREACHING-THE-BARRIE 新增 1938
  alireza786786_V2RAY-BREACHING-THE-BARRIE 新增 1163
  anaer_Sub__clash.yaml.yaml               新增 2001
  asgharkapk_Sub-Config-Extractor__output_ 新增  637
  asgharkapk_Sub-Config-Extractor__output_ 新增   13
  asgharkapk_Sub-Config-Extractor__output_ 新增  145
  daily_clashnode.me_20261128.yaml         新增   67
  dongchengjie_airport__subs_merged_tested 新增 1013
  looomix_Node-Configs__configs_clash_prox 新增 1142
  ts-sf_fly__clash.yaml                    新增  192
  yuan2pro_sub_merge__sub_merged_proxies_1 新增   60
  yuan2pro_sub_merge__sub_merged_proxies_2 新增   56
  yy1588133_proxy-pool__clash.yaml.yaml    新增  341
  已过滤开放/明文协议: http-plain/socks5
  去重后候选: 12785（用时 15.4s）
[4/9] 内核校验
  mihomo 版本: v1.19.34
  Mihomo Meta v1.19.34 linux amd64 with go1.26.11 Wed Nov 11 06:48:42 UTC 2026
  内核报错无法定位节点:
time="2026-11-28T15:03:33.752290478Z" level=error msg="yaml: line 6789: block sequence entries are not allowed in this context"
configuration file /home/runner/work/flclash-subscription/flclash-subscription/.cache/work/validate.yaml test failed

  剔除非法节点 78，剩余 12707（用时 7.0s）
    - vless 15.204.97.195 (invalid REALITY short ID)
    - vless 15.204.97.197 (invalid REALITY short ID)
    - vless 15.204.97.206 (invalid REALITY short ID)
    - vless 15.204.97.214 (invalid REALITY short ID)
    - vless 15.204.97.216 (invalid REALITY short ID)
    - vless 15.204.97.219 (invalid REALITY short ID)
    - vless 51.158.206.103 (invalid REALITY short ID)
    - vless 51.158.206.12 (invalid REALITY short ID)
[5/9] 初筛：真实请求（128 线程，1 轮）
Traceback (most recent call last):
  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 2576, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 2096, in main
    quick = measure(exe, merged, work, args.workers, 1, args.timeout, url)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 504, in measure
    proc = start_core(exe, cfg, workdir, ctl, os.path.join(workdir, "core.log"))
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 475, in start_core
    raise RuntimeError("mihomo 启动失败:\n" + open(logfile, encoding="utf-8", errors="ignore").read()[-1500:])
RuntimeError: mihomo 启动失败:
time="2026-11-28T15:03:37.682275912Z" level=fatal msg="Parse config error: yaml: line 91798: block sequence entries are not allowed in this context"


::error title=流水线失败::未捕获异常，traceback 末尾：Traceback (most recent call last):%0A  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 2576, in <module>%0A    sys.exit(main())%0A             ^^^^^^%0A  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 2096, in main%0A    quick = measure(exe, merged, work, args.workers, 1, args.timeout, url)%0A            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^%0A  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 504, in measure%0A    proc = start_core(exe, cfg, workdir, ctl, os.path.join(workdir, "core.log"))%0A           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^%0A  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 475, in start_core%0A    raise RuntimeError("mihomo 启动失败:\n" + open(logfile, encoding="utf-8", errors="ignore").read()[-1500:])%0ARuntimeError: mihomo 启动失败:%0Atime="2026-11-28T15:03:37.682275912Z" level=fatal msg="Parse config error: yaml: line 91798: block sequence entries are not allowed in this context"
```
