---
title: " Azure の Recovery Services コンテナーを削除する | Microsoft Docs "
description: "この記事では、Recovery Services コンテナーを削除する方法について説明します。 この記事には、コンテナーを削除しようとしているのに削除できない場合のトラブルシューティングの手順が含まれています。"
services: service-name
documentationcenter: dev-center-name
author: markgalioto
manager: carmonm
editor: 
ms.assetid: 5fa08157-2612-4020-bd90-f9e3c3bc1806
ms.service: backup
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: storage-backup-recovery
ms.date: 12/20/2017
ms.author: markgal;trinadhk
ms.openlocfilehash: 4f4a92159b01b197984130c15195419e1b166fd3
ms.sourcegitcommit: b5c6197f997aa6858f420302d375896360dd7ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/21/2017
---
# <a name="delete-a-recovery-services-vault"></a>Recovery Services コンテナーを削除する
この記事では、Azure Portal で Recovery Services コンテナーを削除する方法について説明します。 Backup コンテナーを保有していた場合は、Recovery Services コンテナーに変換されています。   

" *コンテナーにリソースが含まれていない場合*"、Recovery Services コンテナーの削除は、1 ステップの処理です。 Recovery Services コンテナーを削除する前に、コンテナー内のすべてのリソースを削除する必要があります。 リソースが含まれているコンテナーを削除しようとすると、次の図のようなエラーが表示されます。

![Vault deletion error](./media/backup-azure-delete-vault/vault-deletion-error.png) <br/>

コンテナーからリソースを消去しない限り、 **[再試行]** をクリックすると、同じエラーが発生し続けます。 このエラー メッセージが繰り返し表示されて先に進めない場合は、**[キャンセル]** をクリックし、以下の手順に従ってコンテナー内のリソースを削除します。

## <a name="removing-items-from-a-vault-protecting-a-vm"></a>VM を保護しているコンテナーからのアイテムの削除
既に Recovery Services コンテナーを開いている場合は、手順 2. に進みます。

1. Azure Portal を開き、削除するコンテナーをダッシュボードから開きます。

   Recovery Services コンテナーがダッシュボードにピン留めされていない場合は、ハブ メニューで **[その他のサービス]** をクリックし、リソースの一覧で「**Recovery Services**」と入力します。 入力を始めると、入力内容に基づいて、一覧がフィルター処理されます。 **[Recovery Services コンテナー]**をクリックします。

   ![Create Recovery Services Vault step 1](./media/backup-azure-delete-vault/open-recovery-services-vault.png) <br/>

   Recovery Services コンテナーの一覧が表示されます。 一覧で、削除するコンテナーを選択します。

   ![choose vault from list](./media/backup-azure-work-with-vaults/choose-vault-to-delete.png)
2. コンテナー ビューで、 **[要点]** ウィンドウを見ます。 コンテナーを削除するには、保護されているアイテムがあってはなりません。 **バックアップ アイテム**または**バックアップ管理サーバー**に 0 が表示されていない場合、それらのアイテムを削除する必要があります。 コンテナーにデータが含まれている場合は、そのコンテナーを削除できません。

    ![Look at Essentials pane for protected items](./media/backup-azure-delete-vault/contoso-bkpvault-settings.png)

    VM およびファイル/フォルダーはバックアップ アイテムと見なされ、[要点] ウィンドウの **[バックアップ アイテム]** 領域の一覧に表示されます。 DPM サーバーは、[要点] ウィンドウの **[バックアップ管理サーバー]** 領域の一覧に表示されます。 **[レプリケートされたアイテム]** は、Azure Site Recovery サービスに関連します。
3. コンテナーから保護されているアイテムを削除するには、まず、コンテナー内のアイテムを探します。 コンテナー ダッシュボードで **[設定]**、**[バックアップ アイテム]** の順にクリックして、次のメニューを開きます。

    ![choose vault from list](./media/backup-azure-delete-vault/open-settings-and-backup-items.png)

    **[バックアップ アイテム]** メニューには、アイテムの種類 (Azure Virtual Machines またはファイル フォルダー) に基づいて、個別の一覧があります (図を参照)。 一覧に表示される既定のアイテムの種類は、Azure Virtual Machines です。 コンテナー内のファイル フォルダー アイテムの一覧を表示するには、ドロップダウン メニューで **[ファイル フォルダー]** を選択します。
4. VM を保護しているコンテナーからアイテムを削除する前に、アイテムのバックアップ ジョブを停止し、回復ポイント データを削除する必要があります。 コンテナー内の各アイテムに対して、次の手順を行います。

    a.[サインオン URL] ボックスに、次のパターンを使用して、ユーザーが Pluralsight アプリケーションへのサインオンに使用する次の URL を入力します。 **[バックアップ アイテム]** メニューでアイテムを右クリックし、コンテキスト メニューで **[バックアップの停止]** を選択します。

    ![stop the backup job](./media/backup-azure-delete-vault/stop-the-backup-process.png)

    [バックアップの停止] メニューが開きます。

    b. **[バックアップの停止]** メニューの **[オプションの選択]** メニューで **[バックアップ データの削除]** を選択し、アイテムの名前を入力して、**[バックアップの停止]** をクリックします。

    削除することを確認するために、アイテムの名前を入力します。 アイテムを確認したら、**[バックアップの停止]** ボタンがアクティブになります。 **[バックアップ データの保持]** を選択した場合、バックアップ アイテムの名前を入力するダイアログ ボックスは表示されません。

    ![[バックアップ データの削除]](./media/backup-azure-delete-vault/stop-backup-blade-delete-backup-data.png)

    必要に応じて、データを削除する理由を指定し、コメントを追加できます。 **[バックアップの停止]**をクリックした後、削除ジョブが完了するまで待機してから、コンテナーを削除します。 ジョブの完了を確認するには、Azure メッセージ ![バックアップ データの削除](./media/backup-azure-delete-vault/messages.png) <br/>
    ジョブが完了すると、バックアップ プロセスが停止されたことと、バックアップ データが削除されたことを示すメッセージがサービスから送信されます。

    c. 一覧のアイテムを削除した後、**[バックアップ アイテム]** メニューの **[更新]** をクリックして、コンテナー内の残りのアイテムを確認します。

      ![[バックアップ データの削除]](./media/backup-azure-delete-vault/empty-items-list.png)

      一覧にアイテムがなくなったら、[Recovery Services コンテナー] メニューの **[要点]** ウィンドウまでスクロールします。 一覧には、**[バックアップ アイテム]**、**[バックアップ管理サーバー]**、**[レプリケートされたアイテム]** のどれも表示されないはずです。 コンテナーに引き続きアイテムが表示される場合は、手順 3. に戻り、別のアイテムの種類の一覧を選択します。  
5. コンテナー ツール バーにアイテムがなくなったら、 **[削除]**をクリックします。

    ![[バックアップ データの削除]](./media/backup-azure-delete-vault/delete-vault.png)
6. コンテナーを削除することを確認するために、**[はい]** をクリックします。

    コンテナーが削除され、ポータルが **[新規]** サービス メニューに戻ります。

## <a name="what-if-i-stopped-the-backup-process-but-retained-the-data"></a>バックアップ プロセスを停止してもデータが保持されている場合の対処
バックアップ プロセスを停止したものの、誤ってデータが " *保持* " されてしまった場合は、コンテナーを削除する前にバックアップ データを削除する必要があります。 バックアップ データを削除するには:

1. **[バックアップ アイテム]** メニューでアイテムを右クリックし、コンテキスト メニューで **[バックアップ データの削除]** をクリックします。

    ![[バックアップ データの削除]](./media/backup-azure-delete-vault/delete-backup-data-menu.png)

    **[バックアップ データを削除]** メニューが開きます。
2. **[バックアップ データの削除]** メニューでアイテムの名前を入力し、**[削除]** をクリックします。

    ![[バックアップ データの削除]](./media/backup-azure-delete-vault/delete-retained-vault.png)

    データを削除したら、手順 4. の c. に戻り、プロセスを続行します。

## <a name="delete-a-vault-used-to-protect-a-dpm-server"></a>DPM サーバーの保護に使用されているコンテナーの削除
DPM サーバーの保護に使用されているコンテナーを削除する前に、作成したすべての回復ポイントを消去し、コンテナーへのサーバーの登録を解除する必要があります。

保護グループに関連付けられているデータを削除するには:

1. DPM 管理者コンソールで **[保護]** をクリックし、保護グループ、保護グループ メンバーの順に選択して、ツール リボンの **[削除]** をクリックします。

  保護グループ メンバーを選択すると、ツール リボンの **[削除]** ボタンがアクティブになります。 例では、メンバーは **dummyvm9**です。 保護グループの複数のメンバーを選択するには、Ctrl キーを押しながら各メンバーをクリックします。

    ![[バックアップ データの削除]](./media/backup-azure-delete-vault/az-portal-delete-protection-group.png)

    **[保護の停止]** ダイアログ ボックスが開かれます。
2. **[保護の停止]** ダイアログで **[保護されるデータを削除する]** を選択し、**[保護の停止]** をクリックします。

    ![[バックアップ データの削除]](./media/backup-azure-delete-vault/delete-dpm-protection-group.png)

    コンテナーを削除するには、保護されたデータのコンテナーを消去 (削除) する必要があります。 復旧ポイントが多数存在し、保護グループ内にデータがある場合は、データを削除するまでに数分かかる場合があります。 **[保護の停止]** ダイアログは、ジョブが完了すると表示されます。

    ![[バックアップ データの削除]](./media/backup-azure-delete-vault/success-deleting-protection-group.png)
3. すべての保護グループのすべてのメンバーに対して、この操作を繰り返します。

    保護されているすべてのデータと保護グループを削除します。
4. 保護グループからすべてのメンバーを削除した後、Azure Portal に切り替えます。 コンテナー ダッシュボードを開き、**バックアップ アイテム**、**バックアップ管理サーバー**、および**レプリケートされたアイテム**がないことを確認します。 コンテナー ツール バーで、 **[削除]**をクリックします。

    ![[バックアップ データの削除]](./media/backup-azure-delete-vault/delete-vault.png)

    コンテナーに登録されているバックアップ管理サーバーがある場合、コンテナーにデータがなくても、コンテナーを削除することはできません。 コンテナーに関連付けられているバックアップ管理サーバーを既に削除しているにもかかわらず、**[要点]** ウィンドウにサーバーが表示されている場合は、「[コンテナーに登録されているバックアップ管理サーバーを探す](backup-azure-delete-vault.md#find-the-backup-management-servers-registered-to-the-vault)」をご覧ください。
5. コンテナーを削除することを確認するために、**[はい]** をクリックします。

    コンテナーが削除され、ポータルが **[新規]** サービス メニューに戻ります。

## <a name="delete-a-vault-used-to-protect-a-production-server"></a>実稼働サーバーの保護に使用されているコンテナーの削除
サーバーの保護に使用されているコンテナーを削除する前に、コンテナーからサーバーを削除するか、登録を解除する必要があります。

コンテナーに関連付けられている実稼働サーバーを削除するには:

1. Azure Portal でコンテナー ダッシュボードを開き、**[設定]**、 > **[バックアップ インフラストラクチャ]**、 > **[実稼働サーバー]** の順にクリックします。

    ![[実稼働サーバー] メニューを開く](./media/backup-azure-delete-vault/delete-production-server.png)

    **[実稼働サーバー]** メニューが開き、コンテナー内のすべての実稼働サーバーが一覧表示されます。

    ![list of Production Servers](./media/backup-azure-delete-vault/list-of-production-servers.png)
2. **[実稼働サーバー]** メニューでサーバーを右クリックし、**[削除]** をクリックします。

    ![delete production server ](./media/backup-azure-delete-vault/delete-server-on-production-server-blade.png)

    **[削除]** メニューが開きます。

    ![delete production server ](./media/backup-azure-delete-vault/delete-blade.png)
3. **[削除]** メニューで、サーバー名を確認し、**[削除]** をクリックします。 **[削除]** ボタンをアクティブにするには、サーバーの名前を正確に入力する必要があります。

    コンテナーが削除されると、コンテナーが削除されたことを示すメッセージが表示されます。 コンテナー内のすべてのサーバーを削除した後、コンテナー ダッシュボードで [要点] ウィンドウに戻るまでスクロールします。
4. コンテナー ダッシュボードで、**バックアップ アイテム**、**バックアップ管理サーバー**、および**レプリケートされたアイテム**がないことを確認します。 コンテナー ツール バーで、 **[削除]**をクリックします。
5. コンテナーを削除することを確認するために、**[はい]** をクリックします。

    コンテナーが削除され、ポータルが **[新規]** サービス メニューに戻ります。

## <a name="find-the-backup-management-servers-registered-to-the-vault"></a>コンテナーに登録されているバックアップ管理サーバーを探す
コンテナーに複数のサーバーが登録されている場合、それらを覚えておくことは難しいことがあります。 コンテナーに登録されているサーバーを確認し、それらを削除するには:

1. コンテナー ダッシュボードを開きます。
2. **[要点]** ウィンドウで **[設定]** をクリックし、メニューを開きます。

    ![[設定メニュー] を開く](./media/backup-azure-delete-vault/backup-vault-click-settings.png)
3. **[設定]** メニューで **[バックアップ インフラストラクチャ]** をクリックします。
4. **[バックアップ インフラストラクチャ]** メニューで **[バックアップ管理サーバー]** をクリックします。 [バックアップ管理サーバー] メニューが開かれます。

    ![list of backup management servers](./media/backup-azure-delete-vault/list-of-backup-management-servers.png)
5. 一覧からサーバーを削除するには、サーバーの名前を右クリックし、 **[削除]**をクリックします。
    **[削除]** メニューが開きます。
6. **[削除]** メニューで、サーバーの名前を指定します。 長い名前である場合は、[バックアップ管理サーバー] の一覧からコピーして貼り付けることができます。 その後、 **[削除]**をクリックします。  
