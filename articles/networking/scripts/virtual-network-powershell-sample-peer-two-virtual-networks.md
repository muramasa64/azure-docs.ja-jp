---
title: Azure PowerShell スクリプト サンプル - 2 つの仮想ネットワークのピアリング | Microsoft Docs
description: Azure PowerShell スクリプト サンプル - 2 つの仮想ネットワークのピアリング
services: virtual-network
documentationcenter: virtual-network
author: KumudD
manager: mtillman
ms.service: virtual-network
ms.devlang: powershell
ms.topic: article
ms.tgt_pltfrm: ''
ms.workload: infrastructure
ms.date: 05/16/2017
ms.author: kumud
ms.openlocfilehash: 53af283813500fc93d3e5fb9d4b00a9c3034af2d
ms.sourcegitcommit: cf36df8406d94c7b7b78a3aabc8c0b163226e1bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2019
ms.locfileid: "73890183"
---
# <a name="peer-two-virtual-networks"></a>2 つの仮想ネットワークのピアリング

このスクリプトでは、Azure ネットワークを使用して同じリージョンに 2 つの仮想ネットワークを作成して接続します。 スクリプトを実行した後で、2 つの仮想ネットワーク間のピアリングを作成します。

必要に応じて、[Azure PowerShell ガイド](https://docs.microsoft.com/powershell/azureps-cmdlets-docs/)の手順に従って Azure PowerShell をインストールし、`Connect-AzAccount` を実行して、Azure との接続を作成します。

[!INCLUDE [quickstarts-free-trial-note](../../../includes/quickstarts-free-trial-note.md)]

## <a name="sample-script"></a>サンプル スクリプト

[!INCLUDE [updated-for-az](../../../includes/updated-for-az.md)]

[!code-azurepowershell[main](../../../powershell_scripts/virtual-network/peer-two-virtual-networks/peer-two-virtual-networks.ps1 "Peer two networks")]

## <a name="clean-up-deployment"></a>デプロイのクリーンアップ 

次のコマンドを実行して、リソース グループ、VM、すべての関連リソースを削除します。

```powershell
Remove-AzResourceGroup -Name myResourceGroup
```

## <a name="script-explanation"></a>スクリプトの説明

このスクリプトでは、次のコマンドを使用して、リソース グループ、仮想マシン、およびすべての関連リソースを作成します。 表内の各コマンドは、それぞれのドキュメントにリンクされています。

| command | メモ |
|---|---|
| [New-AzResourceGroup](/powershell/module/az.resources/new-azresourcegroup) | すべてのリソースを格納するリソース グループを作成します。 | 
| [New-AzVirtualNetwork](/powershell/module/az.network/new-azvirtualnetwork)| Azure 仮想ネットワークとサブネットを作成します。 |
| [Add-AzVirtualNetworkPeering](/powershell/module/az.network/add-azvirtualnetworkpeering) | 2 つの仮想ネットワーク間のピアリングを作成します。  |
| [Remove-AzResourceGroup](/powershell/module/az.resources/remove-azresourcegroup) | 入れ子になったリソースすべてを含むリソース グループを削除します。 |

## <a name="next-steps"></a>次の手順

Azure PowerShell の詳細については、[Azure PowerShell のドキュメント](https://docs.microsoft.com/powershell/azure/overview)を参照してください。

その他のネットワーク PowerShell のサンプル スクリプトは、[Azure ネットワークの概要ドキュメント](../powershell-samples.md?toc=%2fazure%2fnetworking%2ftoc.json)で確認できます。
