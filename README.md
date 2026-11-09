# AIツール早見表

やりたいこと別に、まず試したいAIツールをまとめました。機能や利用条件は更新されることがあるので、使う前に各サービスの公式情報も確認してください。

| やりたいこと | おすすめ | ひとこと |
| --- | --- | --- |
| 相談・文章・画像 | [ChatGPT](https://chatgpt.com/) | 無料 / Plus $20/月。画像生成対応 |
| 長文・文章・コーディング | [Claude](https://claude.ai/) | 無料 / Pro $20/月。Claude Codeも利用可能 |
| PC上の作業を進めるエージェント | [Muse](https://muse.ai/) | 無料枠あり。現在は米国から提供開始 |
| 調査・X連携・自動作業 | [Grok / Grok Bot](https://x.ai/) | 無料 / Plus $8/月 / Premium $30/月（Grok Bot付き） |
| コーディングエージェント | [OpenCode](https://opencode.ai/) | 本体無料。Go $10/月、Go Plus $40/月、またはAPI従量課金 |
| 動画生成 | [Seedance](https://seed.bytedance.com/en/seedance) | Dreamina Basic $15/月からの価格表示例。クレジット制 |
| 画像生成 | ChatGPT / Dreamina | ChatGPT無料枠あり。Dreaminaは月額プランに画像クレジット付き |

料金は2026年11月に確認した米ドルの目安です。日本円価格、税、アプリストア価格、キャンペーンで異なる場合があります。契約画面の継続価格を確認してください。

## 料金の目安

| サービス | 無料で試せる？ | 有料の目安 | メモ |
| --- | --- | --- | --- |
| ChatGPT | あり | Plus $20/月。Pro $100 / $200 / $500/月 | 画像生成も含む。上限と提供プランはアカウントで確認。APIは別料金 |
| Claude | あり | Pro $20/月、年払い $200/年。Max 5x $100/月、Max 20x $200/月 | Claude CodeはPro以上で利用可能。地域・税で変動 |
| Muse | あり | 基本機能無料、上位サブスクあり（地域ごとのアプリ内価格） | 米国で提供開始。タスク実行型のパーソナルエージェント |
| Grok / Grok Bot | あり | Plus $8/月、Premium $30/月、Super $100/月、Ultra $200/月 | 公式料金ページではGrok BotはPremium以上。利用枠はGrok/Cursorで共有 |
| OpenCode Go | OpenCode本体は無料 | Go $10/月、Go Plus $40/月、Go Teams $20/人/月 | 定額の利用枠付き。DeepSeek V4.1 Flashも選択可。枠やモデル構成を確認 |
| DeepSeek APIをOpenCodeに接続 | OpenCode本体は無料 | 月額なし、従量課金。DeepSeek V4.1 Flashは入力 $0.30/100万トークン、出力 $1.20/100万トークン（ピーク時） | オフピークは各半額。使った分だけ支払う |
| Dreamina（Seedance / 画像生成） | 無料枠あり | Basic $15/月からの表示例 | クレジット制。地域・キャンペーン・モデル・画質で変動。更新後の価格を確認 |

## OpenCodeで使うモデル

コスパ重視なら、まず **DeepSeek V4.1 Flash** を試すのがおすすめです。手軽に定額で使うなら OpenCode Go（月 $10）に接続してモデル一覧から選択。自分のAPIキーを使うならDeepSeekプロバイダーを接続します。モデルIDはカタログ更新で変わるため、OpenCode の `/models` に表示されるIDを優先してください。

DeepSeek API のモデル名は `deepseek-flash`。公式価格は100万トークンあたり、ピーク時で入力 $0.30・出力 $1.20、オフピーク時で入力 $0.15・出力 $0.60（キャッシュ入力は別料金）です。コード変更は小さな作業から任せ、差分を確認してから採用すると安心です。

OpenCode本体は無料で、モデルの料金は接続方法によります。Goは定額サブスク、DeepSeek API直結は従量課金、OpenCode Zenはモデルごとの従量課金です。無料のローカルモデルも使えます。

## エージェントAIの使い分け

チャット型は質問や文章作成が得意。エージェント型は、ブラウザやアプリ、開発環境を使いながら複数の手順を実行するのが得意です。どこまで自動で動くか、操作の承認が必要かを見て選びます。

- **[Muse](https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/)**：Metaのパーソナルエージェント。目標や用事を渡し、連携アプリやブラウザを使った複数手順の作業を頼むタイプ。無料枠があり、現時点では米国から展開。
- **[Grok Bot](https://docs.x.ai/grok/overview)**：Grokのクラウド上のAIチームメイト。継続して動く作業やタスク委任向け。公式価格はPremium $30/月から利用可能（利用枠は他のGrok機能と共有）。
- **[OpenCode](https://opencode.ai/)**：リポジトリ内のコードを読んで編集・コマンド実行する開発エージェント。モデルはDeepSeekなどから選べる。コスパ重視ならDeepSeek V4.1 Flash、定額ならOpenCode Go $10/月、API直結なら従量課金。
- **[ChatGPT](https://chatgpt.com/)**：調査、文章、ファイル、画像など広い用途のアシスタント。Plusは$20/月。
- **[Claude](https://claude.ai/)**：長文や資料の読解に加えて、Claude Codeで開発タスクも進められる。Proは$20/月。

エージェントにメール送信、購入、ファイル削除、コード変更などを頼む場合は、実行前の確認と完了後の履歴をチェックしましょう。

## 画像生成AI

- **ChatGPT Images**：会話で画像を作り、同じスレッドで部分修正を頼みやすい。無料プランにも画像生成があるが上限はプランや混雑で変わる。Plusは$20/月。
- **Dreamina / Seedream**：Seedanceと同じDreamina内で画像も動画も作る選択肢。サブスクはクレジット制で、Basicは米国ページで$15/月の通常価格例。画像サイズやモデルで消費クレジットが異なる。

画像の指示は「主役・場所・画風・構図・用途」を入れると調整しやすいです。文字入り画像は、出力後に文字を確認して修正を頼みましょう。

## 動画生成AI

- **Seedance**：テキストや画像をもとに動画を生成。Dreaminaの月額プランでクレジットを購入する方式があり、Basic $15/月の表示例があります。動画の秒数・解像度・モデルにより消費量が異なります。
- 生成前に、選んだ設定で何クレジット使うかを確認。気に入るまで複数回生成する前提で予算を見積もると安心です。

## 生成AIへの指示のコツ

作りたいもの、雰囲気、長さや画角、入れたい要素を具体的に伝えると、イメージに近づけやすくなります。最初から完璧を狙わず、出力を見て「ここをこう変える」と追加で指示していくのがコツです。

例：

> 夕方の海辺を歩く白い犬。映画のワンシーンのような自然な光、ゆっくりしたカメラ移動、縦長動画。

画像も同じように、主役・場所・画風・構図を伝えてから、気になる箇所を会話で調整します。

## 選ぶときのポイント

- まず無料枠や試用範囲で、自分の用途に合うか確認する。
- 機密情報や個人情報を入力する前に、各サービスのデータ取り扱いを確認する。
- AIの出力は間違うことがあるため、事実やコードは必要に応じて確認する。
- 料金、使える地域、機能は変わることがあるので、公式サイトで最新情報を確認する。

## 料金・公式情報

- [ChatGPT のプラン](https://chatgpt.com/pricing)
- [Claude の料金](https://www.anthropic.com/pricing)
- [Meta Muse の紹介](https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/)
- [Grok / Grok Bot の公式情報](https://docs.x.ai/grok/overview)
- [Grok の料金](https://x.ai/pricing)
- [OpenCode のモデル選択](https://opencode.ai/docs/models)
- [OpenCode Go の月額プラン](https://opencode.ai/docs/go)
- [OpenCode Zen のモデル料金](https://opencode.ai/zen)
- [DeepSeek API のモデル・料金](https://api-docs.deepseek.com/quick_start/pricing/)
- [Seedance 公式](https://seed.bytedance.com/en/seedance)
- [Dreamina の Seedance 料金](https://dreamina.capcut.com/pricing/dreamina-seedance-price-day)
