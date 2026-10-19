# CaringFailures

トラウマ級の見た目をした化け物に、**逃げるのではなく自ら近づいてお世話をする**3Dサバイバルホラー。

[![CaringFailures プレイ動画](https://img.youtube.com/vi/rKZcAX_y5iw/maxresdefault.jpg)](https://youtu.be/rKZcAX_y5iw)

※画像をクリックするとYouTubeでプレイ動画（約2分20秒）が再生されます。

| 開発期間 | 人数 | 状況 | 使用技術 |
| --- | --- | --- | --- |
| 2か月 | 1人（全工程） | β版（1周プレイ可能） | Unity 6000.4.5f1 / C# / UniTask / DOTween / Blender |

## 見てほしいポイント

**1. 自分で描いた2Dデザインを、自分で3Dモデルにした**
前作『SquareDeviant』の異形種デザインを、三面図からモデリング、リギング、UV、テクスチャまで一人で制作しました。
→ 制作工程とモデリングで得た知見：[Docs/Modeling.md](.Modeling.md)

| 元の2Dデザイン | 3Dモデル |
| --- | --- |
| <img width="200" alt="StillHuman1" src="https://github.com/user-attachments/assets/f77025c7-e922-4343-a033-ef37392942e3" /> | <img width="400" height="250" alt="StillHuman_Model" src="https://github.com/user-attachments/assets/e32fa554-4e79-46f5-9774-5ff382541762" /> |

**2. 前作の反省を設計に反映した**
前作で起きたクラスの肥大化とAudio周りの混乱を受け、1クラス1責務を徹底し、音を鳴らすオブジェクト自身がAudioSourceを持つ構成に作り直しました。実装前に設計書で共通処理と個別処理の境界を決め、後付けによる複雑化を防いでいます。

**3. 2か月で形にするための効率化**
Audio編集、UI一括設定、アイテムアイコン生成、Lightの影設定などのエディタツールを導入し、繰り返し作業を削減しました。

<details>
<summary><b>生成AIの利用について</b></summary>

設計とレビューは自分が行い、実装はAIの補助を受ける分担で開発しました。AIには厳格なルールを課しています（全文：[CLAUDE.md](./CLAUDE.md)）。生成されたコードは必ず読み、不要なUpdate処理やマジックナンバー、意図とずれた箇所は自分で修正しています。

| ツール | 用途 |
| --- | --- |
| Claude / Gemini | コーディング支援、デバッグ、エディタツールの作成 |
| Claude | 一部アニメーション（喜びの舞など）を生成するBlender用スクリプトの作成。待機モーションとのつなぎは手作業で調整 |
| Meshy.AI | 一部の3Dモデルの生成（メインの化け物は除く） |

</details>

<details>
<summary><b>今後の予定</b></summary>

- マルチプレイ対応
- どれだけ長く生き残れるかに挑戦する「エンドレスお世話モード」（構想段階）

</details>
