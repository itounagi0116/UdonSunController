# UdonSunController（日本語）

**最新のUnityパッケージは[こちら](https://github.com/esnya/UdonSunController/releases/latest)からダウンロードできます！**

明るい昼間、赤みがかった夕焼け、または暗い夜...

UdonSunControllerは、VRChat UdonワールドでランタイムにDirectional Lightを自由にコントロールする機能を提供します。シーンにプレハブを配置するだけで、太陽の方向に応じた明るさや色温度を自動的に制御します。また、リフレクションプローブの再ベイクも可能です。

## 必要条件
最新バージョンへのアップデートを推奨します。

* VRCSDK3_WORLD
* [UdonSharp](https://github.com/MerlinVR/UdonSharp)

## 使い方
1. `Assets/UdonSunController/SunController.prefab` をシーンに配置します。
2. 配置した `SunController` のインスペクターで `Setup From Scene` ボタンを押します。

### 新しいリフレクションプローブを追加した場合
1. 再度 `Setup From Scene` を押してください。

## v2.xからv3.xへの移行
* プレハブからDirectional Lightが削除されました。シーンに手動で追加するか、初期設定されたものをそのまま使用してください。
* ReflectionProbeUpdatorが削除されました。リフレクションプローブに追加した関連するUdonBehaviourを削除してください。UdonSunControllerが直接それらを更新するようになりました。

## ライセンス
MITライセンス

## ギャラリー
![Inspector](Documents~/img/Inspector.png)  
![Day](Documents~/img/Day.png)  
![Night](Documents~/img/Night.png)  
