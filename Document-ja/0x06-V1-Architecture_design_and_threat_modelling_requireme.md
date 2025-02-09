# V1: アーキテクチャ, 設計, 脅威モデリング要件

## 管理目標

理想的な世界では、セキュリティは開発の全てのフェーズを通して考慮されることでしょう。しかし実際には、SDLCの後ろのステージでのみセキュリティは考慮されます。技術的なコントロールのほかに、MASVSではセキュリティが明示的に計画フェーズ中に割り当てられ、すべてのコンポーネントについて機能やセキュリティの役割が明確であることを保証する所定のプロセスを要求します。ほとんどのモバイルアプリはリモートサービスのクライアントとして動作しますので、適切なセキュリティ基準がそれらのサービスに適用されることも保証しなければいけません。モバイルアプリをテストするだけでは不十分です。

カテゴリ「V1」にはアプリのアーキテクチャと設計に関する要件が記載されています。したがって、これは OWASP モバイルテストガイドの技術的なテストケースに対応していない唯一のカテゴリです。脅威モデル、セキュア SDLC、鍵管理などのトピックをカバーするには、MASVS のユーザーはそれぞれの OWASP プロジェクトや以下にリンクされているような他の標準を参照する必要があります。

<div style="page-break-after: always;">
</div>

## セキュリティ検証要件

MASVS-L1 および MASVS-L2 の要件を以下に記します。

| # | MSTG-ID | 説明 | L1 | L2 |
| --- | --- | --- | --- | --- |
| **1.1** | MSTG‑ARCH‑1 | アプリのすべてのコンポーネントを把握し、それらが必要とされている。 | ✓ | ✓ |
| **1.2** | MSTG‑ARCH‑2 | セキュリティコントロールはクライアント側だけではなくそれぞれのリモートエンドポイントで実施されている。 | ✓ | ✓ |
| **1.3** | MSTG‑ARCH‑3 | モバイルアプリと接続されるすべてのリモートサービスの高次のアーキテクチャが定義され、そのアーキテクチャにセキュリティが対応されている。 | ✓ | ✓ |
| **1.4** | MSTG‑ARCH‑4 | モバイルアプリのコンテキストで機密とみなされるデータが明確に特定されている。 | ✓ | ✓ |
| **1.5** | MSTG‑ARCH‑5 | アプリのすべてのコンポーネントは提供する業務上の機能やセキュリティ上の機能の観点で定義されている。 |   | ✓ |
| **1.6** | MSTG‑ARCH‑6 | モバイルアプリとそれに関連するリモートサービスの脅威モデルが作られ、潜在的な脅威と対策を特定している。 |   | ✓ |
| **1.7** | MSTG‑ARCH‑7 | すべてのセキュリティコントロールは集約実装されている。 |   | ✓ |
| **1.8** | MSTG‑ARCH‑8 | 暗号鍵が（もしあれば）どのように管理されるかについての明確な方針があり、暗号鍵のライフサイクルが施行されている。 NIST SP 800-57 などの鍵管理標準に準拠することが理想的である。 |   | ✓ |
| **1.9** | MSTG‑ARCH‑9 | モバイルアプリの更新を強制するメカニズムが存在している。 |   | ✓ |
| **1.10** | MSTG‑ARCH‑10 | セキュリティはソフトウェア開発ライフサイクルのあらゆる部分で対処されている。 |   | ✓ |

## 参考情報

詳しくは以下の情報を参照してください。

- OWASP Mobile Top 10: M10 - Extraneous Functionality: <https://www.owasp.org/index.php/Mobile_Top_10_2016-M10-Extraneous_Functionality>
- OWASP Security Architecture cheat sheet: <https://www.owasp.org/index.php/Application_Security_Architecture_Cheat_Sheet>
- OWASP Thread modelling: <https://www.owasp.org/index.php/Application_Threat_Modeling>
- OWASP Secure SDLC Cheat Sheet: <https://www.owasp.org/index.php/Secure_SDLC_Cheat_Sheet>
- Microsoft SDL: <https://www.microsoft.com/en-us/sdl/>
- NIST SP 800-57: <http://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf>
