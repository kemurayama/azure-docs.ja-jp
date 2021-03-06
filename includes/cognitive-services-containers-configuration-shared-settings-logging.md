---
author: diberry
ms.author: diberry
ms.service: cognitive-services
ms.topic: include
ms.date: 01/02/2019
ms.openlocfilehash: dc527a4e1bdf9648ddfc9f582b0c146197214f26
ms.sourcegitcommit: 90c6b63552f6b7f8efac7f5c375e77526841a678
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2019
ms.locfileid: "56741470"
---
`Logging` の設定では、お客様のコンテナーの ASP.NET Core ログ サポートを管理します。 お客様が ASP.NET Core アプリケーションに対して使用するのと同じ構成設定と値をお客様のコンテナーに使用できます。 

コンテナーでは、次のログ プロバイダーがサポートされています。

|プロバイダー|目的|
|--|--|
|[Console](https://docs.microsoft.com/aspnet/core/fundamentals/logging/?view=aspnetcore-2.1#console-provider)|ASP.NET Core `Console` ログ プロバイダー。 このログ プロバイダーのすべての ASP.NET Core 構成設定と既定値がサポートされています。|
|[デバッグ](https://docs.microsoft.com/aspnet/core/fundamentals/logging/?view=aspnetcore-2.1#debug-provider)|ASP.NET Core `Debug` ログ プロバイダー。 このログ プロバイダーのすべての ASP.NET Core 構成設定と既定値がサポートされています。|
|[ディスク](#disk-logging)|JSON ログ プロバイダー。 このログ プロバイダーは、ログ データを出力マウントに書き込みます。|

### <a name="disk-logging"></a>Disk ログ

`Disk` ログ プロバイダーでは、次の構成設定がサポートされます。  

| Name | データ型 | 説明 |
|------|-----------|-------------|
| `Format` | String | ログ ファイルの出力形式。<br/> **注:** ログ プロバイダーを有効にするためにこの値を `json` に設定する必要があります。 コンテナーのインスタンス化中に、出力マウントを指定せずに、この値を指定した場合、エラーが発生します。 |
| `MaxFileSize` | 整数 | ログ ファイルの最大サイズ (メガバイト (MB))。 現在のログ ファイルのサイズがこの値を満たしているか、または超えている場合、ログ プロバイダーによって新しいログ ファイルが開始されます。 -1 が指定されている場合、ログ ファイルのサイズは、出力マウントの最大ファイル サイズ (存在する場合) によってのみ制限されます。 既定値は 1 です。 |

ASP.NET Core ログのサポートを構成する方法の詳細については、[設定ファイル構成](https://docs.microsoft.com/aspnet/core/fundamentals/logging/?view=aspnetcore-2.1)に関するページを参照してください。
