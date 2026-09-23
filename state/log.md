# 実行ログ

## 2026-09-23（初回ブートストラップ＋実験1）
- やったこと：RULES.md・state・backlog・README・ツール一覧を作成。最初の実験「和暦・西暦・年齢 変換と早見表」（docs/wareki/）を公開。
- 数値：公開中の実験がなかったため計測なし。このセッションにはGitHubのトラフィックAPI／Pages設定APIを呼ぶ手段がない（gh CLIなし）。
- Pages：自動で有効化できず、escalations.md に依頼を記載。
- 次回：Pagesが有効か確認→Issue・スター等を計測→バックログから次の実験（全角半角変換 or CSV文字化け修正）を1つ公開。

## 2026-09-23 引っ越し
公開名義を匿名の Organization tenohira-tools に移し、サイト名を『てのひらツール』に変更。旧リポジトリの履歴は持ち込まず、ファイルだけを移した。

## 2026-09-23 自動化の準備＋実験2
- やったこと：STRATEGY.md（AI時代の選び方を含む）、.github/workflows/maintenance.yml、IndexNow鍵ファイルをリポジトリに作成（これまで無かったため）。新しい実験「CSV・テキストの文字化け直しツール」（docs/csv-fix/）を公開。Shift_JIS/EUC-JP/ISO-2022-JPを自動判定してUTF-8に変換し、ExcelのCSV文字化け対策としてBOM追加・削除を切り替えられる。docs/index.htmlとdocs/sitemap.xmlに追加。
- 検証：Playwright（Chromiumヘッドレス）でCP932エンコードのCSV（丸数字を含む）を読み込ませ、自動判定・プレビュー表示・UTF-8ダウンロード（BOM有無）・言語切替の動作を確認。JSシンタックスエラーなし。
- 数値：公開直後のため計測なし。wareki（初回実験）もPages反映後の閲覧数を取得する手段がまだない（gh CLIなし、トラフィックAPIへのアクセス手段なし）。
- 次回：maintenance.ymlが今夜(22:30 UTC)からsitemap更新・IndexNow通知・毎日の表示チェックを開始する見込み。state/health.mdが書かれたら内容を確認する。反応を計測する手段（Issue・スター等）を優先して探す。
