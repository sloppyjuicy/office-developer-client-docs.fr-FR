---
title: Propriété Recordset.BOF (DAO)
TOCTitle: BOF Property
ms:assetid: c50a0c5f-1b26-33ea-4cf2-311f9514a94a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823092(v=office.15)
ms:contentKeyID: 48547603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: babd2351775a9a3cf3128a55627be291a29ea025
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699673"
---
# <a name="recordsetbof-property-dao"></a><span data-ttu-id="be8c9-102">Propriété Recordset.BOF (DAO)</span><span class="sxs-lookup"><span data-stu-id="be8c9-102">Recordset.BOF property (DAO)</span></span>


<span data-ttu-id="be8c9-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be8c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be8c9-p101">Renvoie une valeur qui indique si la position de l'enregistrement actif est située avant le premier enregistrement dans un objet **Recordset**. Valeur de type **Boolean** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="be8c9-p101">Returns a value that indicates whether the current record position is before the first record in a **Recordset** object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8c9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be8c9-106">Syntax</span></span>

<span data-ttu-id="be8c9-107">*expression* . BOF</span><span class="sxs-lookup"><span data-stu-id="be8c9-107">*expression* .BOF</span></span>

<span data-ttu-id="be8c9-108">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="be8c9-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="be8c9-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="be8c9-109">Remarks</span></span>

<span data-ttu-id="be8c9-110">Vous pouvez utiliser les propriétés **BOF** et **EOF** pour déterminer si un objet **Recordset** contient des enregistrements ou si vous avez dépassé les limites de l'objet **Recordset** en vous déplaçant d'un enregistrement à l'autre.</span><span class="sxs-lookup"><span data-stu-id="be8c9-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="be8c9-111">L'emplacement du pointeur d'enregistrement actif détermine les valeurs renvoyées par **BOF** et **EOF**.</span><span class="sxs-lookup"><span data-stu-id="be8c9-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="be8c9-112">Si la propriété **BOF** ou **EOF** a la valeur **True**, il n'existe aucun enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="be8c9-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="be8c9-p102">Si vous ouvrez un objet **Recordset** qui ne contient aucun enregistrement, les propriétés **BOF** et **EOF** ont la valeur **True** et le paramètre de la propriété **RecordCount** de l'objet **Recordset** est égal à 0. Lorsque vous ouvrez un objet **Recordset** qui contient au moins un enregistrement, le premier enregistrement est l'enregistrement actif et les propriétés **BOF** et **EOF** ont la valeur **False**; elles conservent la valeur **False** jusqu'à ce que vous dépassiez la limite (début ou fin) de l'objet **Recordset** à l'aide des méthodes **MovePrevious** ou **MoveNext**. Lorsque vous dépassez le début ou la fin de l'objet **Recordset**, aucun enregistrement n'existe ou n'est actif.</span><span class="sxs-lookup"><span data-stu-id="be8c9-p102">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0. When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively. When you move beyond the beginning or end of the **Recordset**, there is no current record or no record exists.</span></span>

<span data-ttu-id="be8c9-116">Si vous supprimez le dernier enregistrement restant dans l'objet **Recordset**, les propriétés **BOF** et **EOF** conservent la valeur **False** jusqu'à ce que vous tentiez de repositionner l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="be8c9-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="be8c9-p103">Si vous appelez la méthode **MoveLast** sur un objet **Recordset** contenant des enregistrements, le dernier enregistrement devient l'enregistrement actif ; si vous appelez ensuite la méthode **MoveNext**, l'enregistrement actif n'est plus valide et la propriété **EOF** a la valeur **True**. À l'inverse, si vous appelez la méthode **MoveFirst** sur un objet **Recordset** qui contient des enregistrements, le premier enregistrement devient l'enregistrement actif. Si vous utilisez ensuite la méthode **MovePrevious**, aucun enregistrement n'est actif et la propriété **BOF** prend la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="be8c9-p103">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**. Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="be8c9-119">En règle générale, lorsque vous manipulez tous les enregistrements d'un objet **Recordset**, votre code parcourt tous les enregistrements à l'aide de la méthode **MoveNext** jusqu'à ce que la propriété **EOF** ait la valeur **True**.</span><span class="sxs-lookup"><span data-stu-id="be8c9-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="be8c9-120">Si vous appelez la méthode **MoveNext** alors que la propriété **EOF** a la valeur **True** ou la méthode **MovePrevious** alors que la propriété **BOF** a la valeur **True**, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="be8c9-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="be8c9-121">Ce tableau indique les méthodes Move autorisées en fonction des différentes combinaisons des propriétés **BOF** et **EOF**.</span><span class="sxs-lookup"><span data-stu-id="be8c9-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="be8c9-122">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="be8c9-122">MoveFirst,</span></span><br />
<span data-ttu-id="be8c9-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="be8c9-123">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="be8c9-124">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="be8c9-124">MovePrevious,</span></span><br />
<span data-ttu-id="be8c9-125">Déplacer &lt; 0</span><span class="sxs-lookup"><span data-stu-id="be8c9-125">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="be8c9-126">Move 0</span><span class="sxs-lookup"><span data-stu-id="be8c9-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="be8c9-127">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="be8c9-127">MoveNext,</span></span><br />
<span data-ttu-id="be8c9-128">Déplacer &gt; 0</span><span class="sxs-lookup"><span data-stu-id="be8c9-128">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be8c9-129"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-129"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="be8c9-130">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-130">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="be8c9-131">Autorisé</span><span class="sxs-lookup"><span data-stu-id="be8c9-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="be8c9-132">Erreur</span><span class="sxs-lookup"><span data-stu-id="be8c9-132">Error</span></span></p></td>
<td><p><span data-ttu-id="be8c9-133">Erreur</span><span class="sxs-lookup"><span data-stu-id="be8c9-133">Error</span></span></p></td>
<td><p><span data-ttu-id="be8c9-134">Autorisé</span><span class="sxs-lookup"><span data-stu-id="be8c9-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be8c9-135"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-135"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="be8c9-136">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-136">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="be8c9-137">Autorisé</span><span class="sxs-lookup"><span data-stu-id="be8c9-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="be8c9-138">Autorisé</span><span class="sxs-lookup"><span data-stu-id="be8c9-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="be8c9-139">Erreur</span><span class="sxs-lookup"><span data-stu-id="be8c9-139">Error</span></span></p></td>
<td><p><span data-ttu-id="be8c9-140">Erreur</span><span class="sxs-lookup"><span data-stu-id="be8c9-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be8c9-141">Les deux propriétés ont la valeur <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="be8c9-142">Erreur</span><span class="sxs-lookup"><span data-stu-id="be8c9-142">Error</span></span></p></td>
<td><p><span data-ttu-id="be8c9-143">Erreur</span><span class="sxs-lookup"><span data-stu-id="be8c9-143">Error</span></span></p></td>
<td><p><span data-ttu-id="be8c9-144">Erreur</span><span class="sxs-lookup"><span data-stu-id="be8c9-144">Error</span></span></p></td>
<td><p><span data-ttu-id="be8c9-145">Erreur</span><span class="sxs-lookup"><span data-stu-id="be8c9-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be8c9-146">Les deux propriétés ont la valeur <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="be8c9-147">Autorisé</span><span class="sxs-lookup"><span data-stu-id="be8c9-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="be8c9-148">Autorisé</span><span class="sxs-lookup"><span data-stu-id="be8c9-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="be8c9-149">Autorisé</span><span class="sxs-lookup"><span data-stu-id="be8c9-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="be8c9-150">Autorisé</span><span class="sxs-lookup"><span data-stu-id="be8c9-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be8c9-p104">Si une méthode Move est autorisée, cela ne signifie pas qu'elle parviendra à localiser un enregistrement, mais simplement que la tentative d'exécution de la méthode Move est autorisée et qu'elle ne générera pas d'erreur. L'état des propriétés **BOF** et **EOF** peut changer à la suite de l'exécution de la méthode Move.</span><span class="sxs-lookup"><span data-stu-id="be8c9-p104">Allowing a Move method doesn't mean that the method will successfully locate a record. It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error. The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="be8c9-p105">Une méthode **OpenRecordset** appelle en interne une méthode **MoveFirst**. Par conséquent, l'exécution d'une méthode **OpenRecordset** sur un jeu d'enregistrements vide affecte aux propriétés **BOF** et **EOF** la valeur **True** (consultez le tableau suivant pour en savoir plus sur le comportement d'une méthode **MoveFirst** qui a échoué).</span><span class="sxs-lookup"><span data-stu-id="be8c9-p105">An **OpenRecordset** method internally invokes a **MoveFirst** method. Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**. (See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="be8c9-157">Toutes les méthodes Move qui parviennent à localiser un enregistrement affectent aux propriétés **BOF** et **EOF** la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="be8c9-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="be8c9-158">Dans un espace de travail Microsoft Access, si vous ajoutez un enregistrement à un objet **Recordset** vide, **BOF** prend la valeur **False** mais **EOF** conserve la valeur **True**, indiquant que la fin de l'objet **Recordset** se trouve à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="be8c9-158">In a Microsoft Access workspace, if you add a record to an empty **Recordset**, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of **Recordset**.</span></span>

<span data-ttu-id="be8c9-159">L'appel de la méthode **Delete**, même si elle supprime le dernier enregistrement présent dans un objet **Recordset** ne modifie pas le paramètre des propriétés **BOF** ou **EOF**.</span><span class="sxs-lookup"><span data-stu-id="be8c9-159">Any **Delete** method, even if it removes the only remaining record from a **Recordset**, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="be8c9-160">Le tableau suivant montre les répercussions sur les paramètres des propriétés **BOF** et **EOF** lorsque les méthodes Move ne parviennent pas à localiser un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="be8c9-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="be8c9-161">BOF</span><span class="sxs-lookup"><span data-stu-id="be8c9-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="be8c9-162">EOF</span><span class="sxs-lookup"><span data-stu-id="be8c9-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be8c9-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="be8c9-164"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="be8c9-165"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be8c9-166"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="be8c9-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="be8c9-167">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="be8c9-167">No change</span></span></p></td>
<td><p><span data-ttu-id="be8c9-168">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="be8c9-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be8c9-169"><strong>MovePrevious</strong>, <strong>déplacer</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="be8c9-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="be8c9-170"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="be8c9-171">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="be8c9-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be8c9-172"><strong>MoveNext</strong>, <strong>déplacer</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="be8c9-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="be8c9-173">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="be8c9-173">No change</span></span></p></td>
<td><p><span data-ttu-id="be8c9-174"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="be8c9-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

