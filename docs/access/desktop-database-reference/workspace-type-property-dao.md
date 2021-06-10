---
title: Workspace.Type, propriété (DAO)
TOCTitle: Type Property
ms:assetid: 89e59280-d2cd-b6a2-16c5-9f14f42fdd99
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197086(v=office.15)
ms:contentKeyID: 48546177
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e698963d60809e8d88c4ff87532fb7b74cff275c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311304"
---
# <a name="workspacetype-property-dao"></a><span data-ttu-id="730c4-102">Workspace.Type, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="730c4-102">Workspace.Type property (DAO)</span></span>


<span data-ttu-id="730c4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="730c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="730c4-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="730c4-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="730c4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="730c4-106">Syntax</span></span>

<span data-ttu-id="730c4-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="730c4-107">*expression* .Type</span></span>

<span data-ttu-id="730c4-108">*expression* Variable qui représente un objet **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="730c4-108">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="730c4-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="730c4-109">Remarks</span></span>

<span data-ttu-id="730c4-110">Pour un objet **Workspace**, les valeurs des paramètres et de retour possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="730c4-110">For a **Workspace** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="730c4-111">Constante</span><span class="sxs-lookup"><span data-stu-id="730c4-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="730c4-112">Type d'espace de travail</span><span class="sxs-lookup"><span data-stu-id="730c4-112">Workspace type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="730c4-113"><strong>dbUseJet</strong></span><span class="sxs-lookup"><span data-stu-id="730c4-113"><strong>dbUseJet</strong></span></span></p></td>
<td><p><span data-ttu-id="730c4-114">L'<strong>espace de travail</strong> est connecté au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="730c4-114">The <strong>Workspace</strong> is connected to the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="730c4-115"><strong>dbUseODBC</strong></span><span class="sxs-lookup"><span data-stu-id="730c4-115"><strong>dbUseODBC</strong></span></span></p></td>
<td><p><span data-ttu-id="730c4-116">L'<strong>espace de travail</strong> est connecté à une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="730c4-116">The <strong>Workspace</strong> is connected to an ODBC data source.</span></span></p></td>
</tr>
</tbody>
</table>

