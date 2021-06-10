---
title: Field.SourceField, propriété (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dabfa13bac6973cea4bd69e0867292c4a6967
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292992"
---
# <a name="fieldsourcefield-property-dao"></a><span data-ttu-id="996bc-102">Field.SourceField, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="996bc-102">Field.SourceField property (DAO)</span></span>


<span data-ttu-id="996bc-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="996bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="996bc-p101">Renvoie une valeur spécifiant le nom du champ qui représente la source d'origine des données d'un objet **Field**. Type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="996bc-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="996bc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="996bc-106">Syntax</span></span>

<span data-ttu-id="996bc-107">*.* SourceField</span><span class="sxs-lookup"><span data-stu-id="996bc-107">*expression* .SourceField</span></span>

<span data-ttu-id="996bc-108">*expression* Variable qui représente un objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="996bc-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="996bc-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="996bc-109">Remarks</span></span>

<span data-ttu-id="996bc-110">Pour un objet **Field**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="996bc-110">For a **Field** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="996bc-111">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="996bc-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="996bc-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="996bc-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="996bc-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="996bc-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="996bc-114">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="996bc-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996bc-115"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="996bc-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="996bc-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="996bc-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996bc-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="996bc-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="996bc-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="996bc-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="996bc-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="996bc-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="996bc-120">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="996bc-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="996bc-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="996bc-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="996bc-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="996bc-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="996bc-p102">Ces propriétés indiquent les noms des tables et des champs d'origine associés à un objet **Field**. Vous pouvez, par exemple, utiliser ces propriétés pour déterminer la source d'origine des données dans un champ de requête dont le nom n'a aucun rapport avec le nom du champ dans la table sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="996bc-p102">These properties indicate the original field and table names associated with a **Field** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

