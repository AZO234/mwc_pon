# MineWorldCraft - Power of Nature

地形mod、ノイズ＆構造物生成調整を行い、  
通常のOverworldを16倍程度に広大化・希釈したワールドです。  

通常Overworldはミニチュア感、  
構造物が過剰に密に生成される（ロマンが少ない）、  
交通インフラのメリットを感じたい、  
より自然に近い地形を見たい、  
などなどの気付きがありました。

この構成セットを使用することで、
風水の浸食によるダイナミックで起伏の激しい地形に、  
あるべき気候・バイオームが適応された、
自然感のあるOverworldを体験出来ます。  

利用するmodの特性上、シングルプレイonlyです。  

広いOverworldを踏破し、サバイバルせよ！  

ネザー・エンドは通常と同じです。  

## 導入

1. [Prism Launcher](https://prismlauncher.org/) を使用する

Modrinth APIにより、  
バージョンに互換のあるmod・リソースパック・シェーダの構成を構築する、  
とても便利な非公式ランチャです。

2. Prism Launcher [起動構成を追加]
3. [インポート]
4. https://github.com/AZO234/mwc_pon/raw/refs/heads/main/mwc_pon.zip
5. [シングルプレイ] → [ワールド新規作成]
6. [コマンドの許可：オン]→[ワールド新規作成]
7. WorldEditのmodにより、「木の斧は座標記憶ツール」となっています。  
    「木の斧でブロック破壊が出来ない」動作がデフォルトなので、  
    /toggleeditwand コマンドで、座標記憶モードのオン/オフを切り替えて下さい。


※砂漠・氷山・山頂で初期スポーンすると、  
生存には非常にハードな場合があります。  
ワールド生成のシード値を空白にして、ガチャしてください。


## 技術

### [TerraBlender](https://modrinth.com/mod/terrablender)

地形に合わせた気候・バイオーム適応mod。

### [Techtonic](https://modrinth.com/datapack/tectonic)

ダイナミックで自然な、  
風水による浸食・奇岩・激しい起伏の地形を生成するmod。

### worldgenでOverworldを1/16に希釈

worldgen/.../\*.json を改変し、  
Overworldのバイオームを16倍に広域化、  
構造物生成を1/16に希釈しています。

- 村の間の距離の例  
通常：300ブロック・起伏小  
このワールド：1000ブロック以上・起伏大


## worldgenの値変更 詳細

### worldgen/biome

size_horizontal = default\*16  バイオーム広さ

### worldgen/structure

separation = default\*6  構造物最小間隔チャンク  
spacing = default\*8/3  構造物平均間隔チャンク  
frequency = default/4  構造物生成頻度  
count = default/16  構造物生成数


## その他

- OpenJDK 21
- Minecraft Java Edition 1.21.5
- NeoForge
- [BetterF3](https://modrinth.com/mod/betterf3)  
より良いF3情報
- [BigShot](https://modrinth.com/mod/bigshot)  
アップスケールスクリーンショット
- [Forgematica](https://modrinth.com/mod/forgematica)  
litematic
- [Freecam](https://modrinth.com/mod/freecam)  
F4で偵察カメラモード
- [WorldEdit](https://modrinth.com/plugin/worldedit)  
schem
- [Xaero's Minimap](https://modrinth.com/mod/xaeros-minimap)  
YでミニマップHUD、Uでウェイポイント
- [Xaero's World Map](https://modrinth.com/mod/xaeros-world-map)  
Mでワールドマップ


# 補足

- 移動距離が長大なため、馬・ラクダの重要度が増します。  
  ネザーハイウェイも整備する必要があるでしょう。
- ベッドを持ち歩く旅になるため、  
  誤って初期スポーンに戻らないよう、  
  キャンプを整備し、ウェイポイントを活用しましょう。
- modによるチャンク生成のため、描画が遅くなる場合があります。  
  エリトラ移動はY320付近でも  
  未生成チャンクに埋まってロストがあり得ます。
- 描画チャンクを12→24→32と上げるほど絶景が楽しめますが、  
  ラグがかなり大きくなります。  
  BigShotによるアップコンバード撮影時のみ利用しましょう。
- ゲーミングPCほどの性能は不要ですが、  
  ボトルネックを解消して、基礎性能を上げましょう。  
  例) 8コアCPUを使用、PCIe Gen4 SSDを使用
