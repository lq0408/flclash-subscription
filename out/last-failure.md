# 上次构建失败：2026-11-26 14:10 UTC

```
运行环境: python 3.12.16 | Linux x86_64 | 工作目录 /home/runner/work/flclash-subscription/flclash-subscription
参数: workers=128 rounds=2 timeout=3000ms max_delay=3000ms 输出=out/flclash-free-nodes.yaml
[1/9] 复测上一版订阅（老节点优先）
  从 flclash-free-nodes.yaml 读到 60 个老节点，复测后上海 RTT ≤150ms 才保留
[2/9] 抓取节点源
  [ok]   anaer/Sub                                 596 KB  (raw.githubusercontent.com)
  [ok]   Barabama/FreeNodes                        941 KB  (raw.githubusercontent.com)
  [ok]   Au1rxx/free-vpn-subscriptions             601 KB  (raw.githubusercontent.com)
  [ok]   cysk003/freeSub                           271 KB  (raw.githubusercontent.com)
  [ok]   ts-sf/fly                                 243 KB  (raw.githubusercontent.com)
  [ok]   ermaozi/get_subscribe                     150 KB  (raw.githubusercontent.com)
  [ok]   share-daily/node                          143 KB  (raw.githubusercontent.com)
  [ok]   yy1588133/proxy-pool                      287 KB  (raw.githubusercontent.com)
  [ok]   freeclashnode.com                         134 KB  (freeclashnode.com/20261126)
  [ok]   clashnode.me                              134 KB  (clashnode.me/20261126)
  抓取完成: 成功 10 / 10，用时 1.2s
[3/9] 解析 / 清洗 / 去重
  Au1rxx_free-vpn-subscriptions__output_cl 新增  807
  Barabama_FreeNodes__nodes_merged.yaml.ya 新增 2341
  anaer_Sub__clash.yaml.yaml               新增 2099
  cysk003_freeSub__clash.yaml.yaml         新增  500
  daily_clashnode.me_20261126.yaml         新增   65
  daily_freeclashnode.com_20261126.yaml    新增    0
  ermaozi_get_subscribe__subscribe_clash.y 新增  157
  share-daily_node__clash.yaml.yaml        新增   92
  ts-sf_fly__clash.yaml                    新增  189
  yy1588133_proxy-pool__clash.yaml.yaml    新增  158
  已过滤开放/明文协议: http-plain/socks5
  去重后候选: 6468（用时 5.6s）
[4/9] 内核校验
  mihomo 版本: v1.19.34
  Mihomo Meta v1.19.34 linux amd64 with go1.26.11 Wed Nov 11 06:48:42 UTC 2026
  内核报错无法定位节点:
time="2026-11-26T14:10:47.465132754Z" level=error msg="yaml: control characters are not allowed"
configuration file /home/runner/work/flclash-subscription/flclash-subscription/.cache/work/validate.yaml test failed

  剔除非法节点 0，剩余 6468（用时 1.0s）
[5/9] 初筛：真实请求（128 线程，1 轮）
Traceback (most recent call last):
  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 2491, in <module>
    sys.exit(main())
             ^^^^^^
  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 2020, in main
    quick = measure(exe, merged, work, args.workers, 1, args.timeout, url)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 481, in measure
    proc = start_core(exe, cfg, workdir, ctl, os.path.join(workdir, "core.log"))
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 452, in start_core
    raise RuntimeError("mihomo 启动失败:\n" + open(logfile, encoding="utf-8", errors="ignore").read()[-1500:])
RuntimeError: mihomo 启动失败:
time="2026-11-26T14:10:47.599893837Z" level=fatal msg="Parse config error: yaml: control characters are not allowed"


::error title=流水线失败::未捕获异常，traceback 末尾：Traceback (most recent call last):%0A  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 2491, in <module>%0A    sys.exit(main())%0A             ^^^^^^%0A  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 2020, in main%0A    quick = measure(exe, merged, work, args.workers, 1, args.timeout, url)%0A            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^%0A  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 481, in measure%0A    proc = start_core(exe, cfg, workdir, ctl, os.path.join(workdir, "core.log"))%0A           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^%0A  File "/home/runner/work/flclash-subscription/flclash-subscription/scripts/pipeline.py", line 452, in start_core%0A    raise RuntimeError("mihomo 启动失败:\n" + open(logfile, encoding="utf-8", errors="ignore").read()[-1500:])%0ARuntimeError: mihomo 启动失败:%0Atime="2026-11-26T14:10:47.599893837Z" level=fatal msg="Parse config error: yaml: control characters are not allowed"
```
