---
title: Index.Required Property (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 71ea383cbf1c55fb15b484fea039c71c44a4e470
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881411"
---
# <a name="indexrequired-property-dao"></a><span data-ttu-id="beabe-102">Index.Required Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="beabe-102">Index.Required Property (DAO)</span></span>


<span data-ttu-id="beabe-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="beabe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="beabe-104">Définit ou renvoie une valeur qui indique si un objet **[Field](field-object-dao.md)** requiert une valeur non Null.</span><span class="sxs-lookup"><span data-stu-id="beabe-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="beabe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="beabe-105">Syntax</span></span>

<span data-ttu-id="beabe-106">*expression* . Obligatoire</span><span class="sxs-lookup"><span data-stu-id="beabe-106">*expression* .Required</span></span>

<span data-ttu-id="beabe-107">*expression* Variable qui représente un objet **Index** .</span><span class="sxs-lookup"><span data-stu-id="beabe-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="beabe-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="beabe-108">Remarks</span></span>


> [!NOTE]
> <P><span data-ttu-id="beabe-p101">[!REMARQUE] Lorsque vous définissez cette propriété pour un objet <STRONG>Index</STRONG> ou <STRONG>Field</STRONG>, définissez-la pour l'objet <STRONG>Field</STRONG>. La validité du paramètre de propriété d'un objet <STRONG>Field</STRONG> est vérifiée avant celle d'un objet <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="beabe-p101">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



<span data-ttu-id="beabe-111">La disponibilité de la propriété **Required** dépend de l'objet contenant la collection [Fields](fields-collection-dao.md), comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="beabe-111">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="beabe-112">Si la collection Fields appartient à un</span><span class="sxs-lookup"><span data-stu-id="beabe-112">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="beabe-113">Alors Required est</span><span class="sxs-lookup"><span data-stu-id="beabe-113">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="beabe-114">							objet <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="beabe-114"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="beabe-115">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="beabe-115">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beabe-116">							objet <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="beabe-116"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="beabe-117">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="beabe-117">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beabe-118">							objet <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="beabe-118"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="beabe-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="beabe-119">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beabe-120">							objet <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="beabe-120"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="beabe-121">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="beabe-121">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beabe-122">							objet <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="beabe-122"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="beabe-123">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="beabe-123">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

