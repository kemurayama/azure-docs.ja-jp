---
title: Azure Stream Analytics ジョブの削除
description: この記事では、Azure Stream Analytics ジョブを削除するさまざまな方法を示します。
services: stream-analytics
author: mamccrea
ms.author: mamccrea
ms.reviewer: jasonh
ms.service: stream-analytics
ms.topic: conceptual
ms.date: 12/06/2018
ms.custom: seodec18
ms.openlocfilehash: 85db38fef5e69c4de855f8cb6d54151496faebbe
ms.sourcegitcommit: 9fb6f44dbdaf9002ac4f411781bf1bd25c191e26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2018
ms.locfileid: "53090246"
---
# <a name="clean-up-your-azure-stream-analytics-job"></a>Azure Stream Analytics ジョブの削除

Azure Stream Analytics ジョブは、Azure Portal、Azure PowerShell、Azure SDK for .Net または REST API を使用して簡単に削除できます。

>[!NOTE] 
>Azure Stream Analytics ジョブを停止すると、Event Hubs または Azure SQL Database などの入力および出力ストレージのみでデータが永続化されます。 Azure からデータを削除する必要がある場合は、Stream Analytics ジョブの入力と出力のリソースの削除処理を実行してください。

## <a name="stop-a-job-in-azure-portal"></a>Azure Portal でジョブを停止する

1. [Azure Portal](https://portal.azure.com) にサインインします。 

2. 実行されている Stream Analytics ジョブを探し､選択します｡

3. Stream Analytics ジョブのページで **[停止]** をクリックします。 

   ![Azure Stream Analytics ジョブを停止する](./media/stream-analytics-clean-up-your-job/stop-stream-analytics-job.png)


## <a name="delete-a-job-in-azure-portal"></a>Azure Portal でジョブを削除する

1. Azure ポータルにサインインします。 

2. Stream Analytics ジョブがある場所を探し､ジョブを選択します｡

3. Stream Analytics ジョブのページで **[削除]** を選択してジョブを削除します。 

   ![Azure Stream Analytics ジョブを削除する](./media/stream-analytics-clean-up-your-job/delete-stream-analytics-job.png)


## <a name="stop-or-delete-a-job-using-powershell"></a>PowerShell を使用してジョブを停止または削除する

PowerShell を使用してジョブを停止するには、[Stop-AzureRmStreamAnalyticsJob](https://docs.microsoft.com/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob?view=azurermps-5.7.0) コマンドレットを使用します。 PowerShell を使用してジョブを削除するには、[Remove-AzureRmStreamAnalyticsJob](https://docs.microsoft.com/powershell/module/azurerm.streamanalytics/Remove-AzureRmStreamAnalyticsJob?view=azurermps-5.7.0) コマンドレットを使用します。

## <a name="stop-or-delete-a-job-using-azure-sdk-for-net"></a>Azure SDK for .NET を使用してジョブを停止または削除する

Azure SDK for .NET を使用してジョブを停止するには、[StreamingJobsOperationsExtensions.BeginStop](https://docs.microsoft.com/dotnet/api/microsoft.azure.management.streamanalytics.streamingjobsoperationsextensions.beginstop?view=azure-dotnet) メソッドを使用します。 Azure SDK for .NET を使用してジョブを削除するには、[StreamingJobsOperationsExtensions.BeginDelete](https://docs.microsoft.com/dotnet/api/microsoft.azure.management.streamanalytics.streamingjobsoperationsextensions.begindelete?view=azure-dotnet) メソッドを使用します。

## <a name="stop-or-delete-a-job-using-rest-api"></a>REST API を使用してジョブを停止または削除する

REST API を使用してジョブを停止するには、[Stop](https://docs.microsoft.com/rest/api/streamanalytics/stream-analytics-job#stop) メソッドを参照してください。 REST API を使用してジョブを削除するには、[Delete](https://docs.microsoft.com/rest/api/streamanalytics/stream-analytics-job#delete) メソッドを参照してください。
