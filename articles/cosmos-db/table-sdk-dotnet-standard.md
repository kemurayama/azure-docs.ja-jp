---
title: Azure Cosmos DB Table API .NET Standard SDK およびリソース
description: リリース日、提供終了日、各バージョン間の変更点など、Azure Cosmos DB Table API および .NET Standard SDK に関するあらゆる詳細を提供します。
author: wmengmsft
ms.author: wmeng
ms.service: cosmos-db
ms.subservice: cosmosdb-table
ms.devlang: dotnet
ms.topic: reference
ms.date: 10/18/2018
ms.openlocfilehash: ce7cc489b107ce4bd95270b9a7f8cb560a2d2398
ms.sourcegitcommit: 898b2936e3d6d3a8366cfcccc0fccfdb0fc781b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "55249648"
---
# <a name="azure-cosmos-db-table-net-standard-api-download-and-release-notes"></a>Azure Cosmos DB Table .NET Standard API: ダウンロードおよびリリース ノート
> [!div class="op_single_selector"]

> * [.NET](table-sdk-dotnet.md)
> * [.NET Standard](table-sdk-dotnet-standard.md)
> * [Java](table-sdk-java.md)
> * [Node.js](table-sdk-nodejs.md)
> * [Python](table-sdk-python.md)

|   |   |
|---|---|
|**SDK のダウンロード**|[NuGet](https://www.nuget.org/packages/Microsoft.Azure.Cosmos.Table)|
|**現在サポートされているフレームワーク**|[Microsoft .NET Standard 2.0](https://www.nuget.org/packages/NETStandard.Library)|

## <a name="release-notes"></a>リリース ノート

### <a name="a-name0101-preview0101-preview"></a><a name="0.10.1-preview"/>0.10.1-preview
* Azure Storage Table エンドポイントに対する SAS トークン、TablePermissions、ServiceProperties、および ServiceStats の操作が追加されています。 
   > [!NOTE]
   > 以前の Azure Storage Table SDK の一部の機能はまだサポートされていません (クライアント側の暗号化など)。

### <a name="a-name0100-preview0100-preview"></a><a name="0.10.0-preview"/>0.10.0-preview
* Azure Storage Table エンドポイントに対するコア CRUD、バッチ、およびクエリ操作のサポートが追加されています。 
   > [!NOTE]
   > 以前の Azure Storage Table SDK の一部の機能はまだサポートされていません (クライアント側の暗号化など)。

### <a name="a-name091-preview091-preview"></a><a name="0.9.1-preview"/>0.9.1-preview
* Azure Cosmos DB Table .NET Standard SDK は、Cosmos DB 上の Table データ モデルに効率的にアクセスするためのクロスプラットフォーム対応 .NET ライブラリです。 この最初のリリースでは、テーブルおよびエンティティの CRUD とクエリの機能全体、および [Cosmos DB Table SDK For .NET Framework](table-sdk-dotnet.md) に類似する API がサポートされています。 
   > [!NOTE]
   >  Azure Storage Table のエンドポイントは、0.9.1-preview バージョンではまだサポートされていません。

## <a name="release-and-retirement-dates"></a>リリース日と提供終了日
Microsoft は、新しい/サポートされるバージョンに速やかに移行する目的で、SDK の提供終了を少なくともその **12 か月**前に通知します。

| Version | リリース日 | 提供終了日 |
| --- | --- | --- |
| [0.10.1-preview](#0.10.1-preview) |2019 年 1 月 22 日 |--- |
| [0.10.0-preview](#0.10.0-preview) |2018 年 12 月 18 日 |--- |
| [0.9.1-preview](#0.9.1-preview) |2018 年 10 月 18 日 |--- |


## <a name="faq"></a>FAQ

[!INCLUDE [cosmos-db-sdk-faq](../../includes/cosmos-db-sdk-faq.md)]

## <a name="see-also"></a>関連項目
Azure Cosmos DB Table API の詳細については、「[Introduction to Azure Cosmos DB Table API (Azure Cosmos DB Table API の概要)](table-introduction.md)」を参照してください。 
