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
ms.openlocfilehash: 1a11544808cfb897a359a5e170332ba23e25ceae
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888040"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="bbb21-102">Field.SourceTable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="bbb21-102">Field.SourceTable Property (DAO)</span></span>


<span data-ttu-id="bbb21-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbb21-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbb21-p101">Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet **Field**. Données de type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bbb21-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb21-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbb21-106">Syntax</span></span>

<span data-ttu-id="bbb21-107">*expression* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="bbb21-107">*expression* .SourceTable</span></span>

<span data-ttu-id="bbb21-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="bbb21-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbb21-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="bbb21-109">Remarks</span></span>

<span data-ttu-id="bbb21-110">Pour un objet **Field**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bbb21-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbb21-111">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="bbb21-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="bbb21-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="bbb21-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbb21-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="bbb21-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="bbb21-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbb21-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbb21-115"><strong>Objet QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="bbb21-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="bbb21-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbb21-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbb21-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="bbb21-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="bbb21-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbb21-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbb21-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="bbb21-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="bbb21-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbb21-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbb21-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="bbb21-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="bbb21-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bbb21-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bbb21-p102">Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="bbb21-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bbb21-125">[!REMARQUE] La propriété <STRONG>SourceTable</STRONG> ne renvoie aucun nom de table significatif lorsqu'elle est utilisée sur un objet <STRONG>Field</STRONG> de la collection <STRONG>Fields</STRONG> d'un objet <STRONG>Recordset</STRONG> de type table.</span><span class="sxs-lookup"><span data-stu-id="bbb21-125">The <STRONG>SourceTable</STRONG> property will not return a meaningful table name if used on a <STRONG>Field</STRONG> object in the <STRONG>Fields</STRONG> collection of a table-type <STRONG>Recordset</STRONG> object.</span></span></P>


