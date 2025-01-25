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

---
## LLMによる補足

**esnya/UdonSunController** は、VRChatのUdonワールド向けに開発された、ランタイムでディレクショナルライト（太陽光）を自由に制御するためのUnityパッケージです。MITライセンスで公開されており、動的な時間帯の変化（昼間、夕焼け、夜間など）や反射プローブの再ベイク機能を実現します。以下に詳細を解説します。

---

### **1. 主な機能** 
- **ディレクショナルライトの動的制御**  
  太陽光の方向・明るさ・色温度をリアルタイムで調整可能。昼夜の移り変わりや環境光の変化をシームレスに表現できます。
- **反射プローブの自動更新**  
  ライトの変化に応じて反射プローブを再ベイクし、シーンの質感を維持します。過去のバージョンでは別途管理が必要でしたが、現在は統合されています。
- **最小光量制限**  
  v4.1.0以降では、太陽光の強度に下限値を設定できるようになり、過度な暗さを防ぎます。
- **軽量な設計**  
  UdonSharpを用いた単一のUdon Behaviourで動作し、計算量を最適化。

---

### **2. インストール手順** 
1. **前提条件**  
   - `VRCSDK3_WORLD` と `UdonSharp` がプロジェクトにインストールされている必要があります。
2. **パッケージの追加**  
   - GitHubから最新の`.unitypackage`をダウンロードし、Unityプロジェクトにインポート。
3. **Prefabの配置**  
   - `Assets/UdonSunController/SunController.prefab` をシーンに配置。
4. **セットアップ**  
   - Prefabのインスペクターで「**Setup From Scene**」ボタンを2回クリックし、ディレクショナルライトを手動で追加。

---

### **3. バージョン履歴と注意点** 
- **v4.0.0（2023-02-11）**  
  - 複数のUdonを単一のスクリプトに統合し、同期機能を廃止。
  - UdonSharp 1.xへの移行とVPM（VRChat Package Manager）対応。
- **v4.1.0（2023-09-18）**  
  - 太陽光の強度に最小値を設定する機能を追加。
- **破壊的変更**  
  - ディレクショナルライトはPrefabから削除されたため、シーンに手動で追加する必要があります。

---

### **4. 応用例と関連プロジェクト** 
- **ワールドデザイン**  
  昼夜切り替え機能を持つワールド（例：チキンナゲットが食べられる「Just Chicken Nugget」）で使用され、照明の自然な遷移を実現。
- **関連ツール**  
  - **InariUdon**：esnya氏が開発したUdonユーティリティ集。
  - **UdonDoor**：ドアの物理挙動を制御するパッケージ。
  - **EsnyaUnityShaders**：VRChat向けの多機能シェーダー集。

---

### **5. コミュニティとサポート** 
- **トラブルシューティング**  
  UnityのInput System設定で「Process Events In Dynamic Update」を選択すると、一部の操作エラーが解消されるケースがあります。
- **ライセンス**  
  MITライセンスのため、商用・非商用問わず自由に利用・改変可能です。

---

### **6. ダウンロードと参考リンク**
- **GitHubリポジトリ**: [esnya/UdonSunController](https://github.com/esnya/UdonSunController)  
- **デモワールド**: VRChat内で「UdonSunController」や「EsnyaUdonFactory」を検索。

このパッケージは、VRChatワールドの環境表現を柔軟にカスタマイズしたい開発者に強く推奨されます。最新版の利用により、パフォーマンスと機能性の両立が可能です。
