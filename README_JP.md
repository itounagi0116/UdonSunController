# UdonSunController (日本語)

![ライセンスバッジ](https://img.shields.io/badge/ライセンス-MIT-007EC6)

**最新のUnityパッケージは[こちら](https://github.com/esnya/UdonSunController/releases/latest)からダウンロードできます！**  

明るい昼間、赤みがかった夕焼け、または暗い夜……。  
UdonSunControllerは、VRChatのUdonワールド内でランタイム中にDirectional Light（平行光源）を自由に制御できる機能を提供します。このプレハブをシーンに配置するだけで、太陽の方向に基づいて明るさや色温度を自動的に制御します。また、リフレクションプローブの再ベイクも可能です。  

---

## **必要要件**  
最新バージョンへのアップデートを推奨します。  

- **VRCSDK3_WORLD**  
- **[UdonSharp](https://github.com/MerlinVR/UdonSharp)**  

---

## **使い方**  

1. `Assets/UdonSunController/SunController.prefab` をシーンに配置します。  
2. 配置した `SunController` のインスペクター内にある **`Setup From Scene`** ボタンを押します。  

### **新しいリフレクションプローブを追加した場合**  
1. 再度、**`Setup From Scene`** ボタンを押します。  

---

## **v2.xからv3.xへの移行方法**  

- プレハブからDirectional Light（平行光源）が削除されました。シーンに手動で追加するか、初期設定のものを維持してください。  
- ReflectionProbeUpdatorが削除されました。これに伴い、リフレクションプローブに追加したUdonBehaviourを削除してください。現在は、UdonSunControllerがリフレクションプローブを直接更新します。  

---

## **ギャラリー**  
以下は使用例の画像です:  

- **インスペクター画面**  
  ![Inspector](Documents~/img/Inspector.png)  

- **昼間の例**  
  ![Day](Documents~/img/Day.png)  

- **夜間の例**  
  ![Night](Documents~/img/Night.png)  