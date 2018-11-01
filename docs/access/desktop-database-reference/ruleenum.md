---
title: RuleEnum (référence de base de données du bureau Access)
TOCTitle: RuleEnum
ms:assetid: 5b59f202-315b-09b7-8505-9ac08ceccb3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249317(v=office.15)
ms:contentKeyID: 48545071
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: bac61333ab9d8c7abdbbb23a8207716f50c4ac21
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879089"
---
# <a name="ruleenum"></a><span data-ttu-id="a9b3f-102">RuleEnum</span><span class="sxs-lookup"><span data-stu-id="a9b3f-102">RuleEnum</span></span>

<span data-ttu-id="a9b3f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9b3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9b3f-104">Indique la règle à appliquer en cas de suppression d'un objet [Key](key-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="a9b3f-104">Specifies the rule to follow when a [Key](key-object-adox.md) is deleted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9b3f-105">Constant</span><span class="sxs-lookup"><span data-stu-id="a9b3f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a9b3f-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9b3f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a9b3f-107">Description</span><span class="sxs-lookup"><span data-stu-id="a9b3f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9b3f-108"><strong>propriété DeleteRule</strong></span><span class="sxs-lookup"><span data-stu-id="a9b3f-108"><strong>adRICascade</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b3f-109">1</span><span class="sxs-lookup"><span data-stu-id="a9b3f-109">1</span></span></p></td>
<td><p><span data-ttu-id="a9b3f-110">Modifications en cascade.</span><span class="sxs-lookup"><span data-stu-id="a9b3f-110">Cascade changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9b3f-111"><strong>adRINone</strong></span><span class="sxs-lookup"><span data-stu-id="a9b3f-111"><strong>adRINone</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b3f-112">0</span><span class="sxs-lookup"><span data-stu-id="a9b3f-112">0</span></span></p></td>
<td><p><span data-ttu-id="a9b3f-p101">Valeur par défaut. Aucune action n'est effectuée.</span><span class="sxs-lookup"><span data-stu-id="a9b3f-p101">Default. No action is taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9b3f-115"><strong>adRISetDefault</strong></span><span class="sxs-lookup"><span data-stu-id="a9b3f-115"><strong>adRISetDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b3f-116">3</span><span class="sxs-lookup"><span data-stu-id="a9b3f-116">3</span></span></p></td>
<td><p><span data-ttu-id="a9b3f-117">La clé étrangère a la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9b3f-117">Foreign key value is set to the default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9b3f-118"><strong>adRISetNull</strong></span><span class="sxs-lookup"><span data-stu-id="a9b3f-118"><strong>adRISetNull</strong></span></span></p></td>
<td><p><span data-ttu-id="a9b3f-119">2</span><span class="sxs-lookup"><span data-stu-id="a9b3f-119">2</span></span></p></td>
<td><p><span data-ttu-id="a9b3f-120">La clé étrangère a la valeur Null.</span><span class="sxs-lookup"><span data-stu-id="a9b3f-120">Foreign key value is set to null.</span></span></p></td>
</tr>
</tbody>
</table>

