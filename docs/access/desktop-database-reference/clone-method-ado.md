---
title: Clone, méthode-ActiveX Data Objects (ADO)
TOCTitle: Clone method (ADO)
ms:assetid: ca9b2b76-90bf-9a60-2611-3cb4977d5591
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249984(v=office.15)
ms:contentKeyID: 48547693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 095191bbfe55f2c38529cb1c260979c48dd2d5f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296345"
---
# <a name="clone-method-ado"></a><span data-ttu-id="24fc6-102">Clone, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="24fc6-102">Clone method (ADO)</span></span>

<span data-ttu-id="24fc6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24fc6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24fc6-104">Crée une copie de l'objet [Recordset](recordset-object-ado.md) à partir d'un objet **Recordset** existant.</span><span class="sxs-lookup"><span data-stu-id="24fc6-104">Creates a duplicate [Recordset](recordset-object-ado.md) object from an existing **Recordset** object.</span></span> <span data-ttu-id="24fc6-105">Spécifie éventuellement que le clone doit être en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24fc6-105">Optionally, specifies that the clone be read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="24fc6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24fc6-106">Syntax</span></span>

<span data-ttu-id="24fc6-107">**Définir** *rstDuplicate*  =  *rstOriginal*. Clone (*LockType*)</span><span class="sxs-lookup"><span data-stu-id="24fc6-107">**Set** *rstDuplicate* = *rstOriginal*.Clone (*LockType*)</span></span>

## <a name="return-value"></a><span data-ttu-id="24fc6-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="24fc6-108">Return value</span></span>

<span data-ttu-id="24fc6-109">Retourne une référence d'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="24fc6-109">Returns a **Recordset** object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="24fc6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24fc6-110">Parameters</span></span>

|<span data-ttu-id="24fc6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="24fc6-111">Parameter</span></span>|<span data-ttu-id="24fc6-112">Description</span><span class="sxs-lookup"><span data-stu-id="24fc6-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="24fc6-113">*rstDuplicate*</span><span class="sxs-lookup"><span data-stu-id="24fc6-113">*rstDuplicate*</span></span> |<span data-ttu-id="24fc6-114">Variable objet qui identifie la copie de l'objet **Recordset** à créer.</span><span class="sxs-lookup"><span data-stu-id="24fc6-114">An object variable that identifies the duplicate **Recordset** object to be created.</span></span>|
|<span data-ttu-id="24fc6-115">*rstOriginal*</span><span class="sxs-lookup"><span data-stu-id="24fc6-115">*rstOriginal*</span></span> |<span data-ttu-id="24fc6-116">Variable objet qui identifie l'objet **Recordset** à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="24fc6-116">An object variable that identifies the **Recordset** object to be duplicated.</span></span>|
|<span data-ttu-id="24fc6-117">*LockType*</span><span class="sxs-lookup"><span data-stu-id="24fc6-117">*LockType*</span></span> |<span data-ttu-id="24fc6-p102">Facultatif. Valeur [LockTypeEnum](locktypeenum.md) qui spécifie le type de verrou de l'objet **Recordset** d'origine ou un objet **Recordset** en lecture seule. Les valeurs valides sont **adLockUnspecified** ou **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="24fc6-p102">Optional. A [LockTypeEnum](locktypeenum.md) value that specifies either the lock type of the original **Recordset**, or a read-only **Recordset**. Valid values are **adLockUnspecified** or **adLockReadOnly**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="24fc6-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="24fc6-121">Remarks</span></span>

<span data-ttu-id="24fc6-p103">Faites appel à la méthode **Clone** pour créer plusieurs copies de l'objet **Recordset**, notamment si vous voulez conserver plusieurs enregistrements actifs dans un jeu d'enregistrements donné. L'utilisation de la méthode **Clone** est plus efficace que la création et l'ouverture d'un nouvel objet **Recordset** avec la même définition que l'original.</span><span class="sxs-lookup"><span data-stu-id="24fc6-p103">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="24fc6-p104">Si elle existe, la propriété [Filter](filter-property-ado.md) de l'objet **Recordset** d'origine, n'est pas appliquée au clone. Définissez la propriété **Filter** du nouvel objet **Recordset** afin de filtrer les résultats. Le moyen le plus simple de copier une valeur **Filter** existante consiste à l'affecter directement de cette façon :</span><span class="sxs-lookup"><span data-stu-id="24fc6-p104">The [Filter](filter-property-ado.md) property of the original **Recordset**, if any, will not be applied to the clone. Set the **Filter** property of the new **Recordset** in order to filter the results. The simplest way to copy any existing **Filter** value is to assign it directly, like this:</span></span>

<span data-ttu-id="24fc6-127">L'enregistrement actif du clone que vous venez de créer correspond au premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="24fc6-127">The current record of a newly created clone is set to the first record.</span></span>

<span data-ttu-id="24fc6-p105">Les modifications apportées à un objet **Recordset** apparaissent dans tous ses clones, quel que soit le type de curseur utilisé. Toutefois, après l'exécution de la méthode [Requery](requery-method-ado.md) sur l'objet **Recordset** d'origine, les clones ne sont plus synchronisés avec l'original.</span><span class="sxs-lookup"><span data-stu-id="24fc6-p105">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="24fc6-130">De même que la fermeture de l'objet **Recordset** d'origine ne ferme pas ses clones, la fermeture d'un clone ne ferme pas l'original ni aucune autre copie.</span><span class="sxs-lookup"><span data-stu-id="24fc6-130">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="24fc6-p106">Vous ne pouvez cloner qu'un objet **Recordset** prenant en charge les signets. Les valeurs de signet sont interchangeables ; cela signifie qu'une référence de signet d'un objet **Recordset** renvoie au même enregistrement dans l'un de ses clones.</span><span class="sxs-lookup"><span data-stu-id="24fc6-p106">You can only clone a **Recordset** object that supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

<span data-ttu-id="24fc6-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span><span class="sxs-lookup"><span data-stu-id="24fc6-p107">Some **Recordset** events that are triggered will also fire in all **Recordset** clones. However, because the current record can differ between cloned **Recordsets**, the events may not be valid for the clone.</span></span>

<span data-ttu-id="24fc6-p108">Par exemple, si vous modifiez la valeur d’un champ, un événement [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) est déclenché au niveau de l’objet **Recordset** modifié et de tous ses clones. Le paramètre *Fields* de l’événement **WillChangeField** d’un objet **Recordset** cloné (qui, lui, n’a pas été modifié) référencera simplement les champs de l’enregistrement actif du clone, qui peut correspondre à un enregistrement différent de celui de l’objet **Recordset** d’origine au niveau duquel la modification a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="24fc6-p108">For example, if you change a value of a field, a [WillChangeField](willchangefield-and-fieldchangecomplete-events-ado.md) event will occur in the changed **Recordset** and in all clones. The *Fields* parameter of the **WillChangeField** event of a cloned **Recordset** (where the change was not made) will simply refer to the fields of the current record of the clone, which may be a different record than the current record of the original **Recordset** where the change occurred.</span></span>

<span data-ttu-id="24fc6-137">Le tableau suivant répertorie tous les événements **Recordset** et indique s'ils sont valides et s'ils sont déclenchés pour tous les clones de l'objet Recordset générés à l'aide de la méthode **Clone**.</span><span class="sxs-lookup"><span data-stu-id="24fc6-137">The following table provided a full listing of all **Recordset** events and indicates whether they are valid and triggered for any recordset clones generated using the **Clone** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24fc6-138">Événement</span><span class="sxs-lookup"><span data-stu-id="24fc6-138">Event</span></span></p></th>
<th><p><span data-ttu-id="24fc6-139">Déclenché au niveau des clones ?</span><span class="sxs-lookup"><span data-stu-id="24fc6-139">Triggered in clones?</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24fc6-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-140"><a href="endofrecordset-event-ado.md">EndOfRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-141">Non</span><span class="sxs-lookup"><span data-stu-id="24fc6-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24fc6-142"><a href="fetchcomplete-event-ado.md">FetchComplete,</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-142"><a href="fetchcomplete-event-ado.md">FetchComplete</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-143">Non</span><span class="sxs-lookup"><span data-stu-id="24fc6-143">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24fc6-144"><a href="fetchprogress-event-ado.md">FetchProgress,</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-144"><a href="fetchprogress-event-ado.md">FetchProgress</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-145">Non</span><span class="sxs-lookup"><span data-stu-id="24fc6-145">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24fc6-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-146"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-147">Oui</span><span class="sxs-lookup"><span data-stu-id="24fc6-147">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24fc6-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-148"><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-149">Non</span><span class="sxs-lookup"><span data-stu-id="24fc6-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24fc6-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-150"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-151">Oui</span><span class="sxs-lookup"><span data-stu-id="24fc6-151">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24fc6-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-152"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-153">Non</span><span class="sxs-lookup"><span data-stu-id="24fc6-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24fc6-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-154"><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-155">Oui</span><span class="sxs-lookup"><span data-stu-id="24fc6-155">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24fc6-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-156"><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-157">Oui</span><span class="sxs-lookup"><span data-stu-id="24fc6-157">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24fc6-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-158"><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-159">Non</span><span class="sxs-lookup"><span data-stu-id="24fc6-159">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24fc6-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span><span class="sxs-lookup"><span data-stu-id="24fc6-160"><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></span></span></p></td>
<td><p><span data-ttu-id="24fc6-161">Non</span><span class="sxs-lookup"><span data-stu-id="24fc6-161">No</span></span></p></td>
</tr>
</tbody>
</table>

