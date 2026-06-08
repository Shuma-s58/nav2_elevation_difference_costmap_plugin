## nav2_elevation_difference_costmap_plugin
---

このリポジトリは, nav2のcostmap用のpluginです.
高低差格子地図の仕組みを実装しています.

高低差格子地図の仕組みはこちらを参考に実装しています.
井上裕文（千葉工大），上田隆一（千葉工大），林原靖男（千葉工大），"高低差格子地図を用いた移動ロボットの自己位置推定"，3I1-4，SI2016 (2016)

----
* 使い方
以下を参考にnav2_param.yamlにelevation_layerを追加することで使用できます.
```
local_costmap:
  local_costmap:
    ros__parameters:
      plugins: ["elevation_layer"]
      elevation_layer:
        plugin: "nav2_elevation_difference_costmap_plugin::ElevationLayer"
        enabled: True

```
