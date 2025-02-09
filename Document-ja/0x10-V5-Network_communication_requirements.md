# V5: ネットワーク通信要件

## 管理目標

モバイルアプリとリモートサービスのエンドポイント間で交換される情報の機密性と完全性を確認することがこのセクションで説明されるコントロールの目的です。少なくとも、モバイルアプリは適切な設定でのTLSプロトコルを使用したネットワーク通信のために、セキュアで暗号化されたチャネルを設定する必要があります。レベル2には SSL ピンニングなどの追加の多層防御施策があります。

## セキュリティ検証要件

| # | MSTG-ID | 説明 | L1 | L2 |
| --- | --- | --- | --- | --- |
| **5.1** | MSTG‑NETWORK‑1 | データはネットワーク上でTLSを使用して暗号化されている。セキュアチャネルがアプリ全体を通して一貫して使用されている。 | ✓ | ✓ |
| **5.2** | MSTG‑NETWORK‑2 | TLS 設定は現在のベストプラクティスと一致している。モバイルオペレーティングシステムが推奨される標準規格をサポートしていない場合には可能な限り近い状態である。 | ✓ | ✓ |
| **5.3** | MSTG‑NETWORK‑3 | セキュアチャネルが確立されたときに、アプリはリモートエンドポイントのX.509証明書を検証している。信頼されたCAにより署名された証明書のみが受け入れられている。 | ✓ | ✓ |
| **5.4** | MSTG‑NETWORK‑4 | アプリは自身の証明書ストアを使用するか、エンドポイント証明書もしくは公開鍵をピンニングしている。信頼されたCAにより署名された場合でも、別の証明書や鍵を提供するエンドポイントとの接続を確立していない。 |   | ✓ |
| **5.5** | MSTG‑NETWORK‑5 | アプリは登録やアカウントリカバリーなどの重要な操作において（電子メールやSMSなどの）単方向のセキュアでない通信チャネルに依存していない。 |  | ✓ |
| **5.6** | MSTG‑NETWORK‑6 | アプリは最新の接続ライブラリとセキュリティライブラリにのみ依存している。 |  | ✓ |

<div style="page-break-after: always;">
</div>

## 参考情報

OWASP モバイルセキュリティテストガイドでは、このセクションに記載されている要件を検証するための詳細な手順を提供しています。

- Android - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05g-Testing-Network-Communication.md>
- iOS - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06g-Testing-Network-Communication.md>

詳しくは以下の情報を参照してください。

- OWASP Mobile Top 10: M3 - Insecure Communication: <https://www.owasp.org/index.php/Mobile_Top_10_2016-M3-Insecure_Communication>
- CWE: <https://cwe.mitre.org/data/definitions/319.html>
- CWE: <https://cwe.mitre.org/data/definitions/295.html>
