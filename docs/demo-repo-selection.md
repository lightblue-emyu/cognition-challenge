# デモ用公開リポジトリの選定

## 目的
デモのターゲット顧客として知名度の高い企業を選び、その企業が管理する公開リポジトリ（理想）を使って、Devin の価値が伝わるデモを行う。

## 選定基準
| 基準 | 内容 |
|---|---|
| 企業の知名度 | 誰もが知る企業がオーナーであること。顧客の自分ごと化につながる |
| アクティブであること | アーカイブされておらず、直近もコミットがあること |
| 適度な規模 | ローカルでビルド・テストがすぐ回ること。巨大モノレポは避ける |
| Issue バックログ | 未解決 Issue／バグが豊富で、具体的かつ再現可能なタスクを選べること |
| テスト・CI | 修正の正しさを「テストが通る」形で示せること |
| デモ映え | 「Issue 読解 → 修正 → テスト通過 → PR」を数分で見せられること |

## 候補一覧
数値は 2026-11-06 時点の GitHub API の値。

| 優先 | リポジトリ | 企業 | 言語 | Star | 未解決Issue | デモの切り口 / 注意点 |
|---|---|---|---|---|---|---|
| 1 | [Netflix/metaflow](https://github.com/Netflix/metaflow) | Netflix | Python | 10.3k | 527 | 機械学習基盤。バグ修正・テスト追加。中規模で扱いやすい |
| 2 | [spotify/luigi](https://github.com/spotify/luigi) | Spotify | Python | 18.8k | 194 | 歴史の長いコード。近代化（型ヒント、古いAPI置換）デモに最適。tox でテスト可 |
| 3 | [line/armeria](https://github.com/line/armeria) | LINEヤフー | Java | 5.2k | 715 | 日本の顧客向けに強い。初心者向けラベル付き Issue 6件。Gradle ビルドが重く事前準備が必要 |
| 4 | [Shopify/liquid](https://github.com/Shopify/liquid) | Shopify | Ruby | 11.9k | 438 | 小規模でテストが速い。短時間のライブデモ向き |
| 5 | [microsoft/vscode-python](https://github.com/microsoft/vscode-python) | Microsoft | TypeScript | 4.6k | 405（バグ122） | 大企業向けの知名度は抜群。拡張機能なので見せ方に工夫が必要 |

小さめの日本企業向け: [line/line-bot-sdk-python](https://github.com/line/line-bot-sdk-python)（LINEヤフー, Python, 2.1k Star）。ただし未解決 Issue が12件と少ない。

## 除外したもの
| リポジトリ | 理由 |
|---|---|
| Netflix/dispatch | アーカイブ済み |
| sony/nnabla | アーカイブ済み |
| backstage/backstage | 8GB超と大きすぎる |
| Mercari の公開リポジトリ | 確認した範囲では 2021〜2022 年から更新が止まっている |

## 推奨
- **第一候補: Netflix/metaflow**。知名度・規模・Issue量のバランスが最も良い。
- 日本の顧客を想定する場合は **line/armeria**（LINEヤフー）。
- 最終決定は、採用担当者からの顧客選定アドバイスを踏まえて行う。

## 次のステップ
1. ターゲット企業を確定
2. 対象リポジトリでデモ向きの Issue を 3〜5 件選定
3. ローカルでビルド・テストが通ることを確認
