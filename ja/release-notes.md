<!-- pre-align:aligned sig=3251e04c861f -->

### 2026. 08. 25.

#### 機能追加

##### Service Gateway
* ユーザー定義エンドポイント機能が追加されました。ユーザーが自身のロードバランサーをエンドポイントとして公開すると、他のプロジェクトからサービスゲートウェイ経由でインターネットを経由せずにアクセスできます。
	* ユーザー定義エンドポイントは韓国(ピョンチョン)リージョンと韓国(パンギョ)リージョンでのみ利用できます。

##### Load Balancer
* HTTP/2 サポート機能が追加されました。リスナープロトコルがTERMINATED_HTTPSであり、メンバーグループプロトコルがHTTPまたはHTTP_REENCRYPTである場合に使用できます。
	* リスナーとメンバーグループの設定画面でプロトコルバージョンを選択でき、HTTP/1がデフォルトで選択されます。
* ロードバランサーのエンジンバージョン(`v1`/`v2`)選択機能が追加されました。新規ロードバランサーは最新バージョン(`v2`)で作成され、ロードバランサーごとにエンジンバージョンを変更できます。
    *  エンジンバージョンによってHTTPトラフィック処理など一部の動作が異なる場合があるため、必ず検証してから本番環境に適用してください。
* [Load Balancer コンソール使用ガイド](/Network/Load%20Balancer/ko/console-guide/)を参照してください。

#### 機能改善

##### Flow Log
* Flow Log のファイル名カスタマイズに timezone テンプレート変数(`#{timezone}`)をオプションとして追加できます。
    * ファイル名のカスタマイズ時に `#{timezone}` 変数を含めるとファイル名に timezone が表示され、除外すると表示されません。
    * デフォルトのファイル名には、従来と同様に timezone が含まれます。timezone の値はリージョンごとに決定されます。(韓国リージョンはKST)
    * [Flow Logコンソール使用ガイド](/Network/Flow%20Log/ko/console-guide/)を参照してください。

    
<a id="network-release-notes"></a>
## Network > リリースノート { #network-release-notes }

<a id="may-27-2026"></a>
### 2026. 05. 27. { #may-27-2026 }

<a id="may-27-2026-added-features"></a>
#### 機能追加

##### Network Interface
* 「ソース/宛先確認」機能の名前を「スプーフィング防止」に変更し、ネットワークインターフェイスの作成・変更画面で設定できるよう位置を移動しました。
* スプーフィング防止を使用中に特定のアドレスのみスプーフィングを許可する「追加許可アドレス」設定機能が追加されました。
* [Network Interface コンソール使用ガイド](/Network/Network%20Interface/ja/console-guide/)を参照してください。

##### Load Balancer(DSR)
* Load Balancer(DSR) の新規サービスが追加されました。DSR（Direct Server Return）方式で動作するロードバランサーサービスを提供します。
	* Load Balancer(DSR) は韓国（ピョンチョン）リージョンと韓国（パンギョ）リージョンでのみ利用できます。
* [Load Balancer(DSR) コンソール使用ガイド](/Network/Load%20Balancer(DSR)/ja/console-guide/)を参照してください。

<a id="may-27-2026-feature-updates"></a>
#### 機能改善

##### Load Balancer
* 再暗号化機能が追加されました。メンバーグループのプロトコルに HTTP_REENCRYPT を選択すると、メンバーへの送信時に SSL 暗号化通信を使用します。
* HTTP Keepalive 無効化機能が追加されました。Keepalive タイムアウト設定で **[使用しない]** を選択すると、Keepalive が無効になります。
* SSL/TLS 暗号化ポリシー設定機能が追加されました。SSL/TLS 暗号化スイート（Cipher Suite）をユーザーがカスタマイズして使用できます。

##### Flow Log
* トラフィックパス（`traffic_path`）フィールドが追加されました。
    * パケットが通過したネットワークパス（VPC Local、Internet Gateway、VPN Gateway、VPC Peering、Region Peering、Project Peering、Service Gateway）を整数値で確認できます。
    * [Flow Log 概要](/Network/Flow%20Log/ja/overview/)を参照してください。

<a id="may-27-2026-may-27-2026-feature-updates"></a>
#### 機能変更

##### VPC
* ネットワークサービス連携のサポートのため、VPC の内部トラフィック処理方式が一部変更されました。新規作成される VPC から適用されます。

<a id="april-14-2026"></a>
### 2026. 04. 14. { #april-14-2026 }

<a id="april-14-2026-added-features"></a>
#### 機能追加

##### DNS Plus
* API v2.0 追加
    * User Access Key トークンをサポートします。

<a id="november-25-2025"></a>
### 2025. 11. 25. { #november-25-2025 }

<a id="november-25-2025-added-features"></a>
#### 機能追加

##### VPN Gateway
* VPNが接続されたVPCにTransit Hubを接続すると、Transit Hubに接続された他のプロジェクトのVPCからもオンプレミスネットワークとのVPN通信をサポートします。（接続された帯域にVPN Connectionの追加作成が必要）

##### Service Gateway
* Service Gateway作成時に、ユーザーがNAT IPを固定して作成できるよう改善されました。

##### Traffic Mirroring
* Public APIにトラフィックミラーリング関連のAPIが追加されました。[Traffic Mirroring APIガイド](/Network/Traffic%20Mirroring/ja/public-api/)を参照してください。

##### Load Balancer
* リスナーごとのユーザー定義レスポンス設定機能が追加されました。
* X-Forwarded-*ヘッダの有効化/無効化機能が追加されました。

<a id="november-25-2025-feature-updates"></a>
#### 機能改善

##### Load Balancer
* 複数のSSL証明書の登録・管理機能がコンソールでサポートされます。

<a id="november-25-2025-november-25-2025-feature-updates"></a>
#### 機能変更

##### DNS Plus
* TXTレコードセットタイプのレコード値の最大長を255バイトから4096バイトに変更しました。

<a id="august-26-2025"></a>
### 2025. 08. 26. { #august-26-2025 }

<a id="august-26-2025-added-features"></a>
#### 機能追加

##### VPN Gateway
* v2がリリースされました。
* VPNゲートウェイ作成時にローカルゲートウェイアドレスが割り当てられ、コンソールで確認できます。
* 1つのVPCで複数のピアゲートウェイ接続を設定できます。
* 同じプロジェクト内では、複数のVPCから1つのピアゲートウェイへの接続を設定できます。
* IKE v2接続がサポートされます。
* VPNゲートウェイサービスが提供されるリージョン間でVPN接続が可能です（機器はFortinet - Fortigate Seriesを設定）。
* v2のリリースに伴い、v1 VPNゲートウェイは新規作成が制限されます。

##### Load Balancer
* ロードバランサーのCPU使用率、リスナー単位の統計、ソケットの接続状態などの指標をCloud Monitoringサービスを通じて確認できるよう追加されました。

<a id="may-27-2025"></a>
### 2025. 05. 27. { #may-27-2025 }

<a id="may-27-2025-added-features"></a>
#### 機能追加

##### NAT Gateway
* Public API に NAT Gateway 関連の API が追加されました。[NAT Gateway API ガイド](/Network/NAT%20Gateway/ja/public-api/)を参照してください。

##### Security Groups
* Public API に Security Groups の接続情報照会 API が追加されました。[Security Groups API ガイド](/Network/Security%20Groups/ja/public-api/)を参照してください。
* セキュリティルールの一括作成、セキュリティルール一覧のダウンロード機能が追加されました。

##### Internet Gateway
* Public API に Internet Gateway 関連の API が追加されました。[Internet Gateway API ガイド](/Network/Internet%20Gateway/ja/public-api/)を参照してください。

##### Colocation Gateway
* Public API に Colocation Gateway 関連の API が追加されました。[Colocation Gateway API ガイド](/Network/Colocation%20Gateway/ja/public-api/)を参照してください。

##### Private DNS
* Public API に Private DNS 関連の API が追加されました。[Private DNS API ガイド](/Network/Private%20DNS/ja/public-api/)を参照してください。

##### Floating IP
* Floating IP にラベル設定機能が追加されました。[Floating IP コンソール使用ガイド](/Network/Floating%20IP/ja/console-guide/)を参照してください。

##### Flow Log
* Region peering gateway、Project peering gateway、Colocation gateway、ロードバランサーのネットワークインターフェイスを対象に Flow Log を作成できるよう機能が追加されました。

<a id="may-27-2025-feature-updates"></a>
#### 機能改善

##### Flow Log
* Flow Log のファイルを OBS に保存する際、フォルダとファイル名を自由に編集できるよう改善されました。

<a id="april-29-2025"></a>
### 2025. 04. 29. { #april-29-2025 }

<a id="april-29-2025-feature-updates"></a>
#### 機能変更

##### DNS Plus
* レコードセットの TTL の最小値を 1 から 10 に変更しました。

<a id="march-4-2025"></a>
### 2025. 03. 04. { #march-4-2025 }

<a id="march-4-2025-feature-updates"></a>
#### 機能改善

##### Service Gateway
* Service Gateway 作成時に、ユーザーが IP アドレスを指定して作成できるよう改善されました。

##### Load Balancer
* L7 ポリシーで L7 Redirect URL をより詳細に設定できるよう改善しました。
* メンバーグループごとの固定ポート番号ではなく、メンバーごとのポート番号に対してヘルスチェックできるよう改善されました。

##### Flow Log
* Transit Hub の接続を対象に Flow Log を作成できるよう機能が追加されました。
* Flow Log収集対象に VPC および Subnet が追加されました。

##### Routing
* ルートに説明項目が追加されました。ルートの作成または変更時に値を入力でき、ルート情報に表示されます。
* ルートの CIDR、ゲートウェイ項目を変更する機能が追加されました。

<a id="november-26-2024"></a>
### 2024. 11. 26. { #november-26-2024 }

<a id="november-26-2024-feature-updates"></a>
#### 機能改善

##### Peering Gateway
* ピアリングに説明項目が追加されました。ピアリングの作成または変更時に、そのピアリングに関する説明を入力でき、ピアリングの基本情報に表示されます。

##### Flow Log
* gzip圧縮機能が追加されました。
* Flow Log がサポートする統計提供情報項目の中から、ユーザーが希望する項目のみを選択して記録できるよう改善されました。サポートする統計項目については、[Flowlog 概要](/Network/Flow%20Log/ja/overview/)を参照してください。

<a id="august-27-2024"></a>
### 2024. 08. 27. { #august-27-2024 }

<a id="august-27-2024-added-features"></a>
#### 機能追加

##### Flow Log
* Flow Log 新規サービスが追加されました。ネットワークインターフェイスで送受信される IP トラフィック情報を収集・保存できます。
    * Flow Log は韓国(平村)リージョンと韓国(板橋)リージョンでのみ利用できます。

##### Routing
* Public API にルーティングテーブルに関連するゲートウェイ情報照会 API が追加されました。[VPC API ガイド](/Network/VPC/ja/public-api/)を参照してください。

##### VPN Gateway
* Diffie-Hellman グループ 14、15、16、17、18、19、20、21、27、28 をサポートします。


<a id="august-27-2024-feature-updates"></a>
#### 機能改善

##### Load Balancer
* メンバーごとにポート番号を指定できます。

##### Region Peering
* 他のプロジェクトで作成された VPC に接続できる機能が追加されました。

##### Transit Hub
* マルチキャストドメインを他のプロジェクトと共有できる機能が追加されました。他のプロジェクトで作成された VPC 間でマルチキャスト通信ができます。

<a id="may-28-2024"></a>
### 2024. 05. 28. { #may-28-2024 }

<a id="may-28-2024-added-features"></a>
#### 機能追加

##### Load Balancer
* L7ロードバランシング機能が追加されました。[ロードバランサーユーザーガイド](/Network/Load%20Balancer/ja/console-guide/)を参照してください。

##### VPN Gateway
* ピアゲートウェイ装置にCisco - Firepower 1000 Seriesが追加されました。

##### Network ACL
* 韓国(パンギョ)リージョンにNetwork ACL機能が追加されました。
* Network ACLがCloudTrailに連携されました。

##### Service Gateway
* Public APIにService Gateway関連APIが追加されました。[Service Gateway APIガイド](/Network/Service%20Gateway/ja/public-api/)を参照してください。

##### DNS Plus
* GSLBヘルスチェックで、ヘルスチェックリクエストのヘッダー、ヘルスチェック周期、最大応答待機時間、最大再試行回数の設定機能が追加されました。

<a id="may-28-2024-feature-updates"></a>
#### 機能改善

##### Service Gateway
* 基本情報タブにAPIエンドポイントドメイン項目が追加されました。

<a id="march-26-2024"></a>
### 2024. 03. 26. { #march-26-2024 }

<a id="march-26-2024-added-features"></a>
#### 機能追加

##### Transit Hub
* Public APIにTransit Hub関連APIが追加されました。[Transit Hub APIガイド](/Network/Transit%20Hub/ja/public-api/)を参照してください。

<a id="march-12-2024"></a>
### 2024. 03. 12. { #march-12-2024 }

<a id="march-12-2024-feature-updates"></a>
#### 機能改善

##### DNS Plus
* SPFレコードセットタイプのサポートが中止されました。TXTレコードセットタイプで代わりに使用できます。
    * 詳細については、[[RFC 7208#section-14.1]](https://datatracker.ietf.org/doc/html/rfc7208#section-14.1)で確認できます。

<a id="february-27-2024"></a>
### 2024. 02. 27. { #february-27-2024 }

<a id="february-27-2024-added-features"></a>
#### 機能追加

##### Floating IP
* Floating IP削除保護機能が追加されました。

##### Load Balancer
* ロードバランサー削除保護機能が追加されました。
* Public APIにL7ロードバランシング関連APIが追加されました。[ロードバランサーAPIガイド](https://docs.nhncloud.com/ko/Network/Load%20Balancer/ko/public-api/)を参照してください。

<a id="february-27-2024-feature-updates"></a>
#### 機能改善/変更

##### Private DNS

- レコードセットに説明フィールドが追加されました。

##### Transit Hub
* ルーティングルールのパケット処理方式に、パケットを破棄するBLACKHOLEが追加されました。

<a id="november-28-2023"></a>
### 2023. 11. 28. { #november-28-2023 }

<a id="november-28-2023-added-features"></a>
#### 機能追加

##### Load Balancer

* ロードバランサーにサブネット静的ルート適用機能が追加されました。ロードバランサーが属するサブネットに設定された静的ルートを、インスタンスだけでなくロードバランサーにも適用できます。

##### Private DNS

* Private DNS新規サービスが追加されました。VPCごとに独立したDNSを構成できます。
  * Private DNSは韓国(ピョンチョン)リージョンと韓国(パンギョ)リージョンでのみ利用できます。

<a id="august-29-2023"></a>
### 2023. 08. 29. { #august-29-2023 }

<a id="august-29-2023-added-features"></a>
#### 機能追加

##### Transit Hub

* Transit Hub の新規サービスが追加されました。VPC を中央集約接続で管理し、接続されたリソース間のルーティングとマルチキャスト通信を提供します。
    * Transit Hub は韓国(坪村)リージョンと韓国(板橋)リージョンでのみ利用できます。

##### VPN Gateway

* 韓国(板橋)リージョンに VPN Gateway 機能が追加されました。

##### NAT インスタンス

* 韓国(板橋)リージョンに NAT インスタンス機能が追加されました。

##### VPC

* Public API に Routing API が追加されました。詳細については、[VPC API ガイド](https://docs.nhncloud.com/ko/Network/VPC/ko/public-api/)を参照してください。

##### Network ACL

* 韓国(坪村) Public API がリリースされました。詳細については、[Network ACL API ガイド](https://docs.nhncloud.com/ko/Network/Network%20ACL/ko/public-api/)を参照してください。

<a id="may-30-2023"></a>
### 2023. 05. 30. { #may-30-2023 }

<a id="may-30-2023-feature-updates"></a>
#### 機能改善

##### Network Interface

* Network Interface UI の改善
    * 検索機能が追加されました。
    * デバイス名を表示するように改善されました。

<a id="march-28-2023"></a>
### 2023. 03. 28. { #march-28-2023 }

<a id="march-28-2023-added-features"></a>
#### 機能追加

##### Traffic Mirroring

* Traffic Mirroring 機能が追加されました。パケットをキャプチャして、コンテンツセキュリティ、脅威分析、トラブルシューティングなどの目的を持つ検知ツールにルーティングできます。
    * トラフィックミラーリングは韓国(坪村)リージョンと韓国(板橋)リージョンでのみ利用できます。

<a id="march-28-2023-feature-updates"></a>
#### 機能改善

##### VPC

* Public API に VPC および VPC Subnet API が追加されました。詳細については、[VPC API ユーザーガイド](https://docs.nhncloud.com/ko/Network/VPC/ko/public-api/)を参照してください。

<a id="march-28-2023-march-28-2023-feature-updates"></a>
#### 機能変更

##### VPC, Floating IP, Security Groups, Load Balancer

* APIエンドポイントアドレスが変更されました。

<a id="january-31-2023"></a>
### 2023. 01. 31. { #january-31-2023 }

<a id="january-31-2023-feature-updates"></a>
#### 機能改善

##### Colocation Gateway

* [韓国 坪村/板橋 リージョン] コロケーションゲートウェイにルートを設定できる機能が追加されました。

##### Service Gateway

* 同一 VPC 内のサービスゲートウェイのみ通信が可能という制約が削除されました。
* ピアリングゲートウェイ、コロケーションゲートウェイを経由して、他の VPC のサービスゲートウェイを利用できます。

<a id="november-29-2022"></a>
### 2022. 11. 29. { #november-29-2022 }

<a id="november-29-2022-added-features"></a>
#### 機能追加

##### Peering Gateway

* [韓国 坪村/板橋 リージョン] ピアリング、プロジェクトピアリング、リージョン間ピアリングにルートを設定できる機能が追加されました。

<a id="october-4-2022"></a>
### 2022. 10. 04. { #october-4-2022 }

<a id="october-4-2022-feature-updates"></a>
#### 機能改善

##### Service Gateway

* 対応サービスの追加
    * NCR

<a id="july-26-2022"></a>
### 2022. 07. 26. { #july-26-2022 }

<a id="july-26-2022-added-features"></a>
#### 機能追加

##### Load Balancer

* ヘルスチェック時にホストヘッダのフィールド値を変更できる機能が追加されました。

<a id="june-30-2022"></a>
### 2022. 06. 30. { #june-30-2022 }

<a id="june-30-2022-feature-updates"></a>
#### 機能改善

##### Service Gateway

* 対応サービスの追加
    * CloudTrail

<a id="may-24-2022"></a>
### 2022. 05. 24. { #may-24-2022 }

<a id="may-24-2022-added-features"></a>
#### 機能追加

##### Peering Gateway

* プロジェクトピアリング機能が追加されました。同じリージョン、異なるプロジェクトに作成された 2 つの VPC を接続できます。
    * プロジェクトピアリングは韓国(坪村)リージョンと韓国(板橋)リージョンでのみ利用できます。

##### VPN Gateway

* [韓国 坪村 リージョン] VPN Gateway 機能が追加されました。

##### NAT ゲートウェイ

* [韓国 板橋 リージョン] NAT ゲートウェイ機能が追加されました。

<a id="march-29-2022"></a>
### 2022. 03. 29. { #march-29-2022 }

<a id="march-29-2022-added-features"></a>
#### 機能追加

##### VPC

* サービスゲートウェイ機能が追加されました。サービスゲートウェイ IP を使用して、サービスゲートウェイ作成時に選択したサービスを接続できます。
    * サービスゲートウェイは韓国(坪村)リージョンと韓国(板橋)リージョンでのみ利用できます。
* リージョン間ピアリング機能が追加されました。異なるリージョンに作成された 2 つの VPC を接続できます。
    * リージョン間ピアリングは韓国(坪村)リージョンと韓国(板橋)リージョンでのみ利用できます。

<a id="january-18-2022"></a>
### 2022. 01. 18. { #january-18-2022 }

<a id="january-18-2022-added-features"></a>
#### 機能追加

##### VPC

* サブネットに静的ルート設定機能が追加されました。サブネット内のインスタンスに DHCP を介して配布する静的ルートを設定できます。
* 「中央集約ルーティングテーブル」の作成および変更機能が追加されました。

##### Network Interface

* 冗長化のための仮想 IP 作成機能が追加されました。仮想 IP として使用する IP を確保し、ルーティングテーブルで該当 IP へのルートを追加できます。
* インスタンスをゲートウェイ/ファイアウォールなどの用途で使用できるよう、ネットワークインターフェイスのセキュリティ設定解除機能が追加されました。

<a id="january-18-2022-feature-updates"></a>
#### 機能改善

##### Load Balancer

* TERMINATED_HTTPS プロトコルを使用するロードバランサーで TLS 1.3 バージョンを使用できるように改善されました。

<a id="august-24-2021"></a>
### 2021. 08. 24. { #august-24-2021 }

<a id="august-24-2021-added-features"></a>
#### 機能追加

##### DNS Plus

* レコードセットの一括作成機能が追加されました。

<a id="april-27-2021"></a>
### 2021. 04. 27. { #april-27-2021 }

<a id="april-27-2021-added-features"></a>
#### 機能追加

##### NAT インスタンス

* [韓国 坪村 リージョン] NAT インスタンス機能が追加されました。

##### Load Balancer

* [韓国 坪村 リージョン] 物理ロードバランサーをオンラインで作成できます。既存のロードバランサーとの変更点については、[ロードバランサーガイド](https://docs.toast.com/ko/Network/Load%20Balancer/ko/console-guide/#_19)を参照してください。

<a id="march-23-2021"></a>
### 2021. 03. 23. { #march-23-2021 }

<a id="march-23-2021-added-features"></a>
#### 機能追加

##### NAT ゲートウェイ

* [韓国 坪村 リージョン] NAT ゲートウェイ機能が追加されました。

##### Load Balancer

* [韓国/日本/米国 リージョン] 無効なリクエストのブロック機能が追加されました。
* [韓国/日本/米国 リージョン] 新しく作成されるロードバランサーのデフォルト接続制限数が 2,000 から 60,000 に変更されます。

<a id="february-6-2021"></a>
### 2021. 02. 06. { #february-6-2021 }

<a id="february-6-2021-feature-updates"></a>
#### 機能変更

##### VPC

* [韓国 板橋 リージョン] ルーティングテーブルのデフォルトルート(VPC アドレス領域全体へのローカルルート)が適用されない問題を修正しました。従来は、VPC 内のサブネットであっても、同じルーティングテーブルに接続されているサブネット間のみ通信が可能でしたが、異なるルーティングテーブルに接続されているサブネット間でも通信できるようになりました。

<a id="november-24-2020"></a>
### 2020. 11. 24. { #november-24-2020 }

<a id="november-24-2020-added-features"></a>
#### 機能追加

##### Network Interface

* Network Interface 機能が追加されました。

<a id="september-22-2020"></a>
### 2020. 09. 22. { #september-22-2020 }

<a id="september-22-2020-feature-updates"></a>
#### 機能改善

##### DNS Plus

* レコードセット編集時にレコードセットタイプの変更が可能になるよう改善されました。

<a id="august-25-2020"></a>
### 2020. 08. 25. { #august-25-2020 }

<a id="august-25-2020-added-features"></a>
#### 機能追加

##### Network ACL

* [韓国 坪村 リージョン] Network ACL 機能が追加されました。ACL 機能を使用して、プロトコル、IP、ポートごとにアクセスを制御できます。

##### Load Balancer

* Public API v2 が IP アクセス制御機能をサポートします。詳細については、[ロードバランサー API ガイド](https://docs.toast.com/ko/Network/Load%20Balancer/ko/public-api/#ip-acl)を参照してください。

<a id="june-23-2020"></a>
### 2020. 06. 23. { #june-23-2020 }

<a id="june-23-2020-feature-updates"></a>
#### 機能変更

##### VPC

* [韓国/日本/米国 リージョン] ルーティングテーブルのルート作成画面で、ゲートウェイ項目に IP を直接入力する方式から、IP を所有するデバイスを選択する方式に変更しました。ルーティングテーブルに明示的に接続していないサブネットのデバイスも選択できます。
* [韓国/日本/米国 リージョン] インターネットゲートウェイ一覧で IP 情報の代わりに接続されたルーティングテーブルの情報を表示するように変更しました。ルーティングテーブルのルートタブでも、接続されたインターネットゲートウェイの名前が表示されます。

<a id="may-26-2020"></a>
### 2020. 05. 26. { #may-26-2020 }

<a id="may-26-2020-feature-updates"></a>
#### 機能改善

##### VPC

* Public API v2がリリースされます。Public API v2はOpenstack APIと互換性があります。

##### Load Balancer

* ロードバランサーと同じVPCに属する別のサブネットのインスタンスをロードバランサーのメンバーとして登録できます。ロードバランサーが属するサブネットとインスタンスのサブネットがルーティングテーブルに接続されている必要があります。
* ロードバランサーが属するVPCがピアリング(peering)接続されている場合、ピアVPCに属するインスタンスをロードバランサーのメンバーとして登録できます。ピアVPCのデフォルトルーティングテーブルに接続されたサブネットのインスタンスのみ接続できます。
* ロードバランサーで複数のリスナーを運用する場合、すべてのリスナーに同じメンバーインスタンスを設定する必要がありましたが、リスナーごとに異なるメンバーインスタンスを設定できるようになりました。
* Public API v2がリリースされます。Public API v2はOpenstack APIと互換性があります。

<a id="march-24-2020"></a>
### 2020. 03. 24. { #march-24-2020 }

<a id="march-24-2020-feature-updates"></a>
#### 機能改善

##### Load Balancer

* Cert Managerサービスを通じた証明書管理機能が追加されました。
* Cert Managerサービスに証明書を登録し、リスナーに該当証明書を関連付けると、メールで証明書の有効期限アラームを受け取ることができます。

<a id="february-25-2020"></a>
### 2020. 02. 25. { #february-25-2020 }

<a id="february-25-2020-feature-updates"></a>
#### 機能改善

##### Security Group

* セキュリティグループルールに「説明」項目が追加されました。セキュリティグループルールごとに説明を追加できます。

<a id="december-24-2019"></a>
### 2019. 12. 24. { #december-24-2019 }

<a id="december-24-2019-added-features"></a>
#### 機能追加

##### DNS Plus

* エンドポイントサーバーのトラフィックを安定的にロードバランシングできるGSLB(Global Server Load Balancing)機能が追加されました。
* 生成されるGSLBドメインは、ルーティングルールに従ってDR(Disaster Recovery)、ランダムロードバランシング、グローバルロードバランシングで構成できます。
* Poolはルーティングルールを適用できる最小単位で、エンドポイントサーバーをグループ化する要素です。
* 定期的にPoolに含まれるエンドポイントサーバーにヘルスチェックを実行し、安定したサービスを提供できます。ヘルスチェックはHTTP/HTTPS/TCPをサポートします。

<a id="december-24-2019-feature-updates"></a>
#### 機能改善

##### DNS Plus

* レコードセットの作成/修正時に、CNAMEレコードセットタイプをユーザーのGSLBドメインを選択して入力できるように改善されました。

<a id="december-17-2019"></a>
### 2019. 12. 17. { #december-17-2019 }

<a id="december-17-2019-feature-updates"></a>
#### 機能改善
* [韓国/日本/米国リージョン] インスタンスに接続されているすべてのネットワークインターフェイスにそれぞれFloating IPを割り当てることができます。

<a id="october-29-2019"></a>
### 2019. 10. 29. { #october-29-2019 }

<a id="october-29-2019-feature-updates"></a>
#### 機能改善

##### Load Balancer

* [韓国/日本リージョン] チェーン証明書を登録する際に、証明書ファイルに含まれる個別証明書の形式が誤っている場合、Webコンソールで通知する機能が追加されました。

<a id="august-27-2019"></a>
### 2019. 08. 27. { #august-27-2019 }

<a id="august-27-2019-feature-updates"></a>
#### 機能改善

##### Load Balancer

* [韓国/日本リージョン] TERMINATED_HTTPSロードバランサーにクライアントと通信するTLSバージョンを指定できます。
    * ロードバランサーのTLSバージョン設定機能の詳細については、[ユーザーガイド](https://docs.toast.com/ko/Network/Load%20Balancer/ko/overview/#ssltls)を参照してください。

##### DNS Plus

* レコードセットの最大作成可能数を追加しました。DNS Zoneあたりレコードセットは最大5,000個まで作成できます。
* レコードセットの統計照会時に、CNAMEレコードセットタイプはAレコードセットタイプとAAAAレコードセットタイプをあわせて照会するように修正しました。

<a id="june-25-2019"></a>
### 2019. 06. 25. { #june-25-2019 }

<a id="june-25-2019-new-service-launch"></a>
#### 新規サービスリリース

##### DNS Plus

* DNS Plusはドメイン管理機能を提供するサービスです。
* DNSサーバーを簡単に設定できます。

<a id="may-30-2019"></a>
### 2019. 05. 30. { #may-30-2019 }

<a id="may-30-2019-feature-updates"></a>
#### 機能改善

##### Load Balancer

* [日本リージョン] IPアクセス制御機能を使用できます。
    * IPベースのアクセス制御機能をLoad Balancerで使用できます。
    * IPアクセス制御機能の詳細については、ユーザーガイドのドキュメントを参照してください。

<a id="may-28-2019"></a>
### 2019. 05. 28. { #may-28-2019 }

<a id="may-28-2019-feature-updates"></a>
#### 機能変更

##### VPC

* [韓国リージョン] ピアリング作成機能を再び使用できます。

<a id="april-25-2019"></a>
### 2019. 04. 25. { #april-25-2019 }

<a id="april-25-2019-feature-updates"></a>
#### 機能改善

##### Load Balancer

* IPアクセス制御機能を使用できます。
    * IPベースのアクセス制御機能をロードバランサーで使用できます。
    * IPアクセス制御機能の詳細については、ユーザーガイドのドキュメントを参照してください。
    * 電話にて設定をご依頼いただいた制御対象IPリストは、Defaultという名前のIPアクセス制御グループに自動的に反映されました。

<a id="december-27-2018"></a>
### 2018. 12. 27. { #december-27-2018 }

<a id="december-27-2018-feature-updates"></a>
#### 機能変更

##### VPC

* ピアリングされた2つのVPC間の通信時にパケットフラッディングが発生する可能性があるため、当面の間、新しいピアリング作成機能は提供しません。
	既存のピアリングの通信には問題がなく、ピアリング作成を除くその他の機能はそのまま提供されます。

<a id="november-27-2018"></a>
### 2018. 11. 27. { #november-27-2018 }

<a id="november-27-2018-bug-fixes"></a>
#### バグ修正

##### Load Balancer

* ロードバランサーにリスナーを追加作成する場合、無効化されたインスタンスに追加されたインスタンスメンバーが有効化された状態で作成されるバグを修正しました。

<a id="november-27-2018-feature-updates"></a>
#### 機能改善

##### Load Balancer

* ロードバランシング統計機能が追加され、次の統計情報がチャート形式で提供されます。
    * セッション数、クライアントの1秒あたりセッション増加量、インスタンスの1秒あたりセッション増加量、Inトラフィック量、Outトラフィック量、ロードバランシング除外数
    * 削除されたロードバランサー、リスナー、メンバーの統計情報は提供されません。
    * トラフィック量にはL2、L3、L4ヘッダーは含まれません。
    * 詳細については、ユーザーガイドのドキュメントを参照してください。

<a id="september-20-2018"></a>
### 2018. 09. 20. { #september-20-2018 }

<a id="september-20-2018-bug-fixes"></a>
#### バグ修正

##### Load Balancer

* Load BalancerにMemberとして登録されたInstanceを削除する際に、一部のListenerのMemberが残ってしまう問題を修正しました。

<a id="september-20-2018-feature-updates"></a>
#### 機能改善

##### Load Balancer

* 専用ロードバランサーサービスが追加されました。
* 専用ロードバランサーはハードウェアリソースを専有して生成されるため、1Gbpsの帯域幅と48万同時セッションをサポートします。

<a id="august-28-2018"></a>
### 2018. 08. 28. { #august-28-2018 }

<a id="august-28-2018-bug-fixes"></a>
#### バグ修正

##### VPC

* ルートが存在するサブネットを持つVPCを削除しようとする問題を修正しました。

<a id="august-28-2018-feature-updates"></a>
#### 機能変更

##### VPC

* サブネット、ルーティングテーブル、ルートの最大作成可能数を調整しました。
* VPCのリソースごとの最大作成可能数は、各リソース作成ウィンドウの右側の説明部分で確認できます。
    * サブネット：VPCあたり10個まで作成できます。
    * ルーティングテーブル：VPCあたり10個まで作成できます。
    * ルート：ルーティングテーブルあたり10個まで作成できます。

##### Load Balancer

* TCP、HTTPSプロトコルを使用する場合、クライアントのIPを取得するためにProxy Protocolを有効にできます。
* Load BalancerのKeepalive timeout値を設定できます。

<a id="april-24-2018"></a>
### 2018. 04. 24. { #april-24-2018 }

<a id="april-24-2018-bug-fixes"></a>
#### バグ修正

##### VPC

* ピアリング時にローカルVPCのインスタンスからピアVPCのロードバランサーへの接続が正常に行えない問題を修正しました。

<a id="april-24-2018-feature-updates"></a>
#### 機能改善

##### VPC

* VPC、サブネット、ルーティングテーブル、インターネットゲートウェイの概要ページで、接続されたリソース情報を確認できます。

##### Floating IP

* Floating IP一覧にページネーション機能を適用しました。

##### Security Group

* Ruleの編集機能が追加されました。

##### Load Balancer

* Keepalive Timeoutを5分に変更しました。
* Listenerのセッション制限値を最大60,000まで設定できます。

<a id="march-22-2018"></a>
### 2018. 03. 22. { #march-22-2018 }

<a id="march-22-2018-bug-fixes"></a>
#### バグ修正

##### VPC

* 新しく追加したサブネットにインスタンスを接続すると、DHCP経由でIPを取得できない問題を修正しました。
* ルーティングポリシーを追加する際に、既存のルーティングポリシーのターゲットと同一のターゲットを入力できる問題を修正しました。
* Floating IPが接続されたインスタンスで、断続的に別のサブネットに位置するインスタンスと通信できない問題を修正しました。

<a id="february-22-2018"></a>
### 2018. 02. 22. { #february-22-2018 }

<a id="february-22-2018-bug-fixes"></a>
#### バグ修正

##### VPC

* Floating IPが接続されたインスタンスからローカルネットワークへトラフィックが転送されない問題を修正しました。

<a id="february-22-2018-feature-updates"></a>
#### 機能改善

##### Networkの基本モデルとしてVPCを導入しました。

* 複数のサブネットを使用できます。
* サブネット単位でポートを作成してインスタンスに接続できます。
* ルーティングポリシーを追加できます。
* VPC間の通信のためにピアリング機能が追加されました。
* インスタンスに複数のVPCポートを追加または削除できます。
* 詳細については、VPC Overviewとユーザーガイドを参照してください。

<a id="november-23-2017"></a>
### 2017. 11. 23. { #november-23-2017 }

<a id="november-23-2017-bug-fixes"></a>
#### バグ修正

##### Load Balancer
* Load Balancer作成時にリスナーの接続制限値が誤って表示される現象を修正しました。

<a id="october-26-2017"></a>
### 2017. 10. 26. { #october-26-2017 }

<a id="october-26-2017-bug-fixes"></a>
#### バグ修正

##### Load Balancer
* Load Balancer作成時に証明書が登録されないバグを修正しました。

<a id="september-21-2017"></a>
### 2017. 09. 21. { #september-21-2017 }

<a id="september-21-2017-added-features"></a>
#### 機能追加

##### Public API追加

* Object Storageに続き、Compute&NetworkサービスをAPIを使用して管理できます。
* 現在は限られた機能のみ利用可能で、今後のAPI追加を通じて機能が拡張されました。

<a id="september-21-2017-bug-fixes"></a>
#### バグ修正

* ProjectにAdmin権限のないユーザーがセキュリティグループ(security group)を修正できないように修正されました。
* ProjectにAdmin権限のないユーザーにはNetworkメニューが表示されないように修正されました。

<a id="august-24-2017"></a>
### 2017. 08. 24. { #august-24-2017 }

<a id="august-24-2017-bug-fixes"></a>
#### バグ修正

##### Load Balancer
* Load Balancerサービスのセッション持続性項目が正しく表示されないバグが修正されました。

<a id="april-20-2017"></a>
### 2017. 04. 20. { #april-20-2017 }

<a id="april-20-2017-bug-fixes"></a>
#### バグ修正
##### Load Balancer
* Listenerへの証明書ファイルアップロード時に、断続的に証明書登録ウィンドウが消えるバグが修正されました。

<a id="march-23-2017"></a>
### 2017. 03. 23. { #march-23-2017 }

<a id="march-23-2017-bug-fixes"></a>
#### バグ修正
##### Floating IP
* Floating IP接続ポップアップで「作成」ボタンが表示されない問題が修正されました。

<a id="february-23-2017"></a>
### 2017. 02. 23. { #february-23-2017 }

<a id="february-23-2017-feature-updates"></a>
#### 機能改善/変更

##### Load Balancer

* ロードバランサーに登録されたリスナーが1つの場合、削除できないことを通知するように変更します。
	  * 従来も削除はできませんでしたが、ユーザーへの通知がなく混乱を招いていました。
	  * ユーザーに対して削除できない旨を明示的にメッセージで通知するように変更します。

##### Floating IP

* Floating IP削除時にインスタンスまたはロードバランサーが接続されている場合、削除できないように変更します。
	  * 従来はインスタンスやロードバランサーが接続されているFloating IPを削除できたため、サービスに障害が発生する可能性がありました。
	  * このような誤操作を事前に防止できるよう、接続のあるFloating IPは削除できないように変更します。
* 名称変更：「ポート」→「ネットワークインターフェイス」
	  * インスタンスにFloating IPを割り当てる際の対象名称を、従来の「ポート」から「ネットワークインターフェイス」に変更します。

<a id="january-19-2017"></a>
### 2017. 01. 19. { #january-19-2017 }

<a id="january-19-2017-bug-fixes"></a>
#### バグ修正
##### Load Balancer
* Load Balancer作成時に接続制限の設定が適用されない問題を修正しました。

<a id="december-22-2016"></a>
### 2016. 12. 22. { #december-22-2016 }

<a id="december-22-2016-bug-fixes"></a>
#### バグ修正

##### Load Balancer
* Health Check ProtocolがTCPの場合にListenerの内容を編集できない問題を修正しました。

##### Floating IP
* Floating IPに接続されたLoad Balancerの名前が表示されない問題を修正しました。

##### Security Group
* 重複したRuleを追加した際にセキュリティグループの一覧が消える問題を修正しました。

<a id="december-8-2016"></a>
### 2016. 12. 08. { #december-8-2016 }

<a id="december-8-2016-bug-fixes"></a>
#### バグ修正

##### Load Balancer
* Load BalancerのHeath check URLが表示されない問題を修正しました。
* Listener編集ボタンクリック時に、登録済みのHealth Check URLではなく「/」が表示される問題を修正しました。

<a id="november-29-2016"></a>
### 2016. 11. 29. { #november-29-2016 }

<a id="november-29-2016-bug-fixes"></a>
#### バグ修正
##### Load Balancer
* TERMINATED_HTTPS タイプのLoad Balancer作成が失敗する問題を修正しました。

<a id="november-24-2016"></a>
### 2016. 11. 24. { #november-24-2016 }

<a id="november-24-2016-feature-updates"></a>
#### 機能改善/変更
##### Load Balancer
* Load BalancerのListenerごとのセッション制限値を表示するように変更しました。

<a id="november-24-2016-bug-fixes"></a>
#### バグ修正
##### Load Balancer
* 特定のProjectでLoad Balancer作成が失敗する問題を修正しました。

<a id="august-4-2016"></a>
### 2016. 08. 04. { #august-4-2016 }

<a id="august-4-2016-feature-updates"></a>
#### 機能改善/変更
##### Load Balancer
* Load BalancerのSSL offloading機能を追加しました。

<a id="august-4-2016-bug-fixes"></a>
#### バグ修正
##### Load Balancer
* Load Balancer削除時に断続的に正常終了しない問題を修正しました。