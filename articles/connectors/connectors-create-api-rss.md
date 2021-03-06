---
title: Azure Logic Apps での RSS コネクタ | Microsoft Docs
description: Azure App Service を使用してロジック アプリを作成します。 RSS コネクタを使用して、フィード アイテムを発行および取得できます。 また、新しいアイテムがフィードに発行されたときに操作をトリガーすることもできます。
services: logic-apps
documentationcenter: .net,nodejs,java
author: ecfan
manager: anneta
editor: ''
tags: connectors
ms.assetid: a10a6277-ed29-4e68-a881-ccdad6fd0ad8
ms.service: logic-apps
ms.devlang: multiple
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: integration
ms.date: 08/18/2016
ms.author: estfan; ladocs
ms.openlocfilehash: 493ee8a961e5d5a57c6276868a55b524dec28018
ms.sourcegitcommit: 8aab1aab0135fad24987a311b42a1c25a839e9f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/16/2018
---
# <a name="get-started-with-the-rss-connector"></a>RSS コネクタの使用
RSS は、ブログ記事やニュースのヘッドラインのように、頻繁に更新されるコンテンツを発行するために使用する一般的な Web 配信形式です。  多くのコンテンツ発行元は、ユーザーがサブスクライブすることができる RSS フィードを提供します。  新しい項目を RSS フィードに発行するときに、RSS コネクタを使用してフィード情報を取得しフローをトリガーします。

まず、ロジック アプリを作成します。[ロジック アプリの作成](../logic-apps/quickstart-create-first-logic-app-workflow.md)に関する記事を参照してください。

## <a name="create-a-connection-to-rss"></a>RSS への接続の作成
> [!INCLUDE [Steps to create a connection to an RSS feed](../../includes/connectors-create-api-rss.md)]
> 

## <a name="connector-specific-details"></a>コネクタ固有の詳細

[コネクタの詳細](/connectors/rss/)に関するページに、Swagger で定義されているトリガーとアクション、さらに制限が記載されています。

## <a name="more-connectors"></a>その他のコネクタ
[API リスト](apis-list.md)に戻ります。