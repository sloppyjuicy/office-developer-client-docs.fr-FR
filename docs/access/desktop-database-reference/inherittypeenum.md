---
title: InheritTypeEnum (référence de base de données de bureau Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291413"
---
# <a name="inherittypeenum"></a><span data-ttu-id="c4136-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="c4136-102">InheritTypeEnum</span></span>

<span data-ttu-id="c4136-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4136-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4136-104">Indique comment les objets hériteront des autorisations définies à l’aide de la méthode [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="c4136-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4136-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c4136-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c4136-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4136-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c4136-107">Description</span><span class="sxs-lookup"><span data-stu-id="c4136-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4136-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="c4136-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="c4136-109">3</span><span class="sxs-lookup"><span data-stu-id="c4136-109">3</span></span></p></td>
<td><p><span data-ttu-id="c4136-110">Les objets et autres conteneurs de l'objet principal héritent de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="c4136-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4136-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="c4136-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="c4136-112">n°2</span><span class="sxs-lookup"><span data-stu-id="c4136-112">2</span></span></p></td>
<td><p><span data-ttu-id="c4136-113">D'autres conteneurs contenus dans l'objet principal héritent de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="c4136-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4136-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="c4136-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="c4136-115">0</span><span class="sxs-lookup"><span data-stu-id="c4136-115">0</span></span></p></td>
<td><p><span data-ttu-id="c4136-p101">Valeur par défaut. Aucun héritage ne se produit.</span><span class="sxs-lookup"><span data-stu-id="c4136-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4136-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="c4136-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="c4136-119">4</span><span class="sxs-lookup"><span data-stu-id="c4136-119">4</span></span></p></td>
<td><p><span data-ttu-id="c4136-120">Les indicateurs <strong>adInheritObjects</strong> et <strong>adInheritContainers</strong> ne sont pas transmis à une entrée héritée.</span><span class="sxs-lookup"><span data-stu-id="c4136-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4136-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="c4136-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="c4136-122">0,1</span><span class="sxs-lookup"><span data-stu-id="c4136-122">1</span></span></p></td>
<td><p><span data-ttu-id="c4136-123">Les objets du conteneur qui ne sont pas du type conteneur héritent des autorisations.</span><span class="sxs-lookup"><span data-stu-id="c4136-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

