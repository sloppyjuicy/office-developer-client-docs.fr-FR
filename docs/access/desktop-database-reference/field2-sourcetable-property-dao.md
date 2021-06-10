---
title: Field2.SourceTable, propriété (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a3ecf8b6655bb9f1dd2b25d264708112834e8a90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292670"
---
# <a name="field2sourcetable-property-dao"></a><span data-ttu-id="70aee-102">Field2.SourceTable, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="70aee-102">Field2.SourceTable property (DAO)</span></span>


<span data-ttu-id="70aee-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70aee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70aee-p101">Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet **Field2**. Données de type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="70aee-p101">Returns a value that indicates the name of the table that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="70aee-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70aee-106">Syntax</span></span>

<span data-ttu-id="70aee-107">*.* SourceTable</span><span class="sxs-lookup"><span data-stu-id="70aee-107">*expression* .SourceTable</span></span>

<span data-ttu-id="70aee-108">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="70aee-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="70aee-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="70aee-109">Remarks</span></span>

<span data-ttu-id="70aee-110">Pour un objet **Field2**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field2** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="70aee-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70aee-111">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="70aee-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="70aee-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="70aee-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70aee-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="70aee-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="70aee-114">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="70aee-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70aee-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="70aee-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="70aee-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70aee-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70aee-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="70aee-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="70aee-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70aee-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70aee-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="70aee-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="70aee-120">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="70aee-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70aee-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="70aee-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="70aee-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70aee-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70aee-p102">Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field2**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="70aee-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>


> [!NOTE]
> <span data-ttu-id="70aee-125">[!REMARQUE] La propriété **SourceTable** ne renvoie aucun nom de table significatif lorsqu'elle est utilisée sur un objet **Field2** de la collection **Fields** d'un objet **Recordset** de type table.</span><span class="sxs-lookup"><span data-stu-id="70aee-125">The **SourceTable** property will not return a meaningful table name if used on a **Field2** object in the **Fields** collection of a table-type **Recordset** object.</span></span>


