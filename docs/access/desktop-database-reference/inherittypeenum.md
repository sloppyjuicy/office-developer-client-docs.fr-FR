---
title: InheritTypeEnum (référence de base de données du bureau Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 031c47aff666bf10f0e2aa597ccd0143ed3d6209
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469605"
---
# <a name="inherittypeenum"></a><span data-ttu-id="a6eb7-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="a6eb7-102">InheritTypeEnum</span></span>


<span data-ttu-id="a6eb7-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a6eb7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a6eb7-104">Indique comment les objets hériteront des autorisations définies à l'aide de la méthode [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="a6eb7-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6eb7-105">Constant</span><span class="sxs-lookup"><span data-stu-id="a6eb7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a6eb7-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6eb7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a6eb7-107">Description</span><span class="sxs-lookup"><span data-stu-id="a6eb7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6eb7-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="a6eb7-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="a6eb7-109">3</span><span class="sxs-lookup"><span data-stu-id="a6eb7-109">3</span></span></p></td>
<td><p><span data-ttu-id="a6eb7-110">Les objets et autres conteneurs de l'objet principal héritent de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="a6eb7-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6eb7-111"><strong>adInheritContainers ne</strong></span><span class="sxs-lookup"><span data-stu-id="a6eb7-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="a6eb7-112">2</span><span class="sxs-lookup"><span data-stu-id="a6eb7-112">2</span></span></p></td>
<td><p><span data-ttu-id="a6eb7-113">D'autres conteneurs contenus dans l'objet principal héritent de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="a6eb7-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6eb7-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="a6eb7-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="a6eb7-115">0</span><span class="sxs-lookup"><span data-stu-id="a6eb7-115">0</span></span></p></td>
<td><p><span data-ttu-id="a6eb7-p101">Valeur par défaut. Aucun héritage ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a6eb7-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6eb7-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="a6eb7-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="a6eb7-119">4</span><span class="sxs-lookup"><span data-stu-id="a6eb7-119">4</span></span></p></td>
<td><p><span data-ttu-id="a6eb7-120">Les indicateurs <strong>adInheritObjects</strong> et <strong>adInheritContainers</strong> ne sont pas transmis à une entrée héritée.</span><span class="sxs-lookup"><span data-stu-id="a6eb7-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6eb7-121"><strong>indicateurs adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="a6eb7-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="a6eb7-122">1</span><span class="sxs-lookup"><span data-stu-id="a6eb7-122">1</span></span></p></td>
<td><p><span data-ttu-id="a6eb7-123">Les objets du conteneur qui ne sont pas du type conteneur héritent des autorisations.</span><span class="sxs-lookup"><span data-stu-id="a6eb7-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

