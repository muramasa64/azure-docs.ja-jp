---
title: 状態構成で使用するための STIG に基づく構成 - Azure Automation
description: Azure Automation での状態構成用の STIG に基づく構成について説明します。
keywords: DSC, PowerShell, 構成, セットアップ
services: automation
ms.service: automation
ms.subservice: dsc
author: mgreenegit
ms.author: migreene
ms.date: 08/08/2019
ms.topic: conceptual
manager: carmonm
ms.openlocfilehash: 275b3bd25f931b73e8a378433899ef9ade4d47c1
ms.sourcegitcommit: dbcc4569fde1bebb9df0a3ab6d4d3ff7f806d486
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2020
ms.locfileid: "76028279"
---
# <a name="configuration-based-on-stig"></a>STIG に基づく構成

> 適用先:Windows PowerShell 5.1

構成コンテンツを初めて作成することは困難である可能性があります。
多くの場合、目標は、業界の推奨事項に沿っていることが望ましい "ベースライン" に従って、サーバーの構成を自動化することです。

> [!NOTE]
> この記事では、オープン ソース コミュニティによって管理されているソリューションについて説明します。
> サポートは、Microsoft からではなく、GitHub コラボレーションの形式でのみ利用できます。

## <a name="community-project-powerstig"></a>コミュニティ プロジェクト:PowerSTIG

[PowerSTIG](https://github.com/microsoft/powerstig) という名前のコミュニティ プロジェクトでは、STIG (セキュリティ技術実装ガイド) に関して提供された[公開情報](https://public.cyber.mil/stigs/)に基づく DSC コンテンツを生成することで、この問題を解決することを目標としています。

ベースラインの処理は、簡単そうに聞こえますが、なかなか大変です。
多くの組織では、ルールに対する[例外を文書化](https://github.com/microsoft/powerstig#powerstigdata)し、そのデータを大規模に管理する必要があります。
PowerSTIG では、設定の全範囲を 1 つの大きなファイルで処理するのではなく、構成の各領域に対応する[複合リソース](https://github.com/microsoft/powerstig#powerstigdsc)を提供することによって、この問題に取り組んでいます。

構成が生成されたら、それらを [DSC 構成スクリプト](/powershell/scripting/dsc/configurations/configurations)を使用して MOF ファイルを生成し、[その MOF ファイルを Azure Automation にアップロードする](/azure/automation/tutorial-configure-servers-desired-state#create-and-upload-a-configuration-to-azure-automation)ことができます。
次に、[オンプレミス](/azure/automation/automation-dsc-onboarding#physicalvirtual-windows-machines-on-premises-or-in-a-cloud-other-than-azure-including-aws-ec2-instances)または [Azure](/azure/automation/automation-dsc-onboarding#azure-virtual-machines) のいずれかからサーバーを登録して、構成をプルします。

PowerSTIG を試すには、[PowerShell ギャラリー](https://www.powershellgallery.com)にアクセスし、ソリューションをダウンロードするか、[Project Site]\(プロジェクト サイト\) をクリックして[ドキュメント](https://github.com/microsoft/powerstig)を参照してください。

## <a name="next-steps"></a>次のステップ

- [Windows PowerShell Desired State Configuration の概要](/powershell/scripting/dsc/overview/overview)
- [DSC リソース](/powershell/scripting/dsc/resources/resources)
- [ローカル構成マネージャーの構成](/powershell/scripting/dsc/managing-nodes/metaconfig)
