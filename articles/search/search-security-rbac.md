---
title: ポータルで Azure Search 管理アクセス用の RBAC ロールを設定する |Microsoft Docs
description: Azure Portal でのロールベースの管理制御。
author: HeidiSteen
manager: cgronlun
services: search
ms.service: search
ms.topic: conceptual
ms.date: 03/20/2018
ms.author: heidist
ms.openlocfilehash: 1a463c9eb52ffe2a667cdeace7478e67233a0806
ms.sourcegitcommit: fa493b66552af11260db48d89e3ddfcdcb5e3152
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2018
---
# <a name="set-rbac-roles-for-administrative-access"></a>管理アクセス用の RBAC ロールを設定する

Azure では、ポータルまたはリソース マネージャー API で管理するすべてのサービスに対して、 [グローバルなロールベースの承認モデル](../role-based-access-control/role-assignments-portal.md) を用意しています。 所有者、共同作成者、および閲覧者のロールによって、各ロールに割り当てられる Active Directory のユーザー、グループ、およびセキュリティ プリンシパルに対する*サービス管理*のレベルが決まります。 

> [!Note]
> インデックスの一部やドキュメントのサブセットを保護するためのロールベースのアクセス制御はありません。 検索結果に対する ID ベースのアクセスの場合は、セキュリティ フィルターを作成して ID 別に結果に手を入れ、要求者がアクセスしてはいけないドキュメントを削除します。 詳細については、[セキュリティ フィルター](search-security-trimming-for-azure-search.md)と[Active Directory を使用してセキュリティ保護する](search-security-trimming-for-azure-search-with-aad.md)を参照してください。

## <a name="management-tasks-by-role"></a>ロール別の管理タスク

Azure Search の場合、ロールは次の管理タスクをサポートするアクセス許可レベルに関連付けられています。

| 役割 | タスク |
| --- | --- |
| Owner |API キー、インデックス、インデクサー、インデクサー データ ソース、インデクサー スケジュールなど、サービス上のサービスやオブジェクトを作成または削除します。<p>カウントとストレージ サイズなど、サービスの状態を表示します。<p>ロール メンバーシップを追加または削除します (所有者のみがロール メンバーシップを管理できます)。<p>サブスクリプション管理者とサービス所有者には、所有者ロールに自動メンバーシップがあります。 |
| Contributor |RBAC ロール管理を除き、アクセス レベルは所有者と同じです。 たとえば、共同作成者はオブジェクトの作成や削除、[API キー](search-security-api-keys.md)の表示や再生成は可能ですが、ロール メンバーシップは変更できません。 |
| [Search Service Contributor 組み込みロール](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#search-service-contributor) | 共同作成者ロールと同じです。 |
| Reader |サービスの要点とメトリックを表示します。 このロールのメンバーは、インデックス、インデクサー、データ ソース、または重要な情報を表示できません。  |

ロールは、サービス エンドポイントへのアクセス権を付与しません。 インデックスの管理、インデックスの作成、検索データのクエリなど、検索サービスの操作は、ロールではなく API キーによって制御されます。 詳細については、「[API キーを管理する](search-security-api-keys.md)」をご覧ください。

## <a name="see-also"></a>関連項目

+ [PowerShell を使用した管理](search-manage-powershell.md) 
+ [Performance and optimization in Azure Search](search-performance-optimization.md) (Azure Search のパフォーマンスと最適化)
+ [Azure Portal でのロールベースの Access Control の基礎を確認する](../role-based-access-control/overview.md)