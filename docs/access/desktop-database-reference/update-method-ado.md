---
title: Update, méthode (ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f077634abea6fadfe5c4305fc25b28e6d57bf13e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306236"
---
# <a name="update-method-ado"></a><span data-ttu-id="44896-102">Update, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="44896-102">Update method (ADO)</span></span>

<span data-ttu-id="44896-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44896-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44896-104">Enregistre les modifications apportées à la ligne active d’un objet [Recordset](recordset-object-ado.md) ou à la collection [Fields](fields-collection-ado.md) d’un objet [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="44896-104">Saves any changes you make to the current row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="44896-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44896-105">Syntax</span></span>

<span data-ttu-id="44896-106">*recordset*. Mettre à *jour les champs,* *valeurs*</span><span class="sxs-lookup"><span data-stu-id="44896-106">*recordset*.Update *Fields*, *Values*</span></span>

<span data-ttu-id="44896-107">*.*</span><span class="sxs-lookup"><span data-stu-id="44896-107">*record*.</span></span> <span data-ttu-id="44896-108">*Champs*. Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="44896-108">*Fields*.Update</span></span>

## <a name="parameters"></a><span data-ttu-id="44896-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44896-109">Parameters</span></span>

|<span data-ttu-id="44896-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="44896-110">Parameter</span></span>|<span data-ttu-id="44896-111">Description</span><span class="sxs-lookup"><span data-stu-id="44896-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="44896-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="44896-112">*Fields*</span></span> |<span data-ttu-id="44896-p102">Facultatif. Valeur de type **Variant** représentant un nom unique ou tableau de valeurs **Variant** représentant les noms ou positions ordinales des champs à modifier.</span><span class="sxs-lookup"><span data-stu-id="44896-p102">Optional. A **Variant** that represents a single name, or a **Variant** array that represents names or ordinal positions of the field or fields you wish to modify.</span></span>|
|<span data-ttu-id="44896-115">*Values*</span><span class="sxs-lookup"><span data-stu-id="44896-115">*Values*</span></span> |<span data-ttu-id="44896-p103">Facultatif. Valeur de type **Variant** représentant une valeur unique ou un tableau de valeurs **Variant** représentant les valeurs du ou des champs du nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="44896-p103">Optional. A **Variant** that represents a single value, or a **Variant** array that represents values for the field or fields in the new record.</span></span>|

## <a name="remarks"></a><span data-ttu-id="44896-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="44896-118">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="44896-119">Recordset</span><span class="sxs-lookup"><span data-stu-id="44896-119">Recordset</span></span>

<span data-ttu-id="44896-p104">Utilisez la méthode **Update** pour enregistrer les modifications apportées à l'enregistrement actif d'un objet **Recordset** depuis l'appel de la méthode [AddNew](addnew-method-ado.md) ou la modification des valeurs des champs d'un enregistrement existant. L'objet **Recordset** doit prendre en charge les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="44896-p104">Use the **Update** method to save any changes you make to the current record of a **Recordset** object since calling the [AddNew](addnew-method-ado.md) method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="44896-122">Pour définir des valeurs de champ, effectuez l'une des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="44896-122">To set field values, do one of the following:</span></span>

- <span data-ttu-id="44896-123">Affectez des valeurs à la propriété [Value](field-object-ado.md) d'un objet [Field](value-property-ado.md) et appelez la méthode **Update**.</span><span class="sxs-lookup"><span data-stu-id="44896-123">Assign values to a [Field](field-object-ado.md) object's [Value](value-property-ado.md) property and call the **Update** method.</span></span>

- <span data-ttu-id="44896-124">Passez un nom de champ et une valeur comme arguments avec l'appel de **Update**.</span><span class="sxs-lookup"><span data-stu-id="44896-124">Pass a field name and a value as arguments with the **Update** call.</span></span>

- <span data-ttu-id="44896-125">Passez un tableau de noms de champs et un tableau de valeurs avec l'appel de **Update**.</span><span class="sxs-lookup"><span data-stu-id="44896-125">Pass an array of field names and an array of values with the **Update** call.</span></span>

<span data-ttu-id="44896-p105">Lorsque vous utilisez des tableaux de champs et de valeurs, ces deux tableaux doivent contenir le même nombre d'éléments. De même, l'ordre des noms de champs doit correspondre à l'ordre des valeurs des champs. Si le nombre et l'ordre des champs et des valeurs ne correspondent pas, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="44896-p105">When you use arrays of fields and values, there must be an equal number of elements in both arrays. Also, the order of field names must match the order of field values. If the number and order of fields and values do not match, an error occurs.</span></span>

<span data-ttu-id="44896-p106">Si l'objet **Recordset** prend en charge la mise à jour par lot, vous pouvez mettre en cache plusieurs modifications d'un ou plusieurs enregistrements jusqu'à ce que vous appeliez la méthode [UpdateBatch](updatebatch-method-ado.md). Si vous modifiez l'enregistrement actif ou que vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **UpdateBatch**, ADO appelle automatiquement la méthode **Update** pour enregistrer les modifications en attente apportées à l'enregistrement avant de transmettre les modifications mises en cache au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="44896-p106">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the [UpdateBatch](updatebatch-method-ado.md) method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="44896-p107">Si vous quittez l'enregistrement ajouté ou modifié avant d'appeler la méthode **Update**, ADO appelle automatiquement la méthode **Update** pour enregistrer les modifications. Vous devez appeler la méthode [CancelUpdate](cancelupdate-method-ado.md) si vous souhaitez annuler les modifications apportées à l'enregistrement actif ou supprimer un enregistrement qui vient d'être ajouté.</span><span class="sxs-lookup"><span data-stu-id="44896-p107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes. You must call the [CancelUpdate](cancelupdate-method-ado.md) method if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="44896-133">L'enregistrement actif reste actif après avoir appelé la méthode **Update**.</span><span class="sxs-lookup"><span data-stu-id="44896-133">The current record remains current after you call the **Update** method.</span></span>

### <a name="record"></a><span data-ttu-id="44896-134">Record</span><span class="sxs-lookup"><span data-stu-id="44896-134">Record</span></span>

<span data-ttu-id="44896-135">La méthode **Update** finalise les ajouts, suppressions et mises à jour des champs de la collection [Fields](fields-collection-ado.md) d’un objet **Record**.</span><span class="sxs-lookup"><span data-stu-id="44896-135">The **Update** method finalizes additions, deletions, and updates to fields in the [Fields](fields-collection-ado.md) collection of a **Record** object.</span></span>

<span data-ttu-id="44896-p108">Par exemple, les champs supprimés avec la méthode **Delete** sont marqués immédiatement pour suppression mais restent dans la collection. La méthode **Update** doit être appelée pour supprimer réellement ces champs de la collection du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="44896-p108">For example, fields deleted with the **Delete** method are marked for deletion immediately but remain in the collection. The **Update** method must be called to actually delete these fields from the provider's collection.</span></span>

