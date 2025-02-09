# V4: 認証とセッション管理要件

## 管理目標

多くの場合、リモートサービスへのユーザーログインはモバイルアプリアーキテクチャ全体の不可欠な要素です。ロジックの大半はエンドポイントで発生しますが、MASVSではユーザーアカウントとセッションの管理方法に関するいくつかの基本的な要件を定義します。

## セキュリティ検証要件

| # | MSTG-ID | 説明 | L1 | L2 |
| --- | --- | --- | --- | --- |
| **4.1** | MSTG‑AUTH‑1 | アプリがユーザーにリモートサービスへのアクセスを提供する場合、ユーザー名/パスワード認証など何らかの形態の認証がリモートエンドポイントで実行されている。 | ✓ | ✓ |
| **4.2** | MSTG‑AUTH‑2 | ステートフルなセッション管理を使用する場合、リモートエンドポイントはランダムに生成されたセッション識別子を使用し、ユーザーの資格情報を送信せずにクライアントリクエストを認証している。 | ✓ | ✓ |
| **4.3** | MSTG‑AUTH‑3 | ステートレスなトークンベースの認証を使用する場合、サーバーはセキュアなアルゴリズムを使用して署名されたトークンを提供している。 | ✓ | ✓ |
| **4.4** | MSTG‑AUTH‑4 | ユーザーがログアウトする際に、リモートエンドポイントは既存のセッションを終了している。 | ✓ | ✓ |
| **4.5** | MSTG‑AUTH‑5 | パスワードポリシーが存在し、リモートエンドポイントで実施されている。 | ✓ | ✓ |
| **4.6** | MSTG‑AUTH‑6 | リモートエンドポイントは過度な資格情報の送信に対する保護を実装している。 | ✓ | ✓ |
| **4.7** | MSTG‑AUTH‑7 | 事前に定義された非アクティブ期間およびアクセストークンの有効期限が切れた後に、セッションはリモートエンドポイントで無効にしている。 | ✓ | ✓ |
| **4.8** | MSTG‑AUTH‑8 | 生体認証が使用される場合は（単に「true」や「false」を返すAPIを使うなどの）イベントバインディングは使用しない。代わりに、キーチェーンやキーストアのアンロックに基づいている。 |   | ✓ |
| **4.9** | MSTG‑AUTH‑9 | リモートエンドポイントに二要素認証が存在し、リモートエンドポイントで二要素認証要件が一貫して適用されている。 |   | ✓ |
| **4.10** | MSTG‑AUTH‑10 | 機密トランザクションはステップアップ認証を必要としている。 |   | ✓ |
| **4.11** | MSTG‑AUTH‑11 | アプリはユーザーのアカウントでのすべてのログインアクティビティをユーザーに通知している。ユーザーはアカウントへのアクセスに使用されるデバイスの一覧を表示し、特定のデバイスをブロックすることができる。 |  | ✓ |

<div style="page-break-after: always;">
</div>

## 参考情報

OWASP モバイルセキュリティテストガイドでは、このセクションに記載されている要件を検証するための詳細な手順を提供しています。

- 総論 - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x04e-Testing-Authentication-and-Session-Management.md>
- Android 用 - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05f-Testing-Local-Authentication.md>
- iOS 用 - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06f-Testing-Local-Authentication.md>

詳しくは以下の情報を参照してください。

- OWASP Mobile Top 10: M4 - Insecure Authentication: <https://www.owasp.org/index.php/Mobile_Top_10_2016-M4-Insecure_Authentication>
- OWASP Mobile Top 10: M6 - Insecure Authorization: <https://www.owasp.org/index.php/Mobile_Top_10_2016-M6-Insecure_Authorization>
- CWE:  <https://cwe.mitre.org/data/definitions/287.html>
