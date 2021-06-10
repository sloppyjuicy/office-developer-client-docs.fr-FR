---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300692"
---
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="64c29-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="64c29-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="64c29-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64c29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64c29-p101">Spécifie si un **Record** doit être ouvert ou si un nouveau **Record** doit être créé pour la méthode [Open](record-object-ado.md) de l'objet [Record](open-method-ado-record.md) . Les valeurs peuvent être combinées avec un opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="64c29-p101">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method. The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64c29-106">Constante</span><span class="sxs-lookup"><span data-stu-id="64c29-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="64c29-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="64c29-107">Value</span></span></p></th>
<th><p><span data-ttu-id="64c29-108">Description</span><span class="sxs-lookup"><span data-stu-id="64c29-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64c29-109"><strong>adCreateCollection</strong></span><span class="sxs-lookup"><span data-stu-id="64c29-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="64c29-110">0x2000</span><span class="sxs-lookup"><span data-stu-id="64c29-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="64c29-p102">Crée un nouveau <strong>Record</strong> sur le nœud spécifié par le paramètre <em>Source</em>, au lieu d'ouvrir un <strong>Record</strong> existant. Si la source pointe sur un nœud existant, une erreur d'exécution se produit, à moins que <strong>adCreateCollection</strong> ne soit combiné avec <strong>adOpenIfExists</strong> ou <strong>adCreateOverwrite</strong>.</span><span class="sxs-lookup"><span data-stu-id="64c29-p102">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>. If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64c29-113"><strong>adCreateNonCollection</strong></span><span class="sxs-lookup"><span data-stu-id="64c29-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="64c29-114">0</span><span class="sxs-lookup"><span data-stu-id="64c29-114">0</span></span></p></td>
<td><p><span data-ttu-id="64c29-115">Crée un nouveau <strong>Record</strong> de type <a href="recordtypeenum.md">adSimpleRecord</a>.</span><span class="sxs-lookup"><span data-stu-id="64c29-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64c29-116"><strong>adCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="64c29-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="64c29-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="64c29-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="64c29-p103">Modifie les indicateurs de création <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> et <strong>adCreateStructDoc</strong>. Quand OR est utilisé avec cette valeur et l'une des valeurs d'indicateur de création, et si l'URL source pointe sur un nœud ou un <strong>Record</strong> existant, le <strong>Record</strong> est remplacé par un nouveau. Cette valeur ne peut être utilisée avec <strong>adOpenIfExists</strong>.</span><span class="sxs-lookup"><span data-stu-id="64c29-p103">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>. When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place. This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64c29-121"><strong>adCreateStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="64c29-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="64c29-122">0x80000000</span><span class="sxs-lookup"><span data-stu-id="64c29-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="64c29-123">Crée un nouveau <strong>Record</strong> de type <a href="recordtypeenum.md">adStructDoc</a>, au lieu d’ouvrir un <strong>Record</strong> existant.</span><span class="sxs-lookup"><span data-stu-id="64c29-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64c29-124"><strong>adFailIfNotExists</strong></span><span class="sxs-lookup"><span data-stu-id="64c29-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="64c29-125">-1</span><span class="sxs-lookup"><span data-stu-id="64c29-125">-1</span></span></p></td>
<td><p><span data-ttu-id="64c29-p104">Par défaut. Provoque une erreur d'exécution si <em>Source</em> pointe sur un nœud inexistant.</span><span class="sxs-lookup"><span data-stu-id="64c29-p104">Default. Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64c29-128"><strong>adOpenIfExists</strong></span><span class="sxs-lookup"><span data-stu-id="64c29-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="64c29-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="64c29-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="64c29-p105">Modifie les indicateurs de création <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> et <strong>adCreateStructDoc</strong>. Quand OR est utilisé avec cette valeur et l’une des valeurs d’indicateur de création, et si l’URL source pointe sur un nœud existant ou sur un objet <strong>Record</strong>, le fournisseur doit ouvrir le <strong>Record</strong> existant au lieu d’en créer un nouveau. Cette valeur ne peut pas être utilisée avec <strong>adCreateOverwrite</strong>.</span><span class="sxs-lookup"><span data-stu-id="64c29-p105">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>. When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one. This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="64c29-133">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="64c29-133">ADO/WFC equivalent</span></span>

<span data-ttu-id="64c29-134">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="64c29-134">These constants do not have ADO/WFC equivalents.</span></span>

