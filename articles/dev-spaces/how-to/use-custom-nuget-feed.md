---
title: カスタム NuGet フィードを使用する
services: azure-dev-spaces
author: zr-msft
ms.author: zarhoads
ms.date: 07/17/2019
ms.topic: conceptual
description: カスタム NuGet フィードを使用して、Azure Dev Space 内の NuGet パッケージにアクセスし、使用します。
keywords: Docker, Kubernetes, Azure, AKS, Azure Container Service, コンテナー
manager: gwallace
ms.openlocfilehash: 39984a3b3a1be64a497fb8088559ccfcdee4f1c6
ms.sourcegitcommit: b77e97709663c0c9f84d95c1f0578fcfcb3b2a6c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/22/2019
ms.locfileid: "74325728"
---
# <a name="use-a-custom-nuget-feed-with-azure-dev-spaces"></a>Azure Dev Spaces にカスタム NuGet フィードを使用する

NuGet フィードは、パッケージ ソースをプロジェクトに取り込むための便利な方法を提供します。 Docker コンテナーで依存関係を正しくインストールするためには、Azure Dev Spaces がこのフィードにアクセスする必要があります。

## <a name="set-up-a-nuget-feed"></a>NuGet フィードのセットアップ

`PackageReference` ノード下の `*.csproj` ファイルで、依存関係の[パッケージ参照](https://docs.microsoft.com/nuget/consume-packages/package-references-in-project-files)を追加します。 例:

```xml
<ItemGroup>
    <!-- ... -->
    <PackageReference Include="Contoso.Utility.UsefulStuff" Version="3.6.0" />
    <!-- ... -->
</ItemGroup>
```

プロジェクト フォルダー内に [NuGet.Config](https://docs.microsoft.com/nuget/reference/nuget-config-file) ファイルを作成し、NuGet フィードに対する `packageSources` および `packageSourceCredentials` セクションを設定します。 `packageSources` セクションにはフィード URL が含まれ、これは AKS クラスターからアクセスが可能である必要があります。 `packageSourceCredentials` は、フィードにアクセスするための資格情報です。 例:

```xml
<packageSources>
    <add key="Contoso" value="https://contoso.com/packages/" />
</packageSources>

<packageSourceCredentials>
    <Contoso>
        <add key="Username" value="user@contoso.com" />
        <add key="ClearTextPassword" value="33f!!lloppa" />
    </Contoso>
</packageSourceCredentials>
```

Dockerfile を更新して、`NuGet.Config` ファイルをイメージにコピーします。 例:

```console
COPY ["<project folder>/NuGet.Config", "./NuGet.Config"]
```

> [!TIP]
> Windows では、`NuGet.Config`、`Nuget.Config`、および `nuget.config` はすべて有効なファイル名として機能します。 Linux では、`NuGet.Config` のみがこのファイルの有効なファイル名です。 Azure Dev Spaces では Docker と Linux が使用されるため、このファイルには `NuGet.Config` という名前を付ける必要があります。 名前は手動で、または `dotnet restore --configfile nuget.config` を実行して修正できます。


Git を使用している場合は、NuGet フィードの資格情報をバージョン コントロールに入れないでください。 プロジェクトの `.gitignore` に `NuGet.Config` を追加して、`NuGet.Config` ファイルがバージョン コントロールに追加されないようにします。 Azure Dev Spaces では、コンテナー イメージのビルド プロセス中にこのファイルが必要になりますが、既定では、同期中に `.gitignore` および `.dockerignore` で定義された規則に従います。 既定の動作を変更し、`NuGet.Config` ファイルの同期を Azure Dev Spaces に許可するには、次のように `azds.yaml` ファイルを更新します。

```yaml
build:
useGitIgnore: true
ignore:
- "!NuGet.Config"
```

Git を使用していない場合は、この手順を省略できます。

Visual Studio Code または Visual Studio で次に `azds up` を実行または `F5` にヒットしたとき、Azure Dev Spaces は `NuGet.Config` ファイルを同期し、それを使用してパッケージの依存関係をインストールします。

## <a name="next-steps"></a>次の手順

[NuGet とそのしくみ](https://docs.microsoft.com/nuget/what-is-nuget)について学びます。