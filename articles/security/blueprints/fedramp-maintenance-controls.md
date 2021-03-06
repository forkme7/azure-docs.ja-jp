---
title: "Azure のセキュリティとコンプライアンスのブループリント - FedRAMP Web アプリケーションの自動化 - メンテナンス"
description: "FedRAMP Web アプリケーションの自動化 - メンテナンス"
services: security
documentationcenter: na
author: jomolesk
manager: mbaldwin
editor: tomsh
ms.assetid: 53acae01-bea9-4570-a9bc-734ff65262ba
ms.service: security
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/08/2018
ms.author: jomolesk
ms.openlocfilehash: de7dd5b4651f7f74d90d9d026af71cd676c720e6
ms.sourcegitcommit: 4723859f545bccc38a515192cf86dcf7ba0c0a67
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/11/2018
---
# <a name="maintenance-ma"></a>メンテナンス (MA)

> [!NOTE]
> この管理策は、NIST および米国商務省により、NIST Special Publication 800-53 Revision 4 の一部として定義されています。 各コントロールのテスト手順とガイダンスについては、NIST 800-53 Rev. 4 を参照してください。

## <a name="nist-800-53-control-ma-1"></a>NIST 800-53 Control MA-1

#### <a name="system-maintenance-policy-and-procedures"></a>システム メンテナンスのポリシーと手順

**MA-1**: 組織は、目的、スコープ、役割、責任、経営陣のコミットメント、組織エンティティ間の調整、およびコンプライアンスを取り上げたシステム メンテナンス ポリシーと、システム メンテナンス ポリシーおよびシステム メンテナンスの関連するコントロールの実装を容易にする手順を策定、文書化し、[割り当て: 組織が定義した担当者または役割]に周知徹底する。また、現在のシステム メンテナンス ポリシーを[割り当て: 組織が定義した頻度]、システム メンテナンスの手順を[割り当て: 組織が定義した頻度]見直し、更新する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様のエンタープライズ レベルのシステム メンテナンスのポリシーと手順で、このコントロールに対処できます。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-2a"></a>NIST 800-53 Control MA-2.a

#### <a name="controlled-maintenance"></a>メンテナンスの管理

**MA-2.a** 組織は、製造元またはベンダーの仕様や組織の要件に従って、情報システム コンポーネントのメンテナンスと修復をスケジュールし、実施すると共に、これらを文書化し、記録を確認する。

**責任:** `Customer Only`

|||
|---|---|
| **お客様** | お客様は、メンテナンスの管理に対して責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用されません |


 ## <a name="nist-800-53-control-ma-2b"></a>NIST 800-53 Control MA-2.b

#### <a name="controlled-maintenance"></a>メンテナンスの管理

**MA-2.b** 組織は、現場で実施するか、リモートから実施するかを問わず、また、機器を現場で点検するか、別の場所に移すかを問わず、すべてのメンテナンス作業を承認し、監視する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様は、メンテナンスの管理に対して責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-2c"></a>NIST 800-53 Control MA-2.c

#### <a name="controlled-maintenance"></a>メンテナンスの管理

**MA-2.c** 組織では、敷地外でのメンテナンスまたは修復のために、情報システムまたはシステム コンポーネントを組織の施設から移動することを、[割り当て: 組織が定義した担当者または役割]が明示的に承認する必要がある。

**責任:** `Azure Only`

|||
|---|---|
| **お客様** | 顧客は、Azure データセンターのどのシステム リソースにも物理的なアクセスはできません。 |
| **プロバイダー (Microsoft Azure)** | Microsoft Azure では、資産 (ネットワーク デバイスやサーバーなど) を敷地外に移動する必要がある場合に資産所有者の明示的な承認を得る必要があります。 |


 ## <a name="nist-800-53-control-ma-2d"></a>NIST 800-53 Control MA-2.d

#### <a name="controlled-maintenance"></a>メンテナンスの管理

**MA-2.d** 組織は、敷地外でのメンテナンスまたは修復のために組織の施設から移動する前に、機器をサニタイズして関連するメディアからすべての情報を削除する。

**責任:** `Azure Only`

|||
|---|---|
| **顧客** | 顧客は、Azure データセンターのどのシステム リソースにも物理的なアクセスはできません。 |
| **プロバイダー (Microsoft Azure)** | Microsoft Azure の Asset Protection Standard では、資産の敷地外への移動に必要な資産取扱い予防策を定めています。 Asset Protection Standard では、データセンターから移動する前に、NIST SP 800-88「Guidelines for Media Sanitization (メディアのサニタイズに関するガイドライン)」に合致する方法で、データ ストレージ資産を消去する必要があります。 |


 ## <a name="nist-800-53-control-ma-2e"></a>NIST 800-53 Control MA-2.e

#### <a name="controlled-maintenance"></a>メンテナンスの管理

**MA-2.e** 組織は、影響を受ける可能性のあるすべてのセキュリティ コントロールをチェックして、メンテナンスまたは修復作業後もコントロールが正常に機能していることを確認する。

**責任:** `Customer Only`

|||
|---|---|
| **お客様** | お客様は、メンテナンスの管理に対して責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-2f"></a>NIST 800-53 Control MA-2.f

#### <a name="controlled-maintenance"></a>メンテナンスの管理

**MA-2.f** 組織は、[割り当て: 組織が定義したメンテナンス関連情報]を組織のメンテナンス記録に含める。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様は、メンテナンスの管理に対して責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ### <a name="nist-800-53-control-ma-2-2a"></a>NIST 800-53 Control MA-2 (2).a

#### <a name="controlled-maintenance--automated-maintenance-activities"></a>メンテナンスの管理 | メンテナンス作業の自動化

**MA-2 (2).a** 組織は、メンテナンスと修復をスケジュール、実施、文書化する自動化されたメカニズムを使用する。

**責任:** `Customer Only`

|||
|---|---|
| **お客様** | お客様は、メンテナンス作業を自動化する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ### <a name="nist-800-53-control-ma-2-2b"></a>NIST 800-53 Control MA-2 (2).b

#### <a name="controlled-maintenance--automated-maintenance-activities"></a>メンテナンスの管理 | メンテナンス作業の自動化

**MA-2 (2).b** 組織は、要求、スケジュール設定、実施、完了まで、すべてのメンテナンスおよび修復作業の最新の正確かつ完全な記録を作成する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様は、メンテナンス作業を自動化する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-3"></a>NIST 800-53 Control MA-3

#### <a name="maintenance-tools"></a>メンテナンス ツール

**MA-3** 組織は、情報システムのメンテナンス ツールを承認、制御、および監視する。

**責任:** `Azure Only`

|||
|---|---|
| **顧客** | 顧客は、Azure データセンターのどのシステム リソースにも物理的なアクセスはできません。 |
| **プロバイダー (Microsoft Azure)** | Microsoft Azure では、複数のツールを使用してメンテナンスを実施します。 ソフトウェア メンテナンス ツールは、Microsoft Azure の変更およびリリース プロセスを通じて承認、制御、管理されます。 <br /> サイト サービス チームは、データセンター内で使用する承認済みのメンテナンス ツールのインベントリを管理しています (MA-3 を参照)。 メンテナンス担当者は、提供されたメンテナンス ツールを使用するよう指示されます。 データセンターで提供されていないツールを使用するには、データセンター管理部門の承認が必要です。 物理的な手工具 (ドライバー、レンチなど) は、このコントロールの対象外となります。 <br /> 各施設には、特殊なメンテナンス ツール (Fluke イーサ スコープ、Fluke ファイバー チャネル テスター、イーサネット トナーなど) を保管するための制限された物理的なロック ボックスまたはアクセス制御された部屋があります。サイト サービス チームは、インベントリの定期チェックを行い、すべてのツールの状態を確認しています。 ロック ボックスまたはメンテナンス保管室へのアクセスは、調査の際に利用できる、アクセス バッジ リーダーのログで追跡されます。 |


 ### <a name="nist-800-53-control-ma-3-1"></a>NIST 800-53 Control MA-3 (1)

#### <a name="maintenance-tools--inspect-tools"></a>メンテナンス ツール | ツールの検査

**MA-3 (1)** 組織は、メンテナンス担当者が施設に持ち込んだメンテナンス ツールを検査して、不適切または未承認の変更が行われていないかどうかを確認する。

**責任:** `Azure Only`

|||
|---|---|
| **顧客** | 顧客は、Azure データセンターのどのシステム リソースにも物理的なアクセスはできません。 |
| **プロバイダー (Microsoft Azure)** | Microsoft Azure のサイト サービス チームは、データセンター内で使用する承認済みのメンテナンス ツールのインベントリを管理しています (詳細については、MA-3 を参照)。 メンテナンス担当者は、提供されたメンテナンス ツールを使用するよう指示されます。 データセンターで提供されていないツールを使用するには、DCM の承認が必要です。 |


 ### <a name="nist-800-53-control-ma-3-2"></a>NIST 800-53 Control MA-3 (2)

#### <a name="maintenance-tools--inspect-media"></a>メンテナンス ツール | メディアの検査

**MA-3 (2)** 組織は、診断プログラムとテスト プログラムが含まれたメディアを情報システムで使用する前に、そのメディアに悪意のあるコードが含まれていないかどうかを確認する。

**責任:** `Azure Only`

|||
|---|---|
| **お客様** | 顧客は、Azure データセンターのどのシステム リソースにも物理的なアクセスはできません。 |
| **プロバイダー (Microsoft Azure)** | Microsoft Azure では、データセンター管理部門の承認を受けずに、Microsoft Azure データセンターの運用環境でモバイル コンピューティングまたはストレージ メディアを使用することを禁止しています。 Microsoft Azure データセンターの運用環境で、個人所有のメディアを使用することは禁止されています。 <br /> Microsoft Azure では、Microsoft Azure データセンターの運用環境で使用する前にノート PC を検査するプロセスを実装しています。 セキュリティ責任者は、運用環境でノート PC を使用している職員を呼び止め、ノート PC が検査済みで検査に合格していることを確認するよう訓練されています。 |


 ### <a name="nist-800-53-control-ma-3-3"></a>NIST 800-53 Control MA-3 (3)

#### <a name="maintenance-tools--prevent-unauthorized-removal"></a>メンテナンス ツール | 未承認の移動の防止

**MA-3 (3)** 組織は、機器に組織情報が含まれていないことを確認する、機器をサニタイズまたは破棄する、施設内に機器を保持する、または施設からの機器の移動を明示的に承認する[割り当て: 組織が定義した担当者または役割]から適用除外を受けることによって、組織情報を含むメンテナンス機器の未承認の移動を防止する。

**責任:** `Azure Only`

|||
|---|---|
| **お客様** | 顧客は、Azure データセンターのどのシステム リソースにも物理的なアクセスはできません。 |
| **プロバイダー (Microsoft Azure)** | Microsoft Azure では、施設内に保持され、移動されることのないデータセンター固有のメンテナンス ツールを使用しています。 各施設には、メンテナンス ツール (Fluke イーサ スコープ、Fluke ファイバー チャネル テスター、イーサネット トナーなど) を保管する制限された物理的なロック ボックスまたは保管室があります。メンテナンス ツールへの未承認のアクセスを禁止するために、ロック ボックスまたは保管室へのアクセスは DCAT で制御されています。 <br /> メンテナンス中、組織情報は MA-4 のコントロールによって保護されます。 ユーザーが組織情報にアクセスするには、特権アカウントと認証子が必要です。 |


 ## <a name="nist-800-53-control-ma-4a"></a>NIST 800-53 Control MA-4.a

#### <a name="nonlocal-maintenance"></a>非ローカル メンテナンス

**MA-4.a** 組織は、非ローカル メンテナンスおよび診断アクティビティを承認し、監視する。

**責任:** `Customer Only`

|||
|---|---|
| **お客様** | お客様は、お客様がデプロイしたオペレーティング システムで非ローカル メンテナンスを実施する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-4b"></a>NIST 800-53 Control MA-4.b

#### <a name="nonlocal-maintenance"></a>非ローカル メンテナンス

**MA-4.b** 組織は、組織のポリシーに適合し、情報システムのセキュリティ プランに記載されている場合にのみ、非ローカル メンテナンスおよび診断ツールの使用を許可する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様は、お客様がデプロイしたオペレーティング システムで非ローカル メンテナンスを実施する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-4c"></a>NIST 800-53 Control MA-4.c

#### <a name="nonlocal-maintenance"></a>非ローカル メンテナンス

**MA-4.c** 組織は、非ローカル メンテナンスおよび診断セッションを確立する際に強力な認証子を使用する。

**責任:** `Customer Only`

|||
|---|---|
| **お客様** | お客様は、お客様がデプロイしたオペレーティング システムで非ローカル メンテナンスを実施する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-4d"></a>NIST 800-53 Control MA-4.d

#### <a name="nonlocal-maintenance"></a>非ローカル メンテナンス

**MA-4.d** 組織は、非ローカル メンテナンスおよび診断アクティビティの記録を保持する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様は、お客様がデプロイしたオペレーティング システムで非ローカル メンテナンスを実施する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-4e"></a>NIST 800-53 Control MA-4.e

#### <a name="nonlocal-maintenance"></a>非ローカル メンテナンス

**MA-4.e** 組織は、非ローカル メンテナンスの完了時にセッションとネットワーク接続を終了する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様は、お客様がデプロイしたオペレーティング システムで非ローカル メンテナンスを実施する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ### <a name="nist-800-53-control-ma-4-2"></a>NIST 800-53 Control MA-4 (2)

#### <a name="nonlocal-maintenance--document-nonlocal-maintenance"></a>非ローカル メンテナンス | 非ローカル メンテナンスの文書化

**MA-4 (2)** 組織は、情報システムのセキュリティ プランに、非ローカル メンテナンスおよび診断用の接続の確立と使用に関するポリシーと手順を文書化する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様は、お客様がデプロイしたオペレーティング システムのセキュリティ プランに、非ローカル メンテナンスを文書化する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ### <a name="nist-800-53-control-ma-4-3"></a>NIST 800-53 Control MA-4 (3)

#### <a name="nonlocal-maintenance--comparable-security--sanitization"></a>非ローカル メンテナンス | 同等のセキュリティ/サニタイズ

**MA-4 (3)** 組織は、サービスを受けるシステムに実装されている機能と同等のセキュリティ機能を実装した情報システムから非ローカル メンテナンスおよび診断サービスを実行する必要がある。または、非ローカル メンテナンスまたは診断サービスの前に、サービスを受けるコンポーネントを情報システムから取り外し、組織の施設から移動させる前に (組織情報に関して) コンポーネントをサニタイズして、サービスの実行後、コンポーネントを情報システムに再接続する前に、(悪意のあるソフトウェアの可能性に関して) コンポーネントを検査し、サニタイズする。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様は、同等のセキュリティを備えた情報システムから、お客様がデプロイしたオペレーティング システムのすべての非ローカル メンテナンスを実施する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ### <a name="nist-800-53-control-ma-4-6"></a>NIST 800-53 Control MA-4 (6)

#### <a name="nonlocal-maintenance--cryptographic-protection"></a>非ローカル メンテナンス | 暗号化による保護

**MA-4 (6)** 情報システムは、非ローカル メンテナンスおよび診断の通信の整合性と機密性を保護する暗号化メカニズムを実装する。

**責任:** `Customer Only`

|||
|---|---|
| **お客様** | お客様は、お客様がデプロイしたオペレーティング システムの非ローカル メンテナンスおよび診断を実施する際に、暗号化メカニズムを実装する責任を負います。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-5a"></a>NIST 800-53 Control MA-5.a

#### <a name="maintenance-personnel"></a>メンテナンス担当者

**MA-5.a** 組織は、メンテナンス担当者の承認プロセスを確立し、承認されたメンテナンス組織または担当者の一覧を管理する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様のエンタープライズ レベルのシステム メンテナンス担当者の承認および付き添いプロセスで、このコントロールに対処できます。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-5b"></a>NIST 800-53 Control MA-5.b

#### <a name="maintenance-personnel"></a>メンテナンス担当者

**MA-5.b** 組織は、情報システムのメンテナンスを実施する、付き添いのいない担当者が、必要なアクセス承認を受けていることを確認する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様のエンタープライズ レベルのシステム メンテナンス担当者の承認および付き添いプロセスで、このコントロールに対処できます。 |
| **プロバイダー (Microsoft Azure)** | 適用されません |


 ## <a name="nist-800-53-control-ma-5c"></a>NIST 800-53 Control MA-5.c

#### <a name="maintenance-personnel"></a>メンテナンス担当者

**MA-5.c** 組織は、必要なアクセス承認を受けていない担当者によるメンテナンス作業を監督するために、必要なアクセス承認を受け、技術的能力がある組織職員を指名する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様のエンタープライズ レベルのシステム メンテナンス担当者の承認および付き添いプロセスで、このコントロールに対処できます。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ### <a name="nist-800-53-control-ma-5-1a"></a>NIST 800-53 Control MA-5 (1).a

#### <a name="maintenance-personnel--individuals-without-appropriate-access"></a>メンテナンス担当者 | 適切なアクセス権のない個人

**MA-5 (1).a** 組織は、適切なセキュリティ クリアランスがないか、米国市民ではないメンテナンス担当者を登用する際の手順を実装する。手順には次の要件を含める。情報システムのメンテナンスおよび診断アクティビティの実施中、必要なアクセス承認、クリアランス、または正式なアクセス承認を受けていないメンテナンス担当者には、十分なクリアランスを持ち、適切なアクセス承認を受け、技術的に資格のある承認済みの組織職員が付き添い、監督する。必要なアクセス承認、クリアランス、または正式なアクセス承認を受けていない担当者がメンテナンスまたは診断アクティビティを開始する前に、情報システム内の揮発性情報ストレージ コンポーネントをすべてサニタイズし、すべての不揮発性ストレージ メディアを取り外すか、システムから物理的に切断してセキュリティを確保する。

**責任:** `Customer Only`

|||
|---|---|
| **顧客** | お客様のエンタープライズ レベルのシステム メンテナンス担当者の承認および付き添いプロセスで、このコントロールに対処できます。 |
| **プロバイダー (Microsoft Azure)** | 適用されません |


 ### <a name="nist-800-53-control-ma-5-1b"></a>NIST 800-53 Control MA-5 (1).a

#### <a name="maintenance-personnel--individuals-without-appropriate-access"></a>メンテナンス担当者 | 適切なアクセス権のない個人

**MA-5 (1).b** 組織は、情報システム コンポーネントをサニタイズ、除去、またはシステムから切断できない場合に、代替のセキュリティ対策を策定し、実装する。

**責任:** `Customer Only`

|||
|---|---|
| **お客様** | お客様のエンタープライズ レベルのシステム メンテナンス担当者の承認および付き添いプロセスで、このコントロールに対処できます。 |
| **プロバイダー (Microsoft Azure)** | 適用外 |


 ## <a name="nist-800-53-control-ma-6"></a>NIST 800-53 Control MA-6

#### <a name="timely-maintenance"></a>タイムリーなメンテナンス

**MA-6** 組織は、故障してから[割り当て: 組織が定義した期間]内に、[割り当て: 組織が定義した情報システム コンポーネント]のメンテナンス サポートを受け、予備部品を入手する。

**責任:** `Azure Only`

|||
|---|---|
| **顧客** | 顧客は、Azure データセンターのどのシステム リソースにも物理的なアクセスはできません。 |
| **プロバイダー (Microsoft Azure)** | Microsoft Azure データセンターでは、重要なデータセンター インフラストラクチャ システムとデータセンター業務をサポートする常駐メンテナンス担当者を確保しています。 チームは、オンサイトに予備を保持する重要なセキュリティおよびテクノロジー システム コンポーネントを特定しました。 重要なシステムは N + 1 構成で設計され、サービスは回復性を備えるように設計されています。 これにより、データセンター管理チームは、サービスの中断やコンティンジェンシー計画の状況が発生した場合に、回復の目標を達成できます。 重要な情報システム サービスは、いずれかのデータセンターでのインシデントによってサービスが中断されないように、複数のデータセンターからプロビジョニングされます。 お客様のアプリケーションは、冗長性と回復性を実現するために複数のデータセンターにデプロイする必要があります。 |
