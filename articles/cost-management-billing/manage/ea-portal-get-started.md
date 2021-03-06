---
title: Azure エンタープライズ ポータルを使い始める
description: この記事では、Azure Enterprise Agreement (Azure EA) のお客様が Azure エンタープライズ ポータルを使用する方法について説明します。
author: bandersmsft
ms.author: banders
ms.date: 03/03/2020
ms.topic: conceptual
ms.service: cost-management-billing
ms.reviewer: boalcsva
ms.openlocfilehash: 5b84cbf4ae7065f13442852cfbf646aa49771e1f
ms.sourcegitcommit: d45fd299815ee29ce65fd68fd5e0ecf774546a47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2020
ms.locfileid: "78272425"
---
# <a name="get-started-with-the-azure-enterprise-portal"></a>Azure エンタープライズ ポータルを使い始める

この記事は、直接的および間接的な Azure Enterprise Agreement (Azure EA) のお客様が [Azure エンタープライズ ポータル](https://ea.azure.com)を使い始めるときに役立ちます。 次のことに関する基本的な情報を得られます。

- Azure エンタープライズ ポータルの構造。
- Azure エンタープライズ ポータルで使用されるロール。
- サブスクリプションの作成。
- Azure エンタープライズ ポータルと Azure portal でのコストの分析。

Azure エンタープライズ ポータルの完全なオンボード セッションについては、こちらのビデオをご覧ください。

> [!VIDEO https://www.youtube.com/embed/OiZ1GdBpo-I]

## <a name="azure-enterprise-portal-hierarchy"></a>Azure エンタープライズ ポータルの階層

Azure エンタープライズ ポータルの階層は、次のもので構成されます。

- **Azure エンタープライズ ポータル** - Azure EA サービスのコストを管理するときに役立つオンライン管理ポータルです。 次のようにすることができます。

  - 部署、アカウント、サブスクリプションを使用して Azure EA 階層を作成します。
  - 使用しているサービスのコストを調整し、使用状況レポートをダウンロードし、価格表を表示します。
  - 加入契約用の API キーを作成します。

- **部署**は、コストを論理的なグループに分割するのに役立ちます。 部署では、部署レベルで予算またはクォータを設定できます。

- **アカウント**は、Azure エンタープライズ ポータルでの組織単位です。 アカウントを使用して、サブスクリプションを管理し、レポートにアクセスできます。

- **サブスクリプション**は、Azure エンタープライズ ポータルの最小単位です。 これらは、サービス管理者によって管理される Azure サービスのコンテナーです。

次の図は、シンプルな Azure EA 階層を示しています。

![シンプルな Azure EA 階層の図](./media/ea-portal-get-started/ea-hierarchies.png)

## <a name="enterprise-user-roles"></a>エンタープライズ ユーザー ロール

次の管理ユーザー ロールは、エンタープライズ加入契約の一部です。

- エンタープライズ管理者
- 部門管理者
- アカウント所有者
- サービス管理者
- 通知の連絡先

ロールは、タスクを完了するために 2 つの異なるポータルで機能します。 課金とコストを管理するには [Azure エンタープライズ ポータル](https://ea.azure.com)を使用し、Azure サービスを管理するには [Azure portal](https://portal.azure.com) を使用します。

ユーザー ロールは、ユーザー アカウントに関連付けられています。 ユーザーの信頼性を確認するには、各ユーザーが有効な職場、学校、または Microsoft アカウントを持っている必要があります。 各アカウントが、アクティブに監視されている電子メール アドレスに関連付けられていることを確認します。 アカウント通知は、電子メール アドレスに送信されます。

ユーザーを設定するときに、複数のアカウントをエンタープライズ管理者ロールに割り当てることができます。 ただし、アカウント所有者ロールを持つことができるアカウントは 1 つだけです。 また、エンタープライズ管理者ロールとアカウント所有者ロールの両方を、1 つのアカウントに割り当てることができます。

### <a name="enterprise-administrator"></a>エンタープライズ管理者

このロールを持つユーザーは、最高レベルのアクセス権を持ちます。 次のことができます。

- アカウントとアカウント所有者を管理する。
- 他のエンタープライズ管理者を管理する。
- 部署管理者を管理する。
- 通知の連絡先を管理する。
- すべてのアカウントの使用状況を表示する。
- すべてのアカウントの未請求料金を表示する。

エンタープライズ加入契約に複数のエンタープライズ管理者を含めることができます。 エンタープライズ管理者に読み取り専用アクセス権を付与することができます。 これらはすべて部門管理者ロールを継承します。

### <a name="department-administrator"></a>部門管理者

このロールのユーザーは、次のことができます。

- 部署を作成して管理する。
- 新しいアカウント所有者を作成する。
- 管理している部署の使用状況の詳細を表示する。
- 必要なアクセス許可がある場合は、そのコストを表示する。

エンタープライズ加入契約ごとに複数の部門管理者を含めることができます。

新しい部署管理者を編集または作成するときに、部署管理者に読み取り専用アクセス権を付与することができます。 読み取り専用オプションを **[はい]** に設定します。

### <a name="account-owner"></a>アカウント所有者

このロールのユーザーは、次のことができます。

- サブスクリプションを作成して管理する。
- サービス管理者を管理する。
- サブスクリプションの使用状況を表示する。

各アカウントには、一意の職場、学校、または Microsoft アカウントが必要です。 Azure エンタープライズ ポータルの管理者ロールの詳細については、「[Azure の Azure Enterprise Agreement 管理者ロールを理解する](understand-ea-roles.md)」を参照してください。

### <a name="service-administrator"></a>サービス管理者

サービス管理者ロールには、Azure portal でサービスを管理し、ユーザーを共同管理者ロールに割り当てる権限があります。

### <a name="notification-contact"></a>通知の連絡先

通知の連絡先は、加入契約に関連する使用状況の通知を受け取ります。

## <a name="activate-your-enrollment"></a>加入契約をアクティブ化する

サービスをアクティブ化するには、最初のエンタープライズ管理者が [Azure エンタープライズ ポータル](https://ea.azure.com)を開き、招待メールのメール アドレスを使用してサインインします。

エンタープライズ管理者として設定されているユーザーは、アクティブ化メールを受け取る必要はありません。 [Azure エンタープライズ ポータル](https://ea.azure.com)にアクセスし、職場、学校、または Microsoft アカウントのメール アドレスとパスワードを使用してサインインします。

複数の加入契約がある場合は、アクティブ化するものを選択します。 既定では、アクティブな加入契約のみが表示されます。 加入契約の履歴を表示するには、Azure エンタープライズ ポータルの右上にある **[アクティブ]** オプションをオフにします。

**[加入契約]** では、状態が **[アクティブ]** と表示されます。

![アクティブな加入契約を示す例](./media/ea-portal-get-started/ea-enrollment-status.png)

他のエンタープライズ管理者を作成できるのは、既存の Azure エンタープライズ管理者だけです。

### <a name="create-another-enterprise-administrator"></a>別のエンタープライズ管理者を作成する

別のエンタープライズ管理者を追加するには:

1. [Azure エンタープライズ ポータル](https://ea.azure.com)にサインインします。
1. **[管理]**  >  **[加入契約の詳細]** に移動します。
1. 右上の **[+ 管理者の追加]** を選択します。

ユーザーのメール アドレスと、職場、学校、または Microsoft アカウントなどの優先認証方法が設定されていることを確認します。

自分がエンタープライズ管理者でない場合は、エンタープライズ管理者に連絡し、自分を加入契約に追加するように依頼します。 加入契約に追加された後、アクティブ化の電子メールを受け取ります。

エンタープライズ管理者が支援できない場合は、[Azure エンタープライズ ポータルのサポート リクエスト](https://support.microsoft.com/supportrequestform/cf791efa-485b-95a3-6fad-3daf9cd4027c)を作成します。 次の情報を指定します。

- 加入契約番号
- 追加するメール アドレスと認証の種類 (職場、学校、または Microsoft アカウント)
- 既存のエンタープライズ管理者からのメールの承認
  - 既存のエンタープライズ管理者を利用できない場合は、パートナーまたはソフトウェア アドバイザーに連絡して、ボリューム ライセンス サービス センター (VLSC) ツールで連絡先の詳細を変更するように依頼します。

エンタープライズ管理者ロールの詳細については、「[Azure の Azure Enterprise Agreement 管理者ロールを理解する](understand-ea-roles.md)」を参照してください。

## <a name="create-an-azure-enterprise-department"></a>Azure エンタープライズ部署を作成する

エンタープライズ管理者と部門管理者は部門を使用して、エンタープライズの Azure サービスと使用状況について、部門およびコスト センター別に整理し、レポートします。 エンタープライズ管理者は、次のことができます。

- 部署を追加または削除する。
- アカウントを部署に関連付ける。
- 部署管理者を作成する。
- 部署管理者に価格とコストの表示を許可する。

部門管理者は、部門に新しいアカウントを追加できます。 部門からアカウントを削除できますが、加入契約からは削除できません。

部門を追加するには:

1. Azure エンタープライズ ポータルにサインインします。
1. 左側のペインで、 **[管理]** を選択します。
1. **[部署]** タブを選択し、 **[+ 部署の追加]** を選択します。
1. 情報を入力します。
   部署名は唯一の必須フィールドです。 これは 3 文字以上である必要があります。
1. 完了したら、 **[追加]** を選択します。

## <a name="add-a-department-administrator"></a>部署管理者を追加する

部署を作成した後、エンタープライズ管理者は部署管理者を追加し、それぞれを部署に関連付けることができます。 部署管理者は、部署に関する次の作業を行うことができます。

- 他の部門管理者を作成する
- 名前やコスト センターなどの部署のプロパティを表示および編集する
- アカウントの追加
- アカウントを削除する
- 使用量の詳細をダウンロードする
- 毎月の使用量と料金を表示する<sup>1</sup>

> <sup>1</sup> エンタープライズ管理者がこれらのアクセス許可を付与する必要があります。 部署の月ごとの使用状況と料金を表示するアクセス許可が付与されていても表示できない場合は、パートナーにお問い合わせください。

### <a name="to-add-a-department-administrator"></a>部署管理者を追加するには

エンタープライズ管理者として:

1. Azure エンタープライズ ポータルにサインインします。
1. 左側のペインで、 **[管理]** を選択します。
1. **[部署]** タブを選択し、部署を選択します。
1. **[+ 管理者の追加]** を選択し、必要な情報を追加します。
1. 読み取り専用アクセスの場合は、 **[読み取り専用]** オプションを **[はい]** に設定し、 **[追加]** を選択します。

![[部門管理者の追加] ダイアログ ボックスを示す例](./media/ea-portal-get-started/ea-create-add-department-admin.png)

### <a name="to-set-read-only-access"></a>読み取り専用アクセス権を設定するには

部門管理者に読み取り専用アクセス権を付与することができます。

- 新しい部署管理者を作成するには、読み取り専用オプションを **[はい]** に設定します。

- 既存の部門管理者を編集するには:
   1. 部署を選択し、編集する**部署管理者**の横にある鉛筆記号を選択します。
   1. 読み取り専用オプションを **[はい]** に設定して、 **[保存]** を選択します。

エンタープライズ管理者には、部署管理者のアクセス許可が自動的に設定されます。

## <a name="add-an-account"></a>[アカウントの追加]

アカウントとサブスクリプションの構造は、管理方法と、請求書やレポートでの表示方法に影響します。 一般的な組織の構造の例としては、事業部、機能チーム、地理的な場所などがあります。

アカウントを追加するには:

1. Azure エンタープライズ ポータルで、左側のナビゲーション領域の **[管理]** を選択します。
1. **[アカウント]** タブを選択します。 **[アカウント]** ページで、 **[+ アカウントの追加]** を選択します。
1. 部署を選択するか、割り当てなしのままにして、必要な認証の種類を選択します。
1. レポートでアカウントを識別するためのフレンドリ名を入力します。
1. 新しいアカウントに関連付ける**アカウント所有者のメール** アドレスを入力します。
1. メール アドレスを確認し、 **[追加]** を選択します。

![アカウントのリストと [+ アカウントの追加] オプションを示す例](./media/ea-portal-get-started/create-ea-add-an-account.png)

別のアカウントを追加するには、 **[別アカウントの追加]** を選択するか、左側のツール バーの右下隅にある **[追加]** を選択します。

アカウントの所有権を確認するには:

1. Azure エンタープライズ ポータルにサインインします。
1. 状態を表示します。

   状態は、 **[保留中]** から **[開始日/終了日]** に変わるはずです。 開始日/終了日は、ユーザーが最初にサインインした日付と契約終了日です。
1. Azure エンタープライズ ポータルに初めてサインインするときに**警告**メッセージが表示されるときは、アカウント所有者は、 **[続行]** を選択してアカウントをアクティブ化する必要があります。

## <a name="change-account-owner"></a>アカウント所有者を変更する

エンタープライズ管理者は、Azure エンタープライズ ポータルを使用して、加入契約のサブスクリプション アカウント所有権を譲渡できます。 このアクションでは、ソース ユーザー アカウントのすべてのサブスクリプションが、ターゲット ユーザー アカウントに転送されます。

アカウントを転送するときは、次の重要な情報に注意してください。

- 次のような転送を行うことができます。
  - 職場または学校アカウントから、別の職場または学校アカウントに。
  - Microsoft アカウントから、職場または学校アカウントに。
  - Microsoft アカウントから、別の Microsoft アカウントに。

    ターゲット アカウントは、転送の有効なターゲットとなる有効な Azure コマース アカウントである必要があります。 新しいアカウントの場合は、Azure エンタープライズ ポータルにサインインするときに、Azure コマース アカウントを作成するよう求められます。 既存のアカウントの場合は、最初に新しい Azure サブスクリプションを作成してから、アカウントが対象となるようにする必要があります。

- 職場または学校アカウントから Microsoft アカウントに転送することはできません。

- サブスクリプションの転送が完了すると、Microsoft によってアカウント所有者が更新されます。

ロールベースのアクセス制御 (RBAC) の以下のポリシーを理解してください。

- 同じテナント内の 2 つの組織 ID 間でサブスクリプション転送を行う場合は、RBAC ポリシーと既存のサービス管理者および共同管理者ロールが保持されます。
- その他のサブスクリプション譲渡では、RBAC ポリシーとロールの割り当てが失われます。
- ポリシーと管理者ロールが、異なるディレクトリ間で転送されることはありません。 サービス管理者は、ターゲット アカウントの所有者に更新されます。

アカウント所有者を変更する前に:

1. Azure エンタープライズ ポータルで、 **[アカウント]** タブを表示し、ソース アカウントを特定します。 ソース アカウントはアクティブである必要があります。
1. ターゲット アカウントを特定し、それがアクティブであることを確認します。

すべてのサブスクリプションのアカウント所有権を転送するには:

1. Azure エンタープライズ ポータルにサインインします。
1. 左側のナビゲーション領域で、 **[管理]** を選択します。
1. **[アカウント]** タブを選択し、アカウントをポイントします。
1. 右側のアカウント所有者変更アイコンを選択します。 人に似たアイコンです。
1. 対象のアカウントを選択し、 **[次へ]** を選択します。
1. 転送を確認し、 **[送信]** を選択します。

![アカウント所有者の変更記号を示す画像](./media/ea-portal-get-started/create-ea-create-sub-transfer-account-ownership-of-sub.png)

単一のサブスクリプションのアカウント所有権を転送するには:

1. Azure エンタープライズ ポータルにサインインします。
1. 左側のナビゲーション領域で、 **[管理]** を選択します。
1. **[アカウント]** タブを選択し、アカウントをポイントします。
1. 右側にあるサブスクリプション譲渡アイコンを選択します。 ページに似たアイコンです。
1. 対象のサブスクリプションを選択し、 **[次へ]** を選択します。
1. 転送を確認してから、 **[送信]** を選択します。

![サブスクリプションの転送記号を示す画像](./media/ea-portal-get-started/ea-transfer-subscriptions.png)

Azure エンタープライズ ポータルでのユーザー管理については、次のビデオをご覧ください。

> [!VIDEO https://www.youtube.com/embed/621jVkvmwm8]

## <a name="create-a-subscription"></a>サブスクリプションの作成

アカウント所有者は、サブスクリプションの表示と管理を行うことができます。 サブスクリプションを使用して、組織内のチームに開発環境やプロジェクトへのアクセスを許可できます。 たとえば、テスト、運用、開発、ステージングなどです。

アプリケーション環境ごとに異なるサブスクリプションを作成すると、各環境のセキュリティ保護に役立ちます。

- また、サブスクリプションごとに異なるサービス管理者アカウントを割り当てることもできます。
- サブスクリプションを任意の数のサービスに関連付けることができます。
- アカウント所有者は、サブスクリプションを作成し、アカウント内の各サブスクリプションにサービス管理者アカウントを割り当てます。

### <a name="add-a-subscription"></a>サブスクリプションの追加

サブスクリプションを追加するには、次の情報を使用します。

アカウントにサブスクリプションを初めて追加するときに、マイクロソフト オンライン サブスクリプション契約 (MOSA) と料金プランに同意するように求められます。 これらは Enterprise Agreement のお客様には適用されませんが、MOSA と料金はプランはサブスクリプションを作成するために必要です。 Microsoft Azure エンタープライズ契約の加入契約変更契約書は、上記の項目よりも優先され、契約関係は変更されません。 メッセージが表示されたら、条項に同意することを示すボックスを選択します。

サブスクリプションが作成されるときの既定の名前は、"_Microsoft Azure エンタープライズ_" です。 加入契約内の他のサブスクリプションと区別し、エンタープライズ レベルのレポートで認識できるようにするため、名前を変更してもかまいません。

サブスクリプションを追加するには:

1. Azure エンタープライズ ポータルで、アカウントにサインインします。
1. **[管理者]** タブを選択し、ページの上部にある **[サブスクリプション]** を選択します。
1. アカウントのアカウント所有者としてサインインしていることを確認します。
1. **[+ サブスクリプションの追加]** を選択し、 **[購入]** を選択します。

   アカウントにサブスクリプションを初めて追加するときは、連絡先情報を入力する必要があります。 サブスクリプションをさらに追加すると、連絡先情報が自動的に追加されます。

1. **[サブスクリプション]** を選択し、作成したサブスクリプションを選択します。
1. **[サブスクリプション詳細の編集]** を選択します。
1. **[サブスクリプション名]** と **[サービス管理者]** を編集し、チェック マークを選択します。

   サブスクリプション名はレポートに表示されます。 それは、開発ポータルでサブスクリプションに関連付けられているプロジェクトの名前です。

新しいサブスクリプションがサブスクリプション リストに表示されるまで、最大 24 時間かかることがあります。 サブスクリプションを作成した後、次のことができます。

- [サブスクリプションの詳細を編集する](https://account.azure.com/Subscriptions)
- [サブスクリプション サービスを管理する](https://portal.azure.com/#home)

## <a name="transfer-an-enterprise-subscription-to-a-pay-as-you-go-subscription"></a>エンタープライズ サブスクリプションを従量課金制サブスクリプションに譲渡する

従量課金制料金の個々のサブスクリプションにエンタープライズ サブスクリプションを譲渡するには、Azure エンタープライズ ポータルで新しいサポート リクエストを作成する必要があります。 サポート リクエストを作成するには、 **[ヘルプとサポート]** 領域の **[+ 新しいサポート リクエスト]** を選択します。

## <a name="associate-an-existing-account-with-your-pay-as-you-go-subscription"></a>既存のアカウントを従量課金制サブスクリプションに関連付ける

Azure portal に Microsoft Azure アカウントが既にある場合、Enterprise Agreement 加入契約と関連付けるには、関連付ける学校、職場、または Microsoft アカウントを入力します。

### <a name="associate-an-existing-account"></a>既存のアカウントを関連付ける

1. Azure エンタープライズ ポータルで、 **[管理]** を選択します。
1. **[アカウント]** タブを選択します。
1. **[+ アカウントの追加]** を選択します。
1. 既存の Azure アカウントに関連付ける職場、学校、または Microsoft アカウントを入力します。
1. 既存の Azure アカウントに関連付けるアカウントを確認します。
1. レポートでこのアカウントを識別するために使用する名前を指定します。
1. **[追加]** を選択します。
1. さらにアカウントを追加するには、 **[+ アカウントの追加]** オプションをもう一度選択するか、または **[管理者]** ボタンを選択してホーム ページに戻ります。
1. **[アカウント]** ページを表示すると、新しく追加したアカウントが **[保留中]** の状態で表示されます。

### <a name="confirm-account-ownership"></a>アカウントの所有権を確認する

1. 指定した職場、学校、または Microsoft アカウントに関連付けられているメール アカウントにサインインします。
1. "_Invitation to Activate your Account on the Microsoft Azure Service from Microsoft Volume Licensing_" (Microsoft ボリューム ライセンスから Microsoft Azure Service でアカウントをアクティブ化するための招待) という件名の電子メール通知を開きます。
1. 招待の **[Log into the Microsoft Azure Enterprise Portal]\(Microsoft Azure エンタープライズ ポータルにログインします\)** リンクを選択します。
1. **[サインイン]** をクリックします。
1. 職場、学校、または Microsoft アカウントとパスワードを入力してサインインし、アカウントの所有権を確認します。

### <a name="azure-marketplace"></a>Azure Marketplace

ほとんどのサブスクリプションは従量課金制環境から Azure Enterprise Agreement に変換できますが、Azure Marketplace サービスはできません。 すべてのサブスクリプションと料金を 1 つのビューで表示するために、Azure Marketplace サービスを Azure エンタープライズ ポータルに追加することをお勧めします。

1. Azure エンタープライズ ポータルにサインインします。
1. 左側のナビゲーションで **[管理]** を選択します。
1. **[加入契約]** タブを選択します。
1. **[加入契約の詳細]** セクションを表示します。
1. [Azure Marketplace] フィールドの右側にある鉛筆アイコンを選択して有効にします。 **[保存]** を選択します。

これで、アカウント所有者は、以前に従量課金制サブスクリプションで所有していた Azure Marketplace サービスを購入できるようになります。

Azure EA 加入契約で新しい Azure Marketplace サブスクリプションをアクティブにした後、従量課金制環境で作成した Azure Marketplace サブスクリプションをキャンセルします。 このステップは、従量課金制の支払い方法の期限が切れた場合に、Azure Marketplace サブスクリプションが無効な状態にならないようにするために重要です。

### <a name="msdn"></a>MSDN

MSDN サブスクリプションは MSDN Dev/Test に自動的に変換され、Azure EA プランの既存の金融クレジットは失われます。

### <a name="azure-in-open"></a>Azure イン オープン プラン

Azure イン オープン プランのサブスクリプションを Enterprise Agreement に関連付けると、未使用分の Azure イン オープン プランのクレジットは失われます。 したがって、Enterprise Agreement にアカウントを追加する前に、Azure イン オープン プラン サブスクリプションのすべてのクレジットを使用することをお勧めします。  

### <a name="accounts-with-support-subscriptions"></a>サポート サブスクリプションを持つアカウント

Enterprise Agreement にサポート サブスクリプションがない場合、サポート サブスクリプションを持つ既存のアカウントを Azure エンタープライズ ポータルに追加すると、MOSA サポート サブスクリプションは自動的に譲渡されません。 猶予期間 (次の月の終わりまで) の間に、Azure EA でサポート サブスクリプションを再購入する必要があります。

## <a name="view-usage-summary-and-download-reports"></a>使用状況の概要を表示してレポートをダウンロードする

エンタープライズ管理者は、Azure エンタープライズ ポータルで使用状況データ、消費された年額コミットメント、および追加使用量に関する料金の概要を表示できます。 料金は、すべてのアカウントとサブスクリプションにわたって概要レベルで示されます。

特定のアカウントの詳細な使用状況を表示するには、使用状況の詳細レポートをダウンロードします。

1. Azure エンタープライズ ポータルにサインインします。
1. **レポート**を選択します。
1. **[利用状況のダウンロード]** タブを選択します。
1. レポートの一覧で、取得する月次レポートの **[ダウンロード]** を選択します。

   > [!NOTE]
   > 使用状況の詳細レポートには、適用される税金は含まれません。
   >
   > 使用が発生してからレポートに反映されるまでに、最大 8 時間の待機時間が発生する場合があります。

使用状況の概要レポートとグラフを表示するには:

1. Azure エンタープライズ ポータルにサインインします。

1. コミットメント期間を選択します。

   **[使用状況の概要]** の日付範囲を変更するには、ページの右上で **[M]** (月単位) から **[C]** (カスタム) に切り替えて、カスタムの開始日と終了日を入力します。

   ![カスタム ビューで使用状況の概要を作成および表示してレポートをダウンロードする](./media/ea-portal-get-started/create-ea-view-usage-summary-and-download-reports-custom-view.png)
1. 追加の詳細を表示するには、グラフで期間または月を選択します。

   - グラフには、使用済み量の内訳、サービスの過剰請求、個別請求の料金、および Azure Marketplace の料金と共に、前月比の使用状況が示されます。
   - 選択した月について、グラフの下のフィールドを使用して、部署、アカウント、サブスクリプションでフィルター処理できます。
   - **[サービスごとに請求]** と **[階層ごとに請求]** を切り替えることができます。
   - 関連するセクションを展開することで、 **[Azure サービス]** 、 **[個別請求の料金]** 、 **[Azure Marketplace]** の詳細を表示します。

使用状況を表示する方法については、次のビデオをご覧ください。

> [!VIDEO https://www.youtube.com/embed/Cv2IZ9QCn9E]

### <a name="download-csv-reports"></a>CSV レポートをダウンロードする

エンタープライズ管理者は [月単位レポートのダウンロード] ページを使用して、以下のレポートを CSV ファイルとしてダウンロードします。

- 残高と料金
- 使用状況の詳細
- Azure Marketplace の料金
- Price Sheet

レポートをダウンロードするには:

1. Azure エンタープライズ ポータルで、 **[レポート]** を選択します。
2. ページの上部にある **[使用状況のダウンロード]** を選択します。
3. 月のレポートの横にある **[ダウンロード]** を選択します。

   > [!NOTE]
   > 使用発生日からレポートに使用状況が表示されるまでに、最大 5 日間の待機時間が発生する場合があります。
   >
   > Safari で CSV ファイルを Excel にダウンロードするユーザーの場合、書式設定エラーが発生することがあります。 エラーを回避するには、テキスト エディターを使用してファイルを開きます。

![[使用状況のダウンロード] ページを示す例](./media/ea-portal-get-started/create-ea-download-csv-reports.png)

使用状況に関する情報をダウンロードする方法については、次のビデオをご覧ください。

> [!VIDEO https://www.youtube.com/embed/eY797htT1qg]

### <a name="advanced-report-download"></a>詳細なレポートのダウンロード

詳細なレポートのダウンロードを使用して、特定の日付範囲またはアカウントについてのレポートを入手できます。 大きなレコード セットに対応するため、出力ファイルは CSV 形式になっています。

1. Azure エンタープライズ ポータルで、 **[詳細なレポートのダウンロード]** を選択します。
1. 適切な日付範囲と適切なアカウントを選択します。
1. **[使用状況データのリクエスト]** を選択します。
1. レポートの状態が **[ダウンロード]** に更新されるまで、 **[更新]** ボタンを選択します。
1. レポートをダウンロードします。

### <a name="download-usage-reports-and-billing-information-for-a-prior-enrollment"></a>以前の加入契約の使用状況レポートと課金情報をダウンロードする

加入契約の転送が行われた後で、前の加入契約の使用状況レポートと課金情報をダウンロードできます。 履歴レポートは、Azure エンタープライズ ポータルと Cost Management の両方で使用できます。

Azure エンタープライズ ポータルでは、非アクティブな加入契約はフィルターによって表示から除外されます。 転送済みの非アクティブな加入契約を表示するには、 **[アクティブ]** ボックスをオフにする必要があります。  

![[アクティブ] ボックスをオフにすると、ユーザーはアクティブでない加入契約を確認できる](./media/ea-portal-get-started/unchecked-active-box.png)

## <a name="azure-ea-term-glossary"></a>Azure EA 用語集

- **アカウント**:Azure エンタープライズ ポータルでの組織単位。 サブスクリプションの管理とレポートのために使用されます。
- **アカウント所有者**:Azure でサブスクリプションとサービス管理者を管理するユーザー。 このアカウントとそれに関連付けられているサブスクリプションの使用状況データを表示できます。
- **変更契約サブスクリプション**:加入契約変更契約書における 1 年間または同時終了サブスクリプション。
- **コミットメント**:この前払いに対する使用状況の割引コミットメント料金での Azure サービスの年額コミットメント。
- **部門管理者**:部署の管理、新しいアカウントとアカウント所有者の作成、管理対象部署の使用状況の詳細の表示、コストの表示 (アクセス許可が付与された場合) を行うユーザー。
- **加入契約番号**:Enterprise Agreement に関連付けられている特定の加入契約を識別するために Microsoft によって提供される一意の識別子。
- **エンタープライズ管理者**:Azure で部署、部署所有者、アカウント、アカウント所有者を管理するユーザー。 エンタープライズ加入契約に関連付けられているすべてのアカウントとサブスクリプションの使用状況データ、請求数量、および未請求料金を表示できるだけでなく、エンタープライズ管理者を管理することもできます。
- **Enterprise Agreement**:Microsoft テクノロジで組織全体を標準化し、Microsoft のソフトウェア標準において情報技術を維持することを希望する、一元的な購入を行う顧客向けの Microsoft ライセンス契約。
- **Enterprise Agreement 加入契約**:Microsoft 製品を割引料金で大量に提供する、Enterprise Agreement プログラムの加入契約。
- **Microsoft アカウント**:複数のサイトにアクセスするときに、単一の資格情報を使用してユーザーを認証できるようにする Web ベース サービス。
- **Microsoft Azure エンタープライズ加入契約変更契約書 (加入契約変更契約書)** : エンタープライズ加入契約の一部として Azure へのアクセスを提供する、企業によって署名される変更契約書。
- **Azure エンタープライズ ポータル**: Azure アカウントとその関連サブスクリプションを管理するために企業のお客様によって使用されるポータル。
- **消費済みリソース数量**:1 か月間に使用された個別の Azure サービスの数量。
- **サービス管理者**:Azure エンタープライズ ポータルでサブスクリプションと開発者プロジェクトにアクセスして管理するユーザー。
- **サブスクリプション**:Azure エンタープライズ ポータル サブスクリプションを表します。これは、同じサービス管理者によって管理される Azure サービスのコンテナーです。
- **職場または学校アカウント**:クラウドへのフェデレーションを使用して Active Directory を設定しており、1 つのテナントにすべてのアカウントが存在する組織。

### <a name="enrollment-statuses"></a>加入契約の状態

- **Pending**: 登録管理者は Azure エンタープライズ ポータルにサインインする必要があります。 サインインすると、加入契約がアクティブな状態に切り替わります。
- **[アクティブ]** : 加入契約はアクティブであり、Azure エンタープライズ ポータルでアカウントとサブスクリプションを作成できます。 加入契約は、Enterprise Agreement の終了日までアクティブな状態が維持されます。
- **無期限の延長期間**:Enterprise Agreement の終了日に達した後、無期限の延長期間の状態になります。 これにより、拡張期間にオプトインした Azure EA のお客様は、Enterprise Agreement の終了後に、Azure サービスを引き続き無期限に使用できます。

   Azure EA 加入契約が Enterprise Agreement の終了日に達する前に、加入契約管理者は次のどのオプションを採用するかを決定する必要があります。

  - 年額コミットメントを追加して登録を更新する。
  - 新しい加入契約に転送する。
  - マイクロソフト オンライン サブスクリプション プログラム (MOSP) に移行する。
  - 登録に関連付けられているすべてのサービスが無効になることを確認する。
- **期限切れ**:Azure EA のお客様は延長期間からオプトアウトされ、Azure EA 加入契約は Enterprise Agreement の終了日に達しています。 加入登録は期限切れになり、関連付けられているすべてのサービスは無効になります。
- **転送済み**:関連付けられているすべてのアカウントとサービスが新しい加入契約に転送された加入契約は、転送済みの状態で表示されます。
  >[!NOTE]
  > 更新時に新しい登録番号が生成された場合、加入契約は自動的には転送されません。 自動転送を容易にするには、前の加入契約番号を、お客様の更新事務処理に含める必要があります。

## <a name="get-started-on-azure-ea---faq"></a>Azure EA の使用開始の際によく寄せられる質問

このセクションでは、オンボード プロセス中にお客様から寄せられる一般的な質問について詳しく説明します。  

### <a name="can-i-associate-my-existing-azure-account-to-azure-ea-enrollment"></a>既存の Azure アカウントを Azure EA 加入契約に関連付けることはできますか?

はい。 自分がアカウント所有者であるすべての Azure サブスクリプションが、Enterprise Agreement に変換されます。 これには、Visual Studio、AzurePass、MPN、BizSpark など、月単位のクレジットを使用するサブスクリプションが含まれます。 そのようなサブスクリプションを変換すると、月単位のクレジットが失われます。

### <a name="i-accidentally-associated-my-existing-azure-account-with-azure-ea-enrollment-as-a-result-i-lost-my-monthly-credit-can-i-get-my-monthly-credit-back"></a>既存の Azure アカウントを Azure EA 加入契約に誤って関連付けてしまいました。 その結果、月単位のクレジットが失われました。 月単位のクレジットを元に戻すことはできますか?

Visual Studio サブスクリプションと同じ資格情報を使用して Azure EA アカウント所有者としてサインインした場合、次のいずれかのアクションを実行して、Visual Studio サブスクリプションの個々の Azure 特典を復旧できます。

- 関連付けられている Azure サブスクリプションを削除または移動した後、Azure エンタープライズ ポータルからアカウント所有者を削除します。 次に、個別の Visual Studio Azure 特典に新たにサインアップします。
- VLSC の管理サイトから Visual Studio サブスクライバーを削除し、今度は異なる資格情報を持つアカウントにサブスクリプションを再度割り当てます。 次に、個別の Visual Studio Azure 特典に新たにサインアップします。

### <a name="what-type-of-subscription-should-i-create"></a>どのような種類のサブスクリプションを作成する必要がありますか?

Azure エンタープライズ ポータルには、企業のお客様向けに 2 種類のサブスクリプションが用意されています。

- Microsoft Azure エンタープライズ。次の場合に最適です。
  - すべての運用環境での使用
  - インフラストラクチャへの支出に基づく最適な料金

  詳細については、[Azure 営業担当者にお問い合わせください](https://azure.microsoft.com/pricing/enterprise-agreement/)。

- Enterprise Dev/Test。次の場合に最適です。
  - チームによるすべての開発/テスト ワークロード
  - 中規模から大規模の個別の開発/テスト ワークロード
  - 特別な MSDN イメージと優先サービス レートへのアクセス

  詳細については、[Enterprise Dev/Test のオファー](https://azure.microsoft.com/offers/ms-azr-0148p/)に関する記事を参照してください。

### <a name="is-it-possible-to-transfer-subscription-ownership-to-another-account"></a>Azure サブスクリプションの所有権を別のアカウントに譲渡できますか?

はい、サブスクリプションの所有権は別のアカウントに譲渡できます。 たとえば、アカウント A に 3 つのサブスクリプションがある場合、エンタープライズ管理者は、アカウント B、アカウント C、アカウント D にそれぞれ 1 つのサブスクリプションを譲渡できます。または、すべてのサブスクリプションをアカウント E に譲渡することもできます。

サブスクリプションを譲渡するには:

1. Azure エンタープライズ ポータルで、 **[管理]**  >  **[アカウント]** を選択します。
1. 右端にある **[アカウント]** をポイントすると、**所有権の譲渡** (人のアイコン) と**サブスクリプションの譲渡** (リスト アイコン) のオプションが表示されます。 これらのオプションは、アクティブなアカウントに対してのみ表示されます。

### <a name="my-subscription-name-is-the-same-as-the-offer-name-should-i-change-the-subscription-name-to-something-meaningful-to-my-organization"></a>サブスクリプション名がプラン名と同じになっています。 サブスクリプション名を組織にとって意味のあるものに変更する必要がありますか?

サブスクリプションを作成するとき、名前は既定で選択したプランの種類になります。 サブスクリプション名を変更して、サブスクリプションを簡単に追跡できるようなものにすることをお勧めします。

名前を変更するには:

1. [https://account.windowsazure.com](https://account.windowsazure.com) にサインインします。
1. サブスクリプションの一覧を選択します。
1. 編集するサブスクリプションを選択します。
1. **[サブスクリプションの管理]** アイコンを選択します。
1. サブスクリプションの詳細を編集します。

### <a name="how-can-i-track-costs-incurred-by-a-cost-center"></a>発生したコストをコスト センター別に追跡するにはどうすればよいですか?

コスト センター別にコストを追跡するには、次のいずれかのレベルでコスト センターを定義する必要があります。

- 部署
- Account
- サブスクリプション

ニーズに応じて、同じコスト センターを使用して、特定のコスト センターに関連付けられた使用状況とコストを追跡できます。

たとえば、複数の部署が関与する特別なプロジェクトのコストを追跡するには、サブスクリプション レベルでコスト センターを定義して、使用状況とコストを追跡できます。

コスト センターをサービス レベルで定義することはできません。 サービス レベルで使用状況を追跡する場合は、サービス レベルで利用可能な "_タグ_" 機能を使用できます。

### <a name="how-do-i-track-usage-and-spend-by-different-departments-in-my-organization"></a>組織内のさまざまな部門ごとの使用状況と支出を追跡するにはどうすればよいですか?

Azure EA 加入契約において、必要な数の部署を作成できます。 使用状況を正しく追跡するには、サブスクリプションが部署間で共有されないようにします。

部署とサブスクリプションを作成した後、使用状況レポートにデータを表示できます。 この情報は、部署レベルで使用状況を追跡し、コストを管理し、支出を管理するのに役立ちます。

Reporting API を使用して、使用状況データにアクセスすることもできます。 詳細な情報とサンプル コードについては、[Azure Enterprise REST API](https://docs.microsoft.com/azure/cost-management-billing/manage/ea-portal-rest-apis) に関するページを参照してください。

### <a name="can-i-set-a-spending-quota-and-get-alerts-as-i-approach-my-limit"></a>利用量クォータを設定して、制限に近づいたらアラートを受け取ることはできますか?

部署レベルで利用量クォータを設定できます。これにより、使用制限が、定義したクォータの 50%、75%、90%、および 100% に達すると通知されます。

利用量クォータを定義するには、部署を選択した後、編集アイコンを選択します。 利用量制限の詳細を編集した後、 **[保存]** を選択します。

### <a name="i-used-resource-groups-to-implement-rbac-and-track-usage-how-can-i-view-the-associated-usage-details"></a>リソース グループを使用して RBAC を実装し、使用状況を追跡しました。 関連する使用状況の詳細を表示するにはどうすればよいですか?

"_リソース グループ_" と "_タグ_" を使用している場合、この情報はサービス レベルで追跡され、詳細な使用状況のダウンロード (CSV) ファイルでアクセスできます。 Azure エンタープライズ ポータルの[使用状況レポートのダウンロード](https://ea.azure.com/report/downloadusage)を参照してください。

API で使用状況にアクセスすることもできます。 詳細な情報とサンプル コードについては、[Azure Enterprise REST API](https://docs.microsoft.com/azure/cost-management-billing/manage/ea-portal-rest-apis) に関するページを参照してください。

> [!NOTE]
> タグを適用できるのは、Azure Resource Manager の操作をサポートするリソースのみです。 仮想マシン、仮想ネットワーク、またはストレージをクラシック デプロイ モデル (クラシック ポータルなど) を使用して作成した場合、そのリソースにタグを適用することはできません。 タグ付けをサポートするには、Resource Manager を介してこれらのリソースを再デプロイする必要があります。 その他のすべてのリソースでは、タグ付けがサポートされています。

### <a name="can-i-perform-analyses-using-power-bi"></a>Power BI を使用して分析を実行できますか?

はい。 Power BI 用の Microsoft Azure エンタープライズ コンテンツ パックを使用すると、次のことができます。

- エンタープライズ加入契約に対する Azure の使用状況をすばやくインポートして分析します。
- 使用量が最も多い部署、アカウント、またはサブスクリプションを明らかにします。
- 組織で最もよく使用されたサービスを確認します。
- 支出と使用状況の傾向を追跡します。

Power BI を使用するには:

1. Power BI の Web サイトに移動します。
1. 有効な職場または学校アカウントでサインインします。

   職場または学校アカウントは、Azure エンタープライズ ポータルを介して加入契約にアクセスするために使用されたのと同じものでも別のものでもかまいません。
1. サービスのダッシュボードで、[Microsoft Azure エンタープライズ] のタイルを選択して、 **[接続]** を選択します。
1. **[Azure エンタープライズに接続]** 画面で、以下を入力します。
    - Azure 環境 URL: [https://ea.azure.com](https://ea.azure.com)
    - 月数: 1 から 36
    - 加入契約番号: 自分の加入契約番号
1. **[次へ]** を選択します。
1. **[アカウント キー]** ボックスに、API キーを入力します。

   API キーは、Azure エンタープライズ ポータルで確認できます。 **[利用状況のダウンロード]** タブで、 **[API アクセス キー]** を選択します。 それをコピーし、Power BI の **[アカウント キー]** ボックスにキーを貼り付けます。

データ セットのサイズによっては、Power BI にデータが読み込まれるまでに 5 から 30 分かかることがあります。

Power BI レポートは、課金情報を表示するアクセス権がある、Azure EA ダイレクト、パートナー、およびインダイレクトのお客様にご利用いただけます。

## <a name="next-steps"></a>次のステップ

- Azure エンタープライズ ポータルの管理者は、[Azure エンタープライズ ポータルの管理](ea-portal-administration.md)に関する記事を読んで、一般的な管理タスクについて学習する必要があります。
- Azure エンタープライズ ポータルの問題のトラブルシューティングに関するヘルプが必要な場合は、[Azure エンタープライズ ポータルへのアクセスのトラブルシューティング](ea-portal-troubleshoot.md)に関する記事を参照してください。
- Azure EA オンボード ガイドについては、[Azure EA オンボード ガイド (PDF)](https://ea.azure.com/api/v3Help/v2AzureEAOnboardingGuide) を参照してください。
