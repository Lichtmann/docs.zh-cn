---
title: 在 Ubuntu 19.04 包管理器上安装 .NET Core - .NET Core
description: 使用包管理器在 Ubuntu 19.04 上安装 .NET Core SDK 和运行时。
author: thraka
ms.author: adegeo
ms.date: 03/17/2020
ms.openlocfilehash: a0a6cedb6dbf572750fcc238aff59b7f66edf44f
ms.sourcegitcommit: 07123a475af89b6da5bb6cc51ea40ab1e8a488f0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/24/2020
ms.locfileid: "80134144"
---
# <a name="ubuntu-1904-package-manager---install-net-core"></a>Ubuntu 19.04 包管理器 - 安装 .NET Core

[!INCLUDE [package-manager-switcher](./includes/package-manager-switcher.md)]

本文介绍如何使用包管理器在 Ubuntu 19.04 上安装 .NET Core。

[!INCLUDE [package-manager-intro-sdk-vs-runtime](includes/package-manager-intro-sdk-vs-runtime.md)]

## <a name="register-microsoft-key-and-feed"></a>注册 Microsoft 密钥和源

安装 .NET 之前，需要：

- 注册 Microsoft 密钥。
- 注册产品存储库。
- 安装必需的依赖项。

每台计算机只需要执行一次此操作。

打开终端并运行以下命令。

```bash
wget https://packages.microsoft.com/config/ubuntu/19.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
```

## <a name="install-the-net-core-sdk"></a>安装 .NET Core SDK

更新可供安装的产品，然后安装 .NET Core SDK。 在终端中，运行以下命令。

```bash
sudo apt-get update
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install dotnet-sdk-3.1
```

> [!IMPORTANT]
> 如果收到类似于“找不到包 dotnet-sdk-3.1”  的错误消息，请参阅[包管理器疑难解答](#troubleshoot-the-package-manager)部分。

## <a name="install-the-aspnet-core-runtime"></a>安装 ASP.NET Core 运行时

更新可供安装的产品，然后安装 ASP.NET Core 运行时。 在终端中，运行以下命令。

```bash
sudo apt-get update
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install aspnetcore-runtime-3.1
```

> [!IMPORTANT]
> 如果收到类似于“找不到包 aspnetcore-runtime-3.1”  的错误消息，请参阅[包管理器疑难解答](#troubleshoot-the-package-manager)部分。

## <a name="install-the-net-core-runtime"></a>安装 .NET Core 运行时

更新可供安装的产品，然后安装 .NET Core 运行时。 在终端中，运行以下命令。

```bash
sudo apt-get update
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install dotnet-runtime-3.1
```

> [!IMPORTANT]
> 如果收到类似于“找不到包 dotnet-runtime-3.1”  的错误消息，请参阅[包管理器疑难解答](#troubleshoot-the-package-manager)部分。

## <a name="how-to-install-other-versions"></a>如何安装其他版本

[!INCLUDE [package-manager-switcher](./includes/package-manager-heading-hack-pkgname.md)]

## <a name="troubleshoot-the-package-manager"></a>包管理器疑难解答

本部分提供有关使用程序包管理器安装 .NET Core 时可能会遇到的常见错误的信息。

### <a name="unable-to-locate"></a>无法定位

如果收到类似于“找不到包 {.NET Core 包}”  的错误消息，请运行以下命令。

```bash
sudo dpkg --purge packages-microsoft-prod && sudo dpkg -i packages-microsoft-prod.deb
sudo apt-get update
sudo apt-get install {the .NET Core package}
```

如果这不起作用，可使用以下命令运行手动安装。

```bash
sudo apt-get install -y gpg
wget -O- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor -o microsoft.asc.gpg
sudo mv microsoft.asc.gpg /etc/apt/trusted.gpg.d/
wget https://packages.microsoft.com/config/ubuntu/19.04/prod.list
sudo mv prod.list /etc/apt/sources.list.d/microsoft-prod.list
sudo chown root:root /etc/apt/trusted.gpg.d/microsoft.asc.gpg
sudo chown root:root /etc/apt/sources.list.d/microsoft-prod.list
sudo apt-get install -y apt-transport-https
sudo apt-get update
sudo apt-get install {the .NET Core package}
```

### <a name="failed-to-fetch"></a>未能提取

[!INCLUDE [package-manager-failed-to-fetch-deb](includes/package-manager-failed-to-fetch-deb.md)]
