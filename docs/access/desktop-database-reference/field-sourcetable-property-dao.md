---
title: Field.SourceTable Property (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b29437a459d29e5238e8bd915901339d87005612
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472327"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="72ea3-102">Field.SourceTable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="72ea3-102">Field.SourceTable Property (DAO)</span></span>


<span data-ttu-id="72ea3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="72ea3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72ea3-p101">Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet **Field**. Données de type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="72ea3-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ea3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72ea3-106">Syntax</span></span>

<span data-ttu-id="72ea3-107">*expression* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="72ea3-107">*expression* .SourceTable</span></span>

<span data-ttu-id="72ea3-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="72ea3-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="72ea3-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="72ea3-109">Remarks</span></span>

<span data-ttu-id="72ea3-110">Pour un objet **Field**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="72ea3-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72ea3-111">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="72ea3-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="72ea3-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="72ea3-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72ea3-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="72ea3-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="72ea3-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="72ea3-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72ea3-115"><strong>Objet QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="72ea3-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="72ea3-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72ea3-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72ea3-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="72ea3-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="72ea3-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72ea3-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72ea3-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="72ea3-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="72ea3-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="72ea3-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72ea3-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="72ea3-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="72ea3-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="72ea3-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72ea3-p102">Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="72ea3-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="72ea3-125">[!REMARQUE] La propriété <STRONG>SourceTable</STRONG> ne renvoie aucun nom de table significatif lorsqu'elle est utilisée sur un objet <STRONG>Field</STRONG> de la collection <STRONG>Fields</STRONG> d'un objet <STRONG>Recordset</STRONG> de type table.</span><span class="sxs-lookup"><span data-stu-id="72ea3-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


