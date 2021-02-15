---
title: DBEngine.DefaultType, propriété (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294378"
---
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="9402a-102">DBEngine.DefaultType, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="9402a-102">DBEngine.DefaultType property (DAO)</span></span>


<span data-ttu-id="9402a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9402a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9402a-104">Définit ou renvoie une valeur qui indique le type d'espace de travail qui sera utilisé par le prochain objet **[Workspace](workspace-object-dao.md)** créé.</span><span class="sxs-lookup"><span data-stu-id="9402a-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="9402a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9402a-105">Syntax</span></span>

<span data-ttu-id="9402a-106">*.* DefaultType</span><span class="sxs-lookup"><span data-stu-id="9402a-106">*expression* .DefaultType</span></span>

<span data-ttu-id="9402a-107">*expression* Variable représentant un objet **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="9402a-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9402a-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="9402a-108">Remarks</span></span>

<span data-ttu-id="9402a-109">Le paramètre ou la valeur renvoyée peut correspondre à l'une des constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9402a-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="9402a-p101">Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9402a-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="9402a-112">Le paramètre peut être retravaillé pour un espace de travail unique en attériant l’argument type sur **[la méthode CreateWorkspace.](dbengine-createworkspace-method-dao.md)** </span><span class="sxs-lookup"><span data-stu-id="9402a-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>

