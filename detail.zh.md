装法：DSH → 插件 → 添加插件 → 填 `https://github.com/zhuchongba-01/dsh-breach`。npm 上只剩一个空壳，填包名会报「没有声明组合包」。

它会改写宿主源码，每条改动留 `.dshhappy.bak`、可一键回滚，但不保证跨宿主版本兼容——用之前先自己备份。
