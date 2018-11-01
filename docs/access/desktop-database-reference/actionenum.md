---
title: ActionEnum (référence de base de données du bureau Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 65fe30c558d5fc22563e002f8d19cb78d7ca3e3d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879997"
---
# <a name="actionenum"></a><span data-ttu-id="3485b-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="3485b-102">ActionEnum</span></span>

<span data-ttu-id="3485b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3485b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3485b-104">Indique le type d'action à effectuer lorsque la méthode [SetPermissions](setpermissions-method-adox.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="3485b-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3485b-105">Constant</span><span class="sxs-lookup"><span data-stu-id="3485b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3485b-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="3485b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3485b-107">Description</span><span class="sxs-lookup"><span data-stu-id="3485b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3485b-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="3485b-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="3485b-109">3</span><span class="sxs-lookup"><span data-stu-id="3485b-109">3</span></span></p></td>
<td><p><span data-ttu-id="3485b-110">Les autorisations spécifiées seront refusées au groupe ou à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3485b-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3485b-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="3485b-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="3485b-112">1</span><span class="sxs-lookup"><span data-stu-id="3485b-112">1</span></span></p></td>
<td><p><span data-ttu-id="3485b-113">Le groupe ou l'utilisateur disposera au moins des autorisations demandées.</span><span class="sxs-lookup"><span data-stu-id="3485b-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3485b-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="3485b-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="3485b-115">4</span><span class="sxs-lookup"><span data-stu-id="3485b-115">4</span></span></p></td>
<td><p><span data-ttu-id="3485b-116">Tous les droits d'accès explicites que le groupe ou l'utilisateur possède seront révoqués.</span><span class="sxs-lookup"><span data-stu-id="3485b-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3485b-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="3485b-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="3485b-118">2</span><span class="sxs-lookup"><span data-stu-id="3485b-118">2</span></span></p></td>
<td><p><span data-ttu-id="3485b-119">Le groupe ou l'utilisateur disposera exactement des autorisations demandées.</span><span class="sxs-lookup"><span data-stu-id="3485b-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

