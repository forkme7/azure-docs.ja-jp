Azure Virtual Machines は、複数のデータ ディスクの接続をサポートしています。 この記事では、VM のデータ ディスクのスケーラビリティとパフォーマンスのターゲットについて説明します。 これらのターゲットは、パフォーマンスと容量の要件を満たすために必要なディスクの数と種類を決めるときに役立ちます。 

> [!IMPORTANT]
> パフォーマンスを最適化するには、仮想マシンに接続する使用率が高いディスク数を制限して、スロットルを回避するようにします。 すべてのアタッチされているディスクの使用率が同時に高くならなければ、仮想マシンは多数のディスクに対応できます。

* **Azure Managed Disks の場合:** 管理ディスクには、リージョンあたりとディスクの種類あたりのディスク制限があります。 サブスクリプションのリージョンあたりとディスクの種類あたりで 10,000 個という管理ディスクの上限は既定の制限でもあります。 たとえば、1 つのリージョン内でサブスクリプションあたりで、10,000 個までの Standard 管理ディスクと 10,000 個までの Premium 管理ディスクを作成できます。

    管理スナップショットおよびイメージは、管理ディスクの制限に対してカウントされます。

* **Standard ストレージ アカウントの場合:** Standard ストレージ アカウントには、20,000 IOPS という最大合計要求レートがあります。 Standard ストレージ アカウントの仮想マシン ディスク全体の合計 IOPS は、この制限を超えることはできません。
  
    1 つの Standard ストレージ アカウントでサポートされる使用率が高いディスク数は、要求レート制限に基づいて概算できます。 たとえば、Basic レベルの VM では、使用率の高いディスクの最大数は約 66 (ディスクあたり 20,000/300 IOPS) であり、Standard レベルの VM では約 40 (ディスクあたり IOPS 20,000/500) です。 

* **Premium Storage アカウントの場合:** Premium Storage アカウントの最大合計スループット レートは 50 Gbps です。 すべての VM ディスク全体の合計スループットは、この制限を超えることはできません。

