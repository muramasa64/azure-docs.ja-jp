---
title: Azure Application Insights Telemetry のデータ モデル - イベント テレメトリ | Microsoft Docs
description: イベント テレメトリ用の Application Insights データ モデル
ms.topic: conceptual
ms.date: 04/25/2017
ms.reviewer: sergkanz
ms.openlocfilehash: bd8b2581f7642f6825aaf0d1b51c8e94d4333d33
ms.sourcegitcommit: 747a20b40b12755faa0a69f0c373bd79349f39e3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/27/2020
ms.locfileid: "77671883"
---
# <a name="event-telemetry-application-insights-data-model"></a>イベント テレメトリ:Application Insights データ モデル

アプリケーションで発生したイベントを表すイベント テレメトリ項目を作成できます ([Application Insights](../../azure-monitor/app/app-insights-overview.md))。 通常は、ボタンのクリックや注文のチェックアウトなどのユーザーの操作です。 初期化や構成の更新などのアプリケーション ライフ サイクル イベントの場合もあります。 

意味的には、イベントは、要求に相関付けられる場合と、関連付けられない場合があります。 ただし、適切に使用すれば、イベント テレメトリは、要求やトレースよりも重要になります。 イベントはビジネス テレメトリを表しているため、独立したより緩やかな[サンプリング](../../azure-monitor/app/api-filtering-sampling.md)の対象にする必要があります。

## <a name="name"></a>名前

イベント名。 適切なグループ分けや有効なメトリックのために、多数の個別イベント名が生成されないようにアプリケーションを制限してください。 たとえば、1 つのイベントで生成されるインスタンスごとに別の名前を使用しないでください。

最大長:512 文字

## <a name="custom-properties"></a>カスタム プロパティ

[!INCLUDE [application-insights-data-model-properties](../../../includes/application-insights-data-model-properties.md)]

## <a name="custom-measurements"></a>カスタム測定値

[!INCLUDE [application-insights-data-model-measurements](../../../includes/application-insights-data-model-measurements.md)]

## <a name="next-steps"></a>次のステップ

- Application Insights の型とデータ モデルについては、[データ モデル](data-model.md)に関するページを参照してください。
- [カスタム イベント テレメトリを記述します](../../azure-monitor/app/api-custom-events-metrics.md#trackevent)。
- Application Insights でサポートされている[プラットフォーム](../../azure-monitor/app/platforms.md)を確認します。
