---
title: 動的グループの作成と状態チェックを行う - Azure Active Directory | Microsoft Docs
description: Azure Portal でグループ メンバーシップ ルールの作成と状態チェックを行う方法。
services: active-directory
documentationcenter: ''
author: curtand
manager: mtillman
ms.service: active-directory
ms.workload: identity
ms.subservice: users-groups-roles
ms.topic: article
ms.date: 01/31/2019
ms.author: curtand
ms.reviewer: krbain
ms.custom: it-pro
ms.collection: M365-identity-device-management
ms.openlocfilehash: 5651d5e37613abcef8c8f5448af38637f91ebe30
ms.sourcegitcommit: 301128ea7d883d432720c64238b0d28ebe9aed59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/13/2019
ms.locfileid: "56193630"
---
# <a name="create-a-dynamic-group-and-check-status"></a>動的グループの作成と状態チェックを行う

Azure Active Directory (Azure AD) では、ユーザーまたはデバイスのプロパティに基づいてメンバーシップを決定するルールを適用することで、グループを作成できます。 ユーザーまたはデバイスの属性が変更された場合、Azure AD は、Azure AD テナント内のすべての動的グループ ルールを評価し、それに基づいて追加または削除を実行します。 ユーザーまたはデバイスがグループ用のルールを満たしている場合はメンバーとして追加され、ルールを満たさなくなった場合は削除されます。

この記事では、セキュリティ グループまたは Office 365 グループに関する動的メンバーシップ用のルールを Azure Portal で設定する方法を説明します。 ルールの構文の例、メンバーシップ ルールでサポートされているプロパティ、演算子、および値の完全な一覧については、[Azure Active Directory でのグループに対する動的メンバーシップ ルール](groups-dynamic-membership.md)に関する記事を参照してください。

## <a name="to-create-a-group-membership-rule"></a>グループ メンバーシップ ルールを作成するには

1. 全体管理者、Intune サービス管理者、またはテナントでユーザー アカウント管理者ロールであるアカウントを使用して、[Azure AD 管理センター](https://aad.portal.azure.com)にサインインします。
2. **[グループ]** を選びます。
3. **[すべてグループ]** を選び、**[新しいグループ]** を選びます。

   ![新しいグループを追加する](./media/groups-create-rule/new-group-creation.png)

4. **[グループ]** ブレードで、新しいグループの名前と説明を入力します。 **[メンバーシップの種類]** で、ユーザーとデバイスのどちらのルールを作成するかに応じて、**[動的ユーザー]** または **[動的デバイス]** を選択し、**[動的クエリの追加]** をクリックします。 ルール ビルダーを使って簡単なルールを作成するか、メンバーシップ ルールを自分で記述できます。 この記事には、使用できるユーザーとデバイスの属性の詳細と、メンバーシップ ルールの例が含まれます。

   ![動的メンバーシップのルールを追加する](./media/groups-create-rule/add-dynamic-group-rule.png)

5. メンバーシップ クエリに追加できるカスタム拡張機能プロパティの完全な一覧を参照するには、**[Get custom extension properties]** \(カスタム拡張機能プロパティの取得\) を選択し、アプリケーション ID を入力して、**[プロパティの更新]** を選択します。 すべてのプロパティの一覧から選択できるようになります。
6. ルールを作成した後、ブレードの下部にある **[クエリの追加]** を選びます。
7. **[作成]** on the **[グループ]** をクリックして、グループを作成します。

> [!TIP]
> 入力したルールが間違った形式または無効な場合、グループの作成は失敗します。 ポータルの右上隅に通知が表示されます。そこにはルールが処理できなかった理由の説明が書かれています。 これをよく読み、ルールを有効にするためにどのような調整が必要なのかを把握しましょう。

## <a name="check-processing-status-for-a-membership-rule"></a>メンバーシップ ルールの処理状態をチェックする

グループの **[概要]** ページで、メンバーシップの処理状態と最終更新日を確認できます。
  
  ![動的グループの状態の表示](./media/groups-create-rule/group-status.png)

**[メンバーシップの処理]** の状態には、次の状態メッセージが表示される場合があります。

* **評価中**:グループの変更が受信され、更新プログラムが評価されています。
* **処理中**:更新プログラムが処理されています。
* **更新の完了**:処理が完了し、該当するすべての更新が行われました。
* **処理エラー**:メンバーシップ規則の評価中にエラーが発生し、処理を完了できませんでした。
* **更新の一時停止**:動的メンバーシップ規則の更新プログラムが管理者によって一時停止されました。 MembershipRuleProcessingState は、"一時停止" に設定されます。

**[メンバーシップの最終更新日時]** の状態には、次の状態メッセージが表示される場合があります。

* &lt;**日付と時刻**&gt;:メンバーシップが最後に更新された日時。
* **進行中**: 更新は現在進行中です。
* **不明**:最終更新時刻を取得することができません。 新しく作成されるグループが原因の可能性があります。

特定のグループのメンバーシップ規則の処理中にエラーが発生すると、そのグループの **[概要]** ページの上部にアラートが表示されます。 24 時間以上、テナント内のすべてのグループに対して保留中の動的メンバーシップの更新が処理できない場合は、**[すべてグループ]** の上部にアラートが表示されます。

![処理エラー メッセージ](./media/groups-create-rule/processing-error.png)

次の記事は、Azure Active Directory のグループに関する追加情報を提供します。

* [既存のグループの表示](../fundamentals/active-directory-groups-view-azure-portal.md)
* [新しいグループの作成とメンバーの追加](../fundamentals/active-directory-groups-create-azure-portal.md)
* [グループの設定の管理](../fundamentals/active-directory-groups-settings-azure-portal.md)
* [グループのメンバーシップの管理](../fundamentals/active-directory-groups-membership-azure-portal.md)
* [グループ内のユーザーの動的ルールの管理](groups-dynamic-membership.md)
