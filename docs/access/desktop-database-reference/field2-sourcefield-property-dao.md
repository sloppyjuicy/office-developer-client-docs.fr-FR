---
title: Field2.SourceField Property (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09351acfea263c41bd9cb7f857139dfacf359421
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470735"
---
# <a name="field2sourcefield-property-dao"></a><span data-ttu-id="b827f-102">Field2.SourceField Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="b827f-102">Field2.SourceField Property (DAO)</span></span>


<span data-ttu-id="b827f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b827f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b827f-p101">Renvoie une valeur indiquant le nom du champ duquel provient les données d'un objet **Field2**. Données de type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b827f-p101">Returns a value that indicates the name of the field that is the original source of the data for a **Field2** object. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b827f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b827f-106">Syntax</span></span>

<span data-ttu-id="b827f-107">*expression* . SourceField</span><span class="sxs-lookup"><span data-stu-id="b827f-107">*expression* .SourceField</span></span>

<span data-ttu-id="b827f-108">*expression* Variable qui représente un objet **Field2** .</span><span class="sxs-lookup"><span data-stu-id="b827f-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b827f-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="b827f-109">Remarks</span></span>

<span data-ttu-id="b827f-110">Pour un objet **Field2**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field2** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b827f-110">For a **Field2** object, use of the **SourceField** and **SourceTable** properties depends on the object that contains the **Fields** collection that the **Field2** object is appended to, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b827f-111">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="b827f-111">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="b827f-112">Utilisation</span><span class="sxs-lookup"><span data-stu-id="b827f-112">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b827f-113"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="b827f-113"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="b827f-114">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="b827f-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b827f-115"><strong>Objet QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="b827f-115"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="b827f-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b827f-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b827f-117"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="b827f-117"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="b827f-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b827f-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b827f-119"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="b827f-119"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="b827f-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="b827f-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b827f-121"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="b827f-121"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="b827f-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b827f-122">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b827f-p102">Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field2**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="b827f-p102">These properties indicate the original field and table names associated with a **Field2** object. For example, you could use these properties to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table.</span></span>

