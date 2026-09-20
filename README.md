# 数字ドロップ サポートサイト

iOSゲーム「数字ドロップ」のApp Store申請に使用する、プライバシーポリシーとサポートページです。HTML/CSSだけで動作し、このWebサイトにはJavaScript、ビルド作業、外部フォント、広告はありません。ゲーム内では広告を表示する予定です。メールアドレスはWebページに掲載しません。

## 公開URL / App Store Connectで使用するURL

GitHubアカウント `storiasalon-code`、リポジトリ `numberdrop-support` の場合：

- **プライバシーポリシーURL**：https://storiasalon-code.github.io/numberdrop-support/privacy.html
- **サポートURL**：https://storiasalon-code.github.io/numberdrop-support/support.html

GitHub Pagesで公開済みです。下記の申請前確認が済んでから、App Store Connectの各欄へ入力してください。アカウントまたはリポジトリ名を変更した場合はURLも変わります。

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
2. 「3. 外部サービスについて」は実際のアプリ仕様に合わせます。現在の導入状況は下の表のとおりです。Unity本体とInput Systemを使用していること、広告SDKなどは未導入であることを記載しています。サービスを追加・削除する場合は本文も更新してください。
3. 使用するSDK、取得する情報、広告の有無、保存先を確認し、1〜5節の記載も合わせます。広告を表示する予定ですが、広告SDKは未導入です。導入する広告サービスが決まったら、実際の取得データ・設定を確認し、提供元のプライバシーポリシーへのリンクを追加してください。
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
- [x] 両方のページをHTTPSの直接URLから開けた（404にならない）
- [x] 認証情報・CookieなしのHTTPリクエストでも両ページを閲覧できた
- [x] ブラウザのスマートフォン幅320px・375pxとPC幅1280pxで表示を確認した（実機検証は未実施）
- [x] 日本語が文字化けせず、ページ間リンクが動いた。フッターのリンク先も正常な公開URLと一致した
- [ ] App Store Connectのプライバシー回答と、実装・ポリシーの内容が一致している

ページの公開と、App Storeへの申請準備完了は別です。仮URLや未確定のサービス記載が残る状態では、申請用として完成したとは扱わないでください。

## 公開確認記録（2026年9月20日）

- リポジトリ：https://github.com/storiasalon-code/numberdrop-support
- `main` ブランチの `/ (root)` から公開。HTTPS強制が有効です。
- `privacy.html`・`support.html`・`style.css` のHTTP 200、UTF-8、ローカルファイルとの一致を確認しました。
- 開発者から訂正された導入状況に合わせ、Game Centerを使用しているという記載を削除しました。広告は表示予定で、広告SDK未導入であることを明記しています。
- お問い合わせボタンは仮URLへの遷移を確認済みですが、Googleのログイン画面へ移動します。実際の問い合わせフォームへの差し替えと送受信確認は未完了です。

## 現在の導入状況（開発者確認済み）

| 項目 | 現在の状態 |
| --- | --- |
| Unity | 導入済み |
| Unity Input System | 導入済み |
| Google AdMob | 実広告SDKは未導入 |
| Unity Ads | 未導入 |
| Firebase Analytics | 未導入 |
| Firebase Crashlytics | 未導入 |
| Firebase Database | 未導入 |
| Game Center | 未導入 |
| 課金SDK / IAP | 未導入 |

Unity本体・Input Systemの導入を、Unity Adsや分析サービスの導入と同一には扱いません。この表は開発者からの申告に基づきます。ゲームのソースコードやUnityの設定をこのリポジトリで検査したものではありません。

広告を表示する方針は確定していますが、採用する広告サービスは未確定として扱っています。AdMobが表にあることだけを理由に採用済みとは記載しません。広告SDK導入後、広告配信開始・App Store申請の前に `privacy.html` の1〜5節を更新してください。導入予定を示す文章も、その時点の実際の仕様に置き換えます。
