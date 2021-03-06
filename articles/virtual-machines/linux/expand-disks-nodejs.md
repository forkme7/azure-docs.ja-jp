---
title: Azure CLI 1.0 を使用して Linux VM の OS ディスクを拡張する | Microsoft Docs
description: Azure CLI 1.0 と Resource Manager デプロイメント モデルを使用して、Linux VM のオペレーティング システム (OS) 仮想ディスクを拡張する方法について説明します
services: virtual-machines-linux
documentationcenter: ''
author: iainfoulds
manager: jeconnoc
editor: ''
ms.assetid: ''
ms.service: virtual-machines-linux
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: vm-linux
ms.workload: infrastructure
ms.date: 05/11/2017
ms.author: iainfou
ms.openlocfilehash: f81054727bb1f0e8ffa752783e866a72d573589d
ms.sourcegitcommit: 5b2ac9e6d8539c11ab0891b686b8afa12441a8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2018
---
# <a name="expand-os-disk-on-a-linux-vm-using-the-azure-cli-with-the-azure-cli-10"></a>Azure CLI と Azure CLI 1.0 を使用して Linux VM の OS ディスクを拡張する
Azure の Linux 仮想マシン (VM) では、通常、オペレーティング システム (OS) の既定の仮想ハード ディスク サイズは 30 GB です。 [データ ディスクを追加](add-disk.md)して追加の記憶域を提供できますが、OS ディスクを拡張することもできます。 この記事では、Azure CLI 1.0 で非管理対象ディスクを使用して Linux VM の OS ディスクを拡張する方法について詳しく説明します。

## <a name="cli-versions-to-complete-the-task"></a>タスクを完了するための CLI バージョン
次のいずれかの CLI バージョンを使用してタスクを完了できます。

- [Azure CLI 1.0](#prerequisites) - クラシック デプロイメント モデルと Resource Manager デプロイメント モデル用の CLI (本記事)
- [Azure CLI 2.0](expand-disks.md) - Resource Manager デプロイ モデル用の次世代 CLI

## <a name="prerequisites"></a>前提条件
[最新の Azure CLI 1.0](../../cli-install-nodejs.md) をインストールし、次のように Resource Manager モードを使用して [Azure アカウント](https://azure.microsoft.com/pricing/free-trial/)にログインする必要があります。

```azurecli
azure config mode arm
```

以下のサンプルでは、パラメーター名を独自の値に置き換えてください。 たとえば、*myResourceGroup* と *myVM* といったパラメーター名にします。

## <a name="expand-os-disk"></a>OS ディスクを拡張する

1. 仮想ハード ディスクに対する操作は、実行中の VM では実行できません。 次の例では、*myResourceGroup* という名前のリソース グループ内の *myVM* という VM を停止し、割り当てを解除します。

    ```azurecli
    azure vm deallocate --resource-group myResourceGroup --name myVM
    ```

    > [!NOTE]
    > `azure vm stop` では、コンピューティング リソースは解放されません。 コンピューティング リソースを解放するには、`azure vm deallocate` を使用します。 仮想ハード ディスクを拡張するには、VM の割り当てを解除する必要があります。

2. `azure vm set` コマンドを使用して、非管理対象 OS ディスクのサイズを更新します。 次の例では、*myResourceGroup* という名前のリソース グループ内の *myVM* という VM を *50* GB に更新しています。

    ```azurecli
    azure vm set \
        --resource-group myResourceGroup \
        --name myVM \
        --new-os-disk-size 50
    ```

3. 次のように VM を起動します。

    ```azurecli
    azure vm start --resource-group myResourceGroup --name myVM
    ```

4. 適切な資格情報を使用して VM に SSH 接続します。 OS ディスクのサイズが変更されたことを確認するには、`df -h` を使用します。 次の出力例は、プライマリ パーティション (*/dev/sda1*) が 50 GB になったことを示しています。

    ```bash
    Filesystem      Size  Used Avail Use% Mounted on
    udev            1.7G     0  1.7G   0% /dev
    tmpfs           344M  5.0M  340M   2% /run
    /dev/sda1        49G  1.3G   48G   3% /
    ```

## <a name="next-steps"></a>次の手順
追加の記憶域が必要な場合に、[Linux VM にデータ ディスクを追加](add-disk.md)します。 ディスク暗号化の詳細については、「[Azure CLI を使って Linux VM のディスクを暗号化する](encrypt-disks.md)」をご覧ください。
