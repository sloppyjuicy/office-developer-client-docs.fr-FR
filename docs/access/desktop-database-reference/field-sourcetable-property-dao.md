---
title: Propriété Field.SourceTable (DAO)
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
localization_priority: Normal
ms.openlocfilehash: a557a4941f5b4aa511489c5d057871df5fa72c08
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726063"
---
# <a name="fieldsourcetable-property-dao"></a><span data-ttu-id="44738-102">Propriété Field.SourceTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="44738-102">Field.SourceTable property (DAO)</span></span>


<span data-ttu-id="44738-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44738-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44738-p101">Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet **Field**. Données de type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="44738-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="44738-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44738-106">Syntax</span></span>

<span data-ttu-id="44738-107">*expression* . SourceTable</span><span class="sxs-lookup"><span data-stu-id="44738-107">*expression* .SourceTable</span></span>

<span data-ttu-id="44738-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="44738-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44738-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="44738-109">Remarks</span></span>

<span data-ttu-id="44738-110">Pour un objet **Field**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="44738-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44738-111">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="44738-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="44738-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="44738-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44738-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="44738-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="44738-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="44738-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44738-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="44738-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="44738-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44738-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44738-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="44738-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="44738-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44738-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44738-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="44738-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="44738-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="44738-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44738-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="44738-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="44738-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44738-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="44738-p102">Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="44738-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="44738-125">[!REMARQUE] La propriété **SourceTable** ne renvoie aucun nom de table significatif lorsqu'elle est utilisée sur un objet **Field** de la collection **Fields** d'un objet **Recordset** de type table.</span><span class="sxs-lookup"><span data-stu-id="44738-125">The **SourceTable** property will not return a meaningful table name if used on a **Field** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


