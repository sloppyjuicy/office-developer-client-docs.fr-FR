---
title: Propriété Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fbde7aa9785e4e875f96569884e7f6e45743f2bb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925582"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="cbac4-102">Propriété Field2.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="cbac4-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="cbac4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbac4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbac4-p101">Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet **Field2**. Données de type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cbac4-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbac4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbac4-106">Syntax</span></span>

<span data-ttu-id="cbac4-107">*expression* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="cbac4-107">*expression* .SourceTable</span></span>

<span data-ttu-id="cbac4-108">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="cbac4-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbac4-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="cbac4-109">Remarks</span></span>

<span data-ttu-id="cbac4-110">Pour un objet **Field2**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field2** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cbac4-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbac4-111">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="cbac4-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="cbac4-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="cbac4-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbac4-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="cbac4-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="cbac4-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbac4-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbac4-115"><strong>Objet QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="cbac4-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="cbac4-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbac4-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbac4-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="cbac4-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="cbac4-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbac4-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbac4-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="cbac4-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="cbac4-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbac4-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cbac4-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="cbac4-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="cbac4-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbac4-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cbac4-p102">Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field2**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="cbac4-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cbac4-125">[!REMARQUE] La propriété <STRONG>SourceTable</STRONG> ne renvoie aucun nom de table significatif lorsqu'elle est utilisée sur un objet <STRONG>Field2</STRONG> de la collection <STRONG>Fields</STRONG> d'un objet <STRONG>Recordset</STRONG> de type table.</span><span class="sxs-lookup"><span data-stu-id="cbac4-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field2</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


