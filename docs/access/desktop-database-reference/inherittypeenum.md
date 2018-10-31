---
title: InheritTypeEnum (référence de base de données du bureau Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: bf7d7ceac1e4822344ce4f7ad8a05e09c0429dff
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860566"
---
# <a name="inherittypeenum"></a><span data-ttu-id="360aa-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="360aa-102">InheritTypeEnum</span></span>

<span data-ttu-id="360aa-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="360aa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="360aa-104">Indique comment les objets hériteront des autorisations définies à l'aide de la méthode [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="360aa-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="360aa-105">Constant</span><span class="sxs-lookup"><span data-stu-id="360aa-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="360aa-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="360aa-106">Value</span></span></p></th>
<th><p><span data-ttu-id="360aa-107">Description</span><span class="sxs-lookup"><span data-stu-id="360aa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="360aa-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="360aa-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="360aa-109">3</span><span class="sxs-lookup"><span data-stu-id="360aa-109">3</span></span></p></td>
<td><p><span data-ttu-id="360aa-110">Les objets et autres conteneurs de l'objet principal héritent de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="360aa-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="360aa-111"><strong>adInheritContainers ne</strong></span><span class="sxs-lookup"><span data-stu-id="360aa-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="360aa-112">2</span><span class="sxs-lookup"><span data-stu-id="360aa-112">2</span></span></p></td>
<td><p><span data-ttu-id="360aa-113">D'autres conteneurs contenus dans l'objet principal héritent de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="360aa-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="360aa-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="360aa-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="360aa-115">0</span><span class="sxs-lookup"><span data-stu-id="360aa-115">0</span></span></p></td>
<td><p><span data-ttu-id="360aa-p101">Valeur par défaut. Aucun héritage ne se produit.</span><span class="sxs-lookup"><span data-stu-id="360aa-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="360aa-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="360aa-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="360aa-119">4</span><span class="sxs-lookup"><span data-stu-id="360aa-119">4</span></span></p></td>
<td><p><span data-ttu-id="360aa-120">Les indicateurs <strong>adInheritObjects</strong> et <strong>adInheritContainers</strong> ne sont pas transmis à une entrée héritée.</span><span class="sxs-lookup"><span data-stu-id="360aa-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="360aa-121"><strong>indicateurs adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="360aa-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="360aa-122">1</span><span class="sxs-lookup"><span data-stu-id="360aa-122">1</span></span></p></td>
<td><p><span data-ttu-id="360aa-123">Les objets du conteneur qui ne sont pas du type conteneur héritent des autorisations.</span><span class="sxs-lookup"><span data-stu-id="360aa-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

