---
title: Recordset.EOF, propriété (DAO)
TOCTitle: EOF Property
ms:assetid: aa82c6f9-89da-1061-437c-8ffb000744b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821459(v=office.15)
ms:contentKeyID: 48546950
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 931de7dfc2cfb80726aafe7077c6107ec65d2f40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300608"
---
# <a name="recordseteof-property-dao"></a><span data-ttu-id="9a218-102">Recordset.EOF, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a218-102">Recordset.EOF Property (DAO)</span></span>


<span data-ttu-id="9a218-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a218-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a218-104">Renvoie une valeur qui indique si la position d'enregistrement actuelle suit le dernier enregistrement d'un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9a218-104">Returns a value that indicates whether the current record position is after the last record in a **Recordset** object.</span></span> <span data-ttu-id="9a218-105">**Boolean** (en lecture seule).</span><span class="sxs-lookup"><span data-stu-id="9a218-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a218-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a218-106">Syntax</span></span>

<span data-ttu-id="9a218-107">*expression* .EOF</span><span class="sxs-lookup"><span data-stu-id="9a218-107">expression  . EOF</span></span>

<span data-ttu-id="9a218-108">*expression* Variable représentant un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9a218-108">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a218-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a218-109">Remarks</span></span>

<span data-ttu-id="9a218-110">Vous pouvez utiliser la **BOF** et **EOF** propriétés pour déterminer si un **jeu d’enregistrements** objet contient des enregistrements ou que vous avez dépassé au-delà des limites d’un \*\* Jeu d’enregistrements\*\* lorsque vous déplacez à partir d’un enregistrement à l’objet.</span><span class="sxs-lookup"><span data-stu-id="9a218-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="9a218-111">Détermine l’emplacement du pointeur d’enregistrement actuel le **BOF** et **EOF** retournent des valeurs.</span><span class="sxs-lookup"><span data-stu-id="9a218-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="9a218-112">Si deux le **BOF** ou **EOF** propriété est **vrai**, il n’est aucun enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="9a218-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="9a218-p102">Si vous ouvrez un **jeu d’enregistrements** objet ne contenant aucun enregistrement, la **BOF** et **EOF** propriétés sont définies sur **vrai**et le \*\* Jeu d’enregistrements\*\* d’objet **RecordCount** paramètre de la propriété est égal à 0. Lorsque vous ouvrez un **jeu d’enregistrements** objet qui contient au moins un enregistrement, le premier enregistrement est l’enregistrement actif et le **BOF** et **EOF** propriétés sont \*\* Faux**; ils restent **faux** jusqu'à ce que vous déplacez au-delà de début ou à la fin de la **jeu d’enregistrements** objet à l’aide de la **MovePrevious** ou \*\* MoveNext** méthode, respectivement. Lorsque vous déplacez au-delà de début ou à la fin de la **jeu d’enregistrements**, il n’est aucun enregistrement actif ou n’existe aucun enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9a218-p102">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0. When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively. When you move beyond the beginning or end of the **Recordset**, there is no current record or no record exists.</span></span>

<span data-ttu-id="9a218-116">Si vous supprimez le dernier enregistrement restant dans la **jeu d’enregistrements** objet, le **BOF** et **EOF** propriétés peuvent restent **faux** jusqu'à ce que vous tentative de repositionner l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="9a218-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="9a218-p103">Si vous utilisez le **MoveLast** méthode sur un **jeu d’enregistrements** objet contenant les enregistrements, le dernier enregistrement devient l’enregistrement actif ; si vous utilisez ensuite la **MoveNext** méthode, la version actuelle enregistrement devient non valide et le **EOF** propriété est définie sur **vrai**. À l’inverse, si vous utilisez le **MoveFirst** méthode sur un **jeu d’enregistrements** objet contenant les enregistrements, le premier enregistrement devient l’enregistrement actif ; si vous utilisez ensuite la \*\*MovePrevious \*\* méthode, il n’est aucun enregistrement actif et le **BOF** propriété est définie sur **vrai**.</span><span class="sxs-lookup"><span data-stu-id="9a218-p103">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**. Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="9a218-119">En règle générale, lorsque vous travaillez avec tous les enregistrements dans une **jeu d’enregistrements** objet, votre code sera parcourir les enregistrements à l’aide de la **MoveNext** méthode jusqu'à ce que le **EOF** propriété est définie pour **vrai**.</span><span class="sxs-lookup"><span data-stu-id="9a218-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="9a218-120">Si vous utilisez le **MoveNext** méthode lors de la **EOF** propriété est définie sur **vrai** ou le **MovePrevious** méthode lors de la \*\* BOF\*\* propriété est définie sur **vrai**, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="9a218-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="9a218-121">Le tableau suivant répertorie les méthodes Move sont autorisés avec différentes combinaisons de la **BOF** et **EOF** propriétés.</span><span class="sxs-lookup"><span data-stu-id="9a218-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="9a218-122">MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="9a218-122">MoveFirst method</span></span><br />
<span data-ttu-id="9a218-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="9a218-123">MoveLast method</span></span></p></th>
<th><p><span data-ttu-id="9a218-124">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="9a218-124">MovePrevious method</span></span><br />
<span data-ttu-id="9a218-125">Move &lt; 0</span><span class="sxs-lookup"><span data-stu-id="9a218-125">&lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="9a218-126">Move 0</span><span class="sxs-lookup"><span data-stu-id="9a218-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="9a218-127">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="9a218-127">MoveNext method</span></span><br />
<span data-ttu-id="9a218-128">Move &gt; 0</span><span class="sxs-lookup"><span data-stu-id="9a218-128">&gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a218-129"><strong>BOF=True,</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-129"><strong>BOF=True,EOF=False</strong></span></span><br /><span data-ttu-id="9a218-130">
<strong>EOF=False</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-130">
<strong>BOF=True,EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="9a218-131">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9a218-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="9a218-132">Erreur</span><span class="sxs-lookup"><span data-stu-id="9a218-132">Error</span></span></p></td>
<td><p><span data-ttu-id="9a218-133">Erreur</span><span class="sxs-lookup"><span data-stu-id="9a218-133">Error</span></span></p></td>
<td><p><span data-ttu-id="9a218-134">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9a218-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a218-135"><strong>BOF=False,</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-135"><strong>BOF=False,EOF=True</strong></span></span><br /><span data-ttu-id="9a218-136">
<strong>EOF=True</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-136">
<strong>BOF=False,EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="9a218-137">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9a218-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="9a218-138">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9a218-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="9a218-139">Erreur</span><span class="sxs-lookup"><span data-stu-id="9a218-139">Error</span></span></p></td>
<td><p><span data-ttu-id="9a218-140">Erreur</span><span class="sxs-lookup"><span data-stu-id="9a218-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a218-141">Les deux <strong>vrai</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="9a218-142">Error</span><span class="sxs-lookup"><span data-stu-id="9a218-142">Error</span></span></p></td>
<td><p><span data-ttu-id="9a218-143">Erreur</span><span class="sxs-lookup"><span data-stu-id="9a218-143">Error</span></span></p></td>
<td><p><span data-ttu-id="9a218-144">Erreur</span><span class="sxs-lookup"><span data-stu-id="9a218-144">Error</span></span></p></td>
<td><p><span data-ttu-id="9a218-145">Error</span><span class="sxs-lookup"><span data-stu-id="9a218-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a218-146">Les deux <strong>faux</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="9a218-147">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9a218-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="9a218-148">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9a218-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="9a218-149">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9a218-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="9a218-150">Autorisé</span><span class="sxs-lookup"><span data-stu-id="9a218-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9a218-p104">Autoriser une méthode de déplacement ne signifie pas que la méthode parviendra à localiser un enregistrement. Il indique simplement qu’une tentative d’effectuer la méthode de déplacement spécifiée est autorisée et ne génère une erreur. L’état de la **BOF** et **EOF** propriétés peuvent changer suite au déplacement a été lancée.</span><span class="sxs-lookup"><span data-stu-id="9a218-p104">Allowing a Move method doesn't mean that the method will successfully locate a record. It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error. The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="9a218-p105">Un **OpenRecordset** méthode appelle en interne une **MoveFirst** méthode. Par conséquent, à l’aide un **OpenRecordset** méthode sur un ensemble de jeux d’enregistrements vide le **BOF** et **EOF** propriétés à **vrai**. (Reportez-vous au tableau suivant pour le comportement d’une situation d’échec **MoveFirst** méthode.)</span><span class="sxs-lookup"><span data-stu-id="9a218-p105">An **OpenRecordset** method internally invokes a **MoveFirst** method. Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**. (See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="9a218-157">Toutes les méthodes de déplacement qui correctement localiser un enregistrement configurera les deux **BOF** et **EOF** à **faux**.</span><span class="sxs-lookup"><span data-stu-id="9a218-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="9a218-158">Dans un espace de travail Microsoft Access, si vous ajoutez un enregistrement à un vide **jeu d’enregistrements**, **BOF** deviendra **faux**, mais **EOF** restent \*\* True\*\*, indiquant que la position actuelle est à la fin de **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="9a218-158">In a Microsoft Access workspace, if you add a record to an empty **Recordset**, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of **Recordset**.</span></span>

<span data-ttu-id="9a218-159">N’importe quel **supprimer** méthode, même si elle supprime du seul enregistrement restant à partir d’un **jeu d’enregistrements**, ne modifiez le paramètre de la **BOF** ou **EOF** propriété.</span><span class="sxs-lookup"><span data-stu-id="9a218-159">Any **Delete** method, even if it removes the only remaining record from a **Recordset**, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="9a218-160">Le tableau suivant montre comment déplacer des méthodes qui ne localiser un enregistrement affectent la **BOF** et **EOF** paramètres de propriété.</span><span class="sxs-lookup"><span data-stu-id="9a218-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="9a218-161">BOF</span><span class="sxs-lookup"><span data-stu-id="9a218-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="9a218-162">EOF</span><span class="sxs-lookup"><span data-stu-id="9a218-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a218-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="9a218-164"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="9a218-165"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a218-166"><strong></strong>Move</span><span class="sxs-lookup"><span data-stu-id="9a218-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="9a218-167">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="9a218-167">No change</span></span></p></td>
<td><p><span data-ttu-id="9a218-168">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="9a218-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a218-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="9a218-169">MovePrevious, Move < 0</span></span></p></td>
<td><p><span data-ttu-id="9a218-170"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="9a218-171">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="9a218-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a218-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="9a218-172">MoveNext, Move > 0</span></span></p></td>
<td><p><span data-ttu-id="9a218-173">Aucune modification</span><span class="sxs-lookup"><span data-stu-id="9a218-173">No change</span></span></p></td>
<td><p><span data-ttu-id="9a218-174"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="9a218-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

