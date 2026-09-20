# 数字ドロップ サポートサイト

iOSゲーム「数字ドロップ」のApp Store申請に使用する、プライバシーポリシーとサポートページです。HTML/CSSだけで動作し、JavaScript、ビルド作業、外部フォント、広告はありません。メールアドレスはWebページに掲載しません。

## 公開予定URL / App Store Connectで使用するURL

GitHubアカウント `storiasalon-code`、リポジトリ `numberdrop-support` の場合：

- **プライバシーポリシーURL**：https://storiasalon-code.github.io/numberdrop-support/privacy.html
- **サポートURL**：https://storiasalon-code.github.io/numberdrop-support/support.html

公開完了と下記の申請前確認が済んでから、App Store Connectの各欄へ入力してください。アカウントまたはリポジトリ名を変更した場合はURLも変わります。

## ファイル

- `privacy.html`：プライバシーポリシー
- `support.html`：サポート案内とお問い合わせボタン
- `style.css`：共通デザイン
- `.nojekyll`：GitHub Pagesで静的ファイルをそのまま公開するための空ファイル

## GoogleフォームURLの変更方法

1. Googleフォームで問い合わせフォームを作成し、回答の受付を有効にします。
2. **回答者用URL**をコピーします。編集用URLではありません。
3. `support.html` を開き、`CONTACT_FORM_URL` を検索します。
4. その直後のリンクの `href="https://forms.google.com/"` を、取得した回答者用URLに置き換えます。

```html
<a class="button" href="ここに回答者用URLを貼り付ける">お問い合わせフォームを開く</a>
```

5. 保存してcommit・pushします。GitHubのWeb画面で編集する場合は「Commit changes」で保存します。
6. 公開サポートページのボタンからフォームを開き、テスト送信と回答の受信を確認します。

現在の `https://forms.google.com/` は仮URLです。このままでは数字ドロップへの問い合わせを受け付けられません。

フォームには、問い合わせ内容、端末、iOSバージョン、アプリバージョン、再現手順を入力できる欄を用意してください。返信先が必要な場合はフォーム内で受け付け、Webページにメールアドレスを直接掲載しないでください。スクリーンショットの添付欄を設ける場合は、回答者側のログイン要否も確認してください。添付できない方にも文章で問い合わせできるようにします。

## プライバシーポリシーの更新方法

1. `privacy.html` の該当箇所を編集します。
2. 「3. 外部サービスについて」は実際のアプリ仕様に合わせます。現在は開発者の確認に基づき **Apple Game Center** のみを記載しています。AdMob、Firebase、Unity関連サービスは掲載していません。サービスを追加・削除する場合は本文も更新してください。
3. 使用するSDK、取得する情報、広告の有無、保存先を確認し、1〜5節の記載も合わせます。Game CenterのApple公式プライバシー案内へのリンクは掲載済みです。
4. 正式仕様が確定したら、将来更新予定・使用可能性を示す仮の文章も実際の仕様に合わせます。
5. 末尾の最終更新日と `<time datetime="2026-09-20">` の日付を両方更新します。
6. 保存してcommit・pushし、公開ページに反映されたことを確認します。

## GitHub Pagesの設定方法

1. GitHubに `numberdrop-support` という公開リポジトリを作成します。
2. 上記ファイルを `main` ブランチのルート（一番上の階層）に置きます。
3. リポジトリの **Settings → Pages** を開きます。
4. **Build and deployment → Source** を **Deploy from a branch** にします。
5. **Branch** を **main**、フォルダを **/ (root)** に設定し、**Save** を押します。
6. デプロイが完了したら、上の2つのURLに直接アクセスします。必要に応じて **Enforce HTTPS** も確認します。

トップページ用の `index.html` はありません。App Store Connectにはリポジトリ直下のURLではなく、必ず末尾が `privacy.html` / `support.html` のURLを登録してください。

## 申請前の最終確認

- [ ] 実際に使用していない外部サービスを削除し、プライバシーポリシーを実装と一致させた
- [ ] 仮の問い合わせURLを回答者用GoogleフォームURLへ変更した
- [ ] 問い合わせフォームで実際に送信・受信できた
- [ ] 両方のページをHTTPSの直接URLから開けた（404にならない）
- [ ] ログアウト状態でも両ページを閲覧できた
- [ ] スマートフォンとPCで文字・余白・ボタンを確認した
- [ ] 日本語が文字化けせず、ページ間リンクとフッターリンクが動いた
- [ ] App Store Connectのプライバシー回答と、実装・ポリシーの内容が一致している

ページの公開と、App Storeへの申請準備完了は別です。仮URLや未確定のサービス記載が残る状態では、申請用として完成したとは扱わないでください。
