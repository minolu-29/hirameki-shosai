# ひらめき書斎

公開URL：https://minolu-29.github.io/hirameki-shosai/

1問で頭が冴える、30代向けの知的ゲーム10本。すきま時間に解ける長さで、ちょっと手ごわい問題がそろっています。結果は画像にしてシェアできます。

## ゲーム一覧

| # | ゲーム | 内容 | リンク |
|---|---|---|---|
| 01 | テンパズル | 4つの数字と四則演算で10を作る（2分で何問） | `#ten` |
| 02 | 数列のつづき | 数列の法則を見抜いて次の数を選ぶ | `#seq` |
| 03 | ナンプレ6×6 | 6×6の数独をタイムアタック | `#sudoku` |
| 04 | ライツアウト | 3×3→4×4→5×5の明かりを全部消す | `#lights` |
| 05 | 8パズル | 数字をスライドして1〜8に並べる | `#slide` |
| 06 | 数字の記憶 | 表示された数字を順に再入力、桁数が増えていく | `#span` |
| 07 | 順位推理 | 条件から一番・二番を推理する | `#logic` |
| 08 | 2バック | 2つ前と同じ文字かを判定し続ける | `#nback` |
| 09 | 図形回転 | 回転か鏡像かを見抜く | `#rotate` |
| 10 | マインスイーパー | 9×9・地雷10個をタイムアタック | `#mines` |

問題は毎回ランダムに作られます（テンパズルは必ず解ける組み合わせ、ナンプレは答えが1つに決まる問題だけを出題）。

## しくみ（どこを直せば何が変わるか）

ゲーム本体は `src/index.html` の1ファイルだけです。ここを直して main に入れると、GitHub が自動で次の3つを作り直します。

| 作られるもの | 置き場所 | 使い道 |
|---|---|---|
| 自分のサイト版 | GitHub Pages（公開URL） | 広告（Google）とアクセス解析つき |
| `hirameki-shosai-crazygames.zip` | Releases の「latest」 | CrazyGames にアップロード |
| `hirameki-shosai-gamedistribution.zip` | Releases の「latest」 | GameDistribution にアップロード |

広告やアクセス解析のIDは `monetize.config.json` に書きます。空のあいだは広告なしで動きます。

| 項目 | 入れるもの |
|---|---|
| `web.adsenseClient` | AdSense のサイト運営者ID（`ca-pub-` で始まる） |
| `web.adTest` | 審査中・確認中は `true`（テスト広告）。本番は `false` |
| `web.ga4` | Google アナリティクスの測定ID（`G-` で始まる） |
| `gamedistribution.gameId` | GameDistribution でゲームを登録したときにもらうID |
| `customDomain` / `siteUrl` | 独自ドメインを使うときに設定 |

画面の文字は、ブラウザが日本語なら日本語、それ以外は英語で出ます。ホーム画面の下のボタンで切り替えられ、URLに `?lang=en` を付けても英語になります。

## ファイル

| ファイル | 役割 |
|---|---|
| `src/index.html` | ゲーム本体（HTML・CSS・JSを1ファイルに収録） |
| `src/platforms/` | 配信先ごとの違い（広告の出し方・記録の保存先）だけをまとめたファイル |
| `tools/build.mjs` | 配信先ごとの版を `dist/` に作るスクリプト（`node tools/build.mjs`） |
| `monetize.config.json` | 広告・解析・配信先のID |
| `public/` | アイコン・SNS用プレビュー画像など、サイトにそのまま置くファイル |
| `store/` | ゲームサイトに提出するカバー画像 |
| `.github/workflows/publish.yml` | 自動で作り直して公開する設定 |

ベスト記録と音のオン・オフは、その端末のブラウザ（CrazyGamesではアカウント）に保存されます。
