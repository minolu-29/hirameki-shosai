# ゲームサイト提出用テキスト

提出フォームは英語なので、英語の文をそのままコピーして使ってください。日本語訳は確認用です。
アップロードするファイルとカバー画像は、GitHub の Releases「latest」に自動で置かれます。

## ひらめき書斎（hirameki-shosai）

**Title**
Hirameki Study - 10 Brain Puzzles

**Description（英語）**
Ten short brain puzzles for grown-ups. Make 10 from four numbers with + − × ÷, find the rule of a number sequence, solve a 6×6 sudoku, switch off every light in Lights Out, slide the 8-puzzle into order, remember long digit strings, deduce who is tallest from clues, train your working memory with 2-back, spot whether a shape is rotated or mirrored, and clear a classic minesweeper board. Puzzles are generated fresh every time.

（日本語訳）大人のための知的ゲーム10本。テンパズル、数列、ナンプレ6×6、ライツアウト、8パズル、数字の記憶、順位推理、2バック、図形回転、マインスイーパー。問題は毎回新しく作られます。

**Controls**
- Tap or click buttons and tiles. In Minesweeper, long-press or use the flag button to place a flag.
- Each puzzle explains its rules before it starts.

**Category / Tags（候補）**
Puzzle / brain, logic, math, sudoku, memory, minesweeper

## CrazyGames の設定
| 項目 | 設定 |
|---|---|
| Game file | `hirameki-shosai-crazygames.zip` をアップロード |
| Orientation（画面の向き） | Portrait（縦）。パソコンでも左右に余白が付いて遊べます |
| Mobile support | Yes（スマホ・タブレット対応） |
| Progress Save（記録の保存） | **必ずオンにする**。オフだとベスト記録が保存されません |
| Covers | `store/` の3枚（1920×1080・800×1200・800×800） |
| Language | English, Japanese（ブラウザの言語で自動切り替え） |

## GameDistribution の設定

1. ゲームを新規登録して、もらった Game ID を `monetize.config.json` の `gamedistribution.gameId` に入れて main に入れる
2. 数分後に Releases「latest」に作り直される `hirameki-shosai-gamedistribution.zip` をアップロードする
3. タイトル・説明文・操作方法は上と同じ英語を使う。画面の向きは Portrait、スマホ対応は Yes
