---
title: Clone, méthode - ActiveX Data Objects (ADO)
TOCTitle: Clone Method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efff94e9f86d1fac7fd8b3716b1df2029bd32eb9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876385"
---
# <a name="clone-method-ado"></a><span data-ttu-id="d3d9f-102">Clone, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="d3d9f-102">Clone Method (ADO)</span></span>


<span data-ttu-id="d3d9f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3d9f-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="d3d9f-p101">Crée une copie de l'objet [Recordset](recordset-object-ado.md) à partir d'un objet **Recordset** existant. Spécifie éventuellement que le clone doit être en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-p101">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object. Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d9f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3d9f-106">Syntax</span></span>

<span data-ttu-id="d3d9f-107">**La valeur** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="d3d9f-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="d3d9f-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d3d9f-108">Return value</span></span>

<span data-ttu-id="d3d9f-109">Retourne une référence d'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3d9f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3d9f-110">Parameters</span></span>

  - <span data-ttu-id="d3d9f-111">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="d3d9f-111">*rstDuplicate*</span></span>

  - <span data-ttu-id="d3d9f-112">Variable objet qui identifie la copie de l'objet **Recordset** à créer.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-112">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>

  - <span data-ttu-id="d3d9f-113">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="d3d9f-113">*rstOriginal*</span></span>

  - <span data-ttu-id="d3d9f-114">Variable objet qui identifie l'objet **Recordset** à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-114">An object variable that identifies the **Recordset** object to be duplicated.</span></span>

  - <span data-ttu-id="d3d9f-115">*LockType*</span><span class="sxs-lookup"><span data-stu-id="d3d9f-115">*LockType*</span></span>

  - <span data-ttu-id="d3d9f-p102">Facultatif. Valeur [LockTypeEnum](locktypeenum.md) qui spécifie le type de verrou de l'objet **Recordset** d'origine ou un objet **Recordset** en lecture seule. Les valeurs valides sont **adLockUnspecified** ou **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3d9f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d3d9f-119">Remarks</span></span>

<span data-ttu-id="d3d9f-p103">Faites appel à la méthode **Clone** pour créer plusieurs copies de l'objet **Recordset**, notamment si vous voulez conserver plusieurs enregistrements actifs dans un jeu d'enregistrements donné. L'utilisation de la méthode **Clone** est plus efficace que la création et l'ouverture d'un nouvel objet **Recordset** avec la même définition que l'original.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="d3d9f-p104">Si elle existe, la propriété [Filter](filter-property-ado.md) de l'objet **Recordset** d'origine, n'est pas appliquée au clone. Définissez la propriété **Filter** du nouvel objet **Recordset** afin de filtrer les résultats. Le moyen le plus simple de copier une valeur **Filter** existante consiste à l'affecter directement de cette façon :</span><span class="sxs-lookup"><span data-stu-id="d3d9f-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="d3d9f-125">L'enregistrement actif du clone que vous venez de créer correspond au premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-125">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="d3d9f-p105">Les modifications apportées à un objet **Recordset** apparaissent dans tous ses clones, quel que soit le type de curseur utilisé. Toutefois, après l'exécution de la méthode [Requery](requery-method-ado.md) sur l'objet **Recordset** d'origine, les clones ne sont plus synchronisés avec l'original.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="d3d9f-128">De même que la fermeture de l'objet **Recordset** d'origine ne ferme pas ses clones, la fermeture d'un clone ne ferme pas l'original ni aucune autre copie.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-128">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="d3d9f-p106">Vous ne pouvez cloner qu'un objet **Recordset** prenant en charge les signets. Les valeurs de signet sont interchangeables ; cela signifie qu'une référence de signet d'un objet **Recordset** renvoie au même enregistrement dans l'un de ses clones.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="d3d9f-131">Certains événements **Recordset** qui sont déclenchées déclenche également dans tous les clones de **l’objet Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d3d9f-131">Some **Recordset** events that are triggered will also fire in all **Recordset** clones.</span></span> <span data-ttu-id="d3d9f-132">Toutefois, étant donné que l’enregistrement actif peut différer entre clonée **jeux d’enregistrements**, les événements peut-être pas valides pour le clone.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-132">However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="d3d9f-133">Par exemple, si vous modifiez la valeur d'un champ, un événement [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) est déclenché au niveau de l'objet **Recordset** modifié et de tous ses clones.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-133">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones.</span></span> <span data-ttu-id="d3d9f-134">Le paramètre *Fields* de l’événement **WillChangeField** d’un **jeu d’enregistrements** d' clonée (où la modification a été apportée pas) système simplement faire référence aux champs de l’enregistrement actif du clone, qui peut être un enregistrement différent de celui en cours Enregistrer de la **objet Recordset** d’origine où la modification s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-134">The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="d3d9f-135">Le tableau suivant répertorie tous les événements **Recordset** et indique s'ils sont valides et s'ils sont déclenchés pour tous les clones de l'objet Recordset générés à l'aide de la méthode **Clone**.</span><span class="sxs-lookup"><span data-stu-id="d3d9f-135">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3d9f-136">Événement</span><span class="sxs-lookup"><span data-stu-id="d3d9f-136">Event</span></span></p></th>
<th><p><span data-ttu-id="d3d9f-137">Déclenché au niveau des clones ?</span><span class="sxs-lookup"><span data-stu-id="d3d9f-137">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3d9f-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-138"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-139">Non</span><span class="sxs-lookup"><span data-stu-id="d3d9f-139">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3d9f-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-140"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-141">Non</span><span class="sxs-lookup"><span data-stu-id="d3d9f-141">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3d9f-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-142"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-143">Non</span><span class="sxs-lookup"><span data-stu-id="d3d9f-143">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3d9f-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-144"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-145">Oui</span><span class="sxs-lookup"><span data-stu-id="d3d9f-145">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3d9f-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-146"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-147">Non</span><span class="sxs-lookup"><span data-stu-id="d3d9f-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3d9f-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-148"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-149">Oui</span><span class="sxs-lookup"><span data-stu-id="d3d9f-149">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3d9f-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-150"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-151">Non</span><span class="sxs-lookup"><span data-stu-id="d3d9f-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3d9f-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-152"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-153">Oui</span><span class="sxs-lookup"><span data-stu-id="d3d9f-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3d9f-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-154"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-155">Oui</span><span class="sxs-lookup"><span data-stu-id="d3d9f-155">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3d9f-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-156"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-157">Non</span><span class="sxs-lookup"><span data-stu-id="d3d9f-157">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d3d9f-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="d3d9f-158"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="d3d9f-159">Non</span><span class="sxs-lookup"><span data-stu-id="d3d9f-159">No</span></span></p></td>
</tr>
</tbody>
</table>

