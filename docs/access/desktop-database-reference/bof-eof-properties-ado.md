---
title: BOF, EOF, propriétés (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d36a65ce8a6808f2128749bd7fbc6e468acbd279
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726126"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="36a18-102">BOF, EOF, propriétés (ADO)</span><span class="sxs-lookup"><span data-stu-id="36a18-102">BOF, EOF properties (ADO)</span></span>


<span data-ttu-id="36a18-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="36a18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36a18-104">**BOF**  Indique que la position d'enregistrement actuelle se trouve avant le premier enregistrement d'un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="36a18-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="36a18-105">**EOF**  Indique que la position d'enregistrement actuelle se trouve après le dernier enregistrement d'un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="36a18-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="36a18-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="36a18-106">Return value</span></span>

<span data-ttu-id="36a18-107">Les propriétés **BOF** et **EOF** retournent des valeurs de type **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="36a18-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="36a18-108">Notes</span><span class="sxs-lookup"><span data-stu-id="36a18-108">Remarks</span></span>

<span data-ttu-id="36a18-109">Utilisez les propriétés **BOF** et **EOF** pour déterminer si un objet **Recordset** contient des enregistrements ou si vous avez dépassé les limites d'un objet **Recordset** lorsque vous vous déplacez d'un enregistrement à l'autre.</span><span class="sxs-lookup"><span data-stu-id="36a18-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="36a18-110">La propriété **BOF** retourne la valeur **True** (-1) si la position d'enregistrement actuelle se trouve avant le premier enregistrement et la valeur **False** (0) si la position d'enregistrement actuelle se trouve au niveau du premier enregistrement ou après celui-ci.</span><span class="sxs-lookup"><span data-stu-id="36a18-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="36a18-111">La propriété **EOF** renvoie la valeur **True** si la position d'enregistrement actuelle se trouve après le dernier enregistrement et la valeur **False** si la position d'enregistrement actuelle se trouve au niveau du dernier enregistrement ou avant celui-ci.</span><span class="sxs-lookup"><span data-stu-id="36a18-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="36a18-112">Si l'une des propriétés **BOF** ou **EOF** a la valeur **True**, il n'y a pas d'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="36a18-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="36a18-p101">Si vous ouvrez un objet **Recordset** qui ne contient pas d’enregistrement, les propriétés **BOF** et **EOF** ont la valeur **True** (reportez-vous à la propriété [RecordCount](recordcount-property-ado.md) pour plus d’informations sur cet état d’un objet **Recordset**). Lorsque vous ouvrez un objet **Recordset** qui contient au moins un enregistrement, le premier enregistrement correspond au dernier enregistrement et les propriétés **BOF** et **EOF** ont la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="36a18-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="36a18-115">Si vous supprimez le dernier enregistrement encore présent dans l'objet **Recordset**, les propriétés **BOF** et **EOF** peuvent conserver la valeur **False** jusqu'à ce que vous tentiez de repositionner l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="36a18-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="36a18-116">Ce tableau répertorie les méthodes **Move** autorisées avec les différentes combinaisons des propriétés **BOF** et **EOF**.</span><span class="sxs-lookup"><span data-stu-id="36a18-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="36a18-117">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="36a18-117">MoveFirst,</span></span><br />
<span data-ttu-id="36a18-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="36a18-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="36a18-119">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="36a18-119">MovePrevious,</span></span><br />
<span data-ttu-id="36a18-120">Déplacer &lt; 0</span><span class="sxs-lookup"><span data-stu-id="36a18-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="36a18-121">Move 0</span><span class="sxs-lookup"><span data-stu-id="36a18-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="36a18-122">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="36a18-122">MoveNext,</span></span><br />
<span data-ttu-id="36a18-123">Déplacer &gt; 0</span><span class="sxs-lookup"><span data-stu-id="36a18-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36a18-124"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="36a18-125">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="36a18-126">Autorisé</span><span class="sxs-lookup"><span data-stu-id="36a18-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="36a18-127">Erreur</span><span class="sxs-lookup"><span data-stu-id="36a18-127">Error</span></span></p></td>
<td><p><span data-ttu-id="36a18-128">Erreur</span><span class="sxs-lookup"><span data-stu-id="36a18-128">Error</span></span></p></td>
<td><p><span data-ttu-id="36a18-129">Autorisé</span><span class="sxs-lookup"><span data-stu-id="36a18-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36a18-130"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="36a18-131">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="36a18-132">Autorisé</span><span class="sxs-lookup"><span data-stu-id="36a18-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="36a18-133">Autorisé</span><span class="sxs-lookup"><span data-stu-id="36a18-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="36a18-134">Erreur</span><span class="sxs-lookup"><span data-stu-id="36a18-134">Error</span></span></p></td>
<td><p><span data-ttu-id="36a18-135">Erreur</span><span class="sxs-lookup"><span data-stu-id="36a18-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36a18-136">Les deux propriétés ont la valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="36a18-137">Erreur</span><span class="sxs-lookup"><span data-stu-id="36a18-137">Error</span></span></p></td>
<td><p><span data-ttu-id="36a18-138">Erreur</span><span class="sxs-lookup"><span data-stu-id="36a18-138">Error</span></span></p></td>
<td><p><span data-ttu-id="36a18-139">Erreur</span><span class="sxs-lookup"><span data-stu-id="36a18-139">Error</span></span></p></td>
<td><p><span data-ttu-id="36a18-140">Erreur</span><span class="sxs-lookup"><span data-stu-id="36a18-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36a18-141">Les deux propriétés ont la valeur <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="36a18-142">Autorisé</span><span class="sxs-lookup"><span data-stu-id="36a18-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="36a18-143">Autorisé</span><span class="sxs-lookup"><span data-stu-id="36a18-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="36a18-144">Autorisé</span><span class="sxs-lookup"><span data-stu-id="36a18-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="36a18-145">Autorisé</span><span class="sxs-lookup"><span data-stu-id="36a18-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="36a18-146">Même si une méthode **Move** est autorisée, rien ne garantit que la méthode parviendra à localiser un enregistrement. Cela signifie uniquement que l'appel de la méthode **Move** spécifiée ne génère pas d'erreur.</span><span class="sxs-lookup"><span data-stu-id="36a18-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="36a18-147">Le tableau ci-dessous répertorie les valeurs prises par les propriétés **BOF** et **EOF** lorsque vous appelez différentes méthodes **Move** et que vous ne parvenez pas à trouver un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="36a18-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="36a18-148">BOF</span><span class="sxs-lookup"><span data-stu-id="36a18-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="36a18-149">EOF</span><span class="sxs-lookup"><span data-stu-id="36a18-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36a18-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="36a18-151">La valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="36a18-152">La valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36a18-153"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="36a18-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="36a18-154">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="36a18-154">No change</span></span></p></td>
<td><p><span data-ttu-id="36a18-155">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="36a18-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36a18-156"><strong>MovePrevious</strong>, <strong>déplacer</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="36a18-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="36a18-157">Prend la valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="36a18-158">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="36a18-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36a18-159"><strong>MoveNext</strong>, <strong>déplacer</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="36a18-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="36a18-160">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="36a18-160">No change</span></span></p></td>
<td><p><span data-ttu-id="36a18-161">Prend la valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="36a18-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

