---
title: ActionEnum, spécifiant (référence de base de données de bureau Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f098adb42df39d1509a6d22decd8d2cead684f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280655"
---
# <a name="actionenum"></a><span data-ttu-id="1b83f-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="1b83f-102">ActionEnum</span></span>

<span data-ttu-id="1b83f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b83f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b83f-104">Indique le type d’action à effectuer lorsque la méthode [SetPermissions](setpermissions-method-adox.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="1b83f-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b83f-105">Constante</span><span class="sxs-lookup"><span data-stu-id="1b83f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="1b83f-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b83f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="1b83f-107">Description</span><span class="sxs-lookup"><span data-stu-id="1b83f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b83f-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="1b83f-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="1b83f-109">3</span><span class="sxs-lookup"><span data-stu-id="1b83f-109">3</span></span></p></td>
<td><p><span data-ttu-id="1b83f-110">Les autorisations spécifiées seront refusées au groupe ou à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b83f-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b83f-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="1b83f-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="1b83f-112">0,1</span><span class="sxs-lookup"><span data-stu-id="1b83f-112">1</span></span></p></td>
<td><p><span data-ttu-id="1b83f-113">Le groupe ou l'utilisateur disposera au moins des autorisations demandées.</span><span class="sxs-lookup"><span data-stu-id="1b83f-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b83f-114"><strong>Valeur adAccessRevoke au</strong></span><span class="sxs-lookup"><span data-stu-id="1b83f-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="1b83f-115">4</span><span class="sxs-lookup"><span data-stu-id="1b83f-115">4</span></span></p></td>
<td><p><span data-ttu-id="1b83f-116">Tous les droits d'accès explicites que le groupe ou l'utilisateur possède seront révoqués.</span><span class="sxs-lookup"><span data-stu-id="1b83f-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b83f-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="1b83f-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="1b83f-118">n°2</span><span class="sxs-lookup"><span data-stu-id="1b83f-118">2</span></span></p></td>
<td><p><span data-ttu-id="1b83f-119">Le groupe ou l'utilisateur disposera exactement des autorisations demandées.</span><span class="sxs-lookup"><span data-stu-id="1b83f-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

