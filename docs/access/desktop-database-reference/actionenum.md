---
title: ActionEnum (référence de base de données du bureau Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af0e5fd734c03b88990383b99815d6e35f2c1290
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469527"
---
# <a name="actionenum"></a><span data-ttu-id="439fa-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="439fa-102">ActionEnum</span></span>


<span data-ttu-id="439fa-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="439fa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="439fa-104">Indique le type d'action à effectuer lorsque la méthode [SetPermissions](setpermissions-method-adox.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="439fa-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="439fa-105">Constant</span><span class="sxs-lookup"><span data-stu-id="439fa-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="439fa-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="439fa-106">Value</span></span></p></th>
<th><p><span data-ttu-id="439fa-107">Description</span><span class="sxs-lookup"><span data-stu-id="439fa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="439fa-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="439fa-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="439fa-109">3</span><span class="sxs-lookup"><span data-stu-id="439fa-109">3</span></span></p></td>
<td><p><span data-ttu-id="439fa-110">Les autorisations spécifiées seront refusées au groupe ou à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="439fa-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="439fa-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="439fa-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="439fa-112">1</span><span class="sxs-lookup"><span data-stu-id="439fa-112">1</span></span></p></td>
<td><p><span data-ttu-id="439fa-113">Le groupe ou l'utilisateur disposera au moins des autorisations demandées.</span><span class="sxs-lookup"><span data-stu-id="439fa-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="439fa-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="439fa-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="439fa-115">4</span><span class="sxs-lookup"><span data-stu-id="439fa-115">4</span></span></p></td>
<td><p><span data-ttu-id="439fa-116">Tous les droits d'accès explicites que le groupe ou l'utilisateur possède seront révoqués.</span><span class="sxs-lookup"><span data-stu-id="439fa-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="439fa-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="439fa-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="439fa-118">2</span><span class="sxs-lookup"><span data-stu-id="439fa-118">2</span></span></p></td>
<td><p><span data-ttu-id="439fa-119">Le groupe ou l'utilisateur disposera exactement des autorisations demandées.</span><span class="sxs-lookup"><span data-stu-id="439fa-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

