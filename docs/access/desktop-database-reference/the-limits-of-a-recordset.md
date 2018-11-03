---
title: Limites d'un jeu d'enregistrements
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c5b0f03e135f4e00b3ca9d6be7417bfe0e5047e6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946579"
---
# <a name="limits-of-a-recordset"></a><span data-ttu-id="d8413-102">Limites d'un recordset</span><span class="sxs-lookup"><span data-stu-id="d8413-102">Limits of a Recordset</span></span>


<span data-ttu-id="d8413-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8413-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8413-p101">Utilisez les propriétés **BOF** et **EOF** pour déterminer si un objet **Recordset** contient des enregistrements ou si vous avez dépassé les limites d'un objet **Recordset** en vous déplaçant d'un enregistrement à l'autre. Considérez les propriétés **BOF** et **EOF** comme des enregistrements « fantômes » placés au début et à la fin de l'objet **Recordset**. En se basant sur l'exemple d'objet **Recordset** présenté dans [Examen des données](chapter-3-examining-data.md), on obtient les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="d8413-p101">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record. Think of **BOF** and **EOF** as "phantom" records that are positioned at the beginning and end of the **Recordset**. Building on the sample **Recordset** from [Examining Data](chapter-3-examining-data.md), it would now look like this:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8413-107">ProductID</span><span class="sxs-lookup"><span data-stu-id="d8413-107">ProductID</span></span></p></th>
<th><p><span data-ttu-id="d8413-108">ProductName</span><span class="sxs-lookup"><span data-stu-id="d8413-108">ProductName</span></span></p></th>
<th><p><span data-ttu-id="d8413-109">UnitPrice</span><span class="sxs-lookup"><span data-stu-id="d8413-109">UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8413-110">BOF</span><span class="sxs-lookup"><span data-stu-id="d8413-110">BOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8413-111">7</span><span class="sxs-lookup"><span data-stu-id="d8413-111">7</span></span></p></td>
<td><p><span data-ttu-id="d8413-112">Pêches séchées bio Oncle Bob</span><span class="sxs-lookup"><span data-stu-id="d8413-112">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="d8413-113">30.0000</span><span class="sxs-lookup"><span data-stu-id="d8413-113">30.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8413-114">14</span><span class="sxs-lookup"><span data-stu-id="d8413-114">14</span></span></p></td>
<td><p><span data-ttu-id="d8413-115">Tofu</span><span class="sxs-lookup"><span data-stu-id="d8413-115">Tofu</span></span></p></td>
<td><p><span data-ttu-id="d8413-116">23.2500</span><span class="sxs-lookup"><span data-stu-id="d8413-116">23.2500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8413-117">28</span><span class="sxs-lookup"><span data-stu-id="d8413-117">28</span></span></p></td>
<td><p><span data-ttu-id="d8413-118">Choucroute Frau Kraut</span><span class="sxs-lookup"><span data-stu-id="d8413-118">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="d8413-119">45.6000</span><span class="sxs-lookup"><span data-stu-id="d8413-119">45.6000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8413-120">51</span><span class="sxs-lookup"><span data-stu-id="d8413-120">51</span></span></p></td>
<td><p><span data-ttu-id="d8413-121">Pommes séchées Manjimup</span><span class="sxs-lookup"><span data-stu-id="d8413-121">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="d8413-122">53.0000</span><span class="sxs-lookup"><span data-stu-id="d8413-122">53.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8413-123">74</span><span class="sxs-lookup"><span data-stu-id="d8413-123">74</span></span></p></td>
<td><p><span data-ttu-id="d8413-124">Tofu LongVi</span><span class="sxs-lookup"><span data-stu-id="d8413-124">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="d8413-125">10.0000</span><span class="sxs-lookup"><span data-stu-id="d8413-125">10.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8413-126">EOF</span><span class="sxs-lookup"><span data-stu-id="d8413-126">EOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8413-127">La propriété **BOF** retourne la valeur **True** (-1) si la position d'enregistrement actif est située avant le premier enregistrement et la valeur **False** (0) si la position d'enregistrement actif est située au niveau du premier enregistrement ou après celui-ci.</span><span class="sxs-lookup"><span data-stu-id="d8413-127">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="d8413-128">La propriété **EOF** renvoie la valeur **True** si la position d'enregistrement actif est située après le dernier enregistrement et la valeur **False** si la position d'enregistrement actif est située au niveau du dernier enregistrement ou avant celui-ci.</span><span class="sxs-lookup"><span data-stu-id="d8413-128">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="d8413-129">Si la propriété **BOF** ou **EOF** a la valeur **True**, cela signifie qu'il n'y a aucun enregistrement actif, comme l'illustre le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d8413-129">If either the **BOF** or **EOF** property is **True**, there is no current record, as shown in the following code:</span></span>

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

<span data-ttu-id="d8413-130">Si vous ouvrez un objet **Recordset** ne contenant aucun enregistrement, les propriétés **BOF** et **EOF** ont toutes deux la valeur **True** et la valeur définie pour la propriété **RecordCount** de l'objet **Recordset** dépend du type de curseur.</span><span class="sxs-lookup"><span data-stu-id="d8413-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span></span> <span data-ttu-id="d8413-131">-1 est retournée pour des curseurs dynamiques (**CursorType** = **adOpenDynamic**) et 0 est retourné pour les autres curseurs.</span><span class="sxs-lookup"><span data-stu-id="d8413-131">-1 will be returned for dynamic cursors (**CursorType** = **adOpenDynamic**) and 0 will be returned for other cursors.</span></span>

<span data-ttu-id="d8413-132">Lorsque vous ouvrez un objet **Recordset** qui contient au moins un enregistrement, le premier enregistrement est l'enregistrement actif. Les propriétés **BOF** et **EOF** ont, dans ce cas, la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="d8413-132">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="d8413-p103">Si vous supprimez le dernier enregistrement restant de l'objet **Recordset**, le curseur reste dans un état indéterminé. Selon le fournisseur, les propriétés **BOF** et **EOF** peuvent conserver la valeur **False** jusqu'à ce que vous tentiez de repositionner l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="d8413-p103">If you delete the last remaining record in the **Recordset** object, the cursor is left in an indeterminate state. The **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record, depending upon the provider.</span></span>

