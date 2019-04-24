---
title: CancelBatch, méthode (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 832b367824fd8043486ff85f63739c3288696774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296639"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="8402f-102">CancelBatch, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="8402f-102">CancelBatch method (ADO)</span></span>

<span data-ttu-id="8402f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8402f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8402f-104">Annule une mise à jour par lot en attente.</span><span class="sxs-lookup"><span data-stu-id="8402f-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="8402f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8402f-105">Syntax</span></span>

<span data-ttu-id="8402f-106">*Recordset*. CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="8402f-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="8402f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8402f-107">Parameters</span></span>

|<span data-ttu-id="8402f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8402f-108">Parameter</span></span>|<span data-ttu-id="8402f-109">Description</span><span class="sxs-lookup"><span data-stu-id="8402f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8402f-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="8402f-110">*AffectRecords*</span></span> |<span data-ttu-id="8402f-p101">Facultatif. Valeur [AffectEnum](affectenum.md) qui indique le nombre d'enregistrements affectés par la méthode **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="8402f-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span> |

## <a name="remarks"></a><span data-ttu-id="8402f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8402f-113">Remarks</span></span>

<span data-ttu-id="8402f-p102">Utilisez la méthode **CancelBatch** pour annuler toutes les mises à jour en attente dans un objet [Recordset](recordset-object-ado.md) en mode de mise à jour par lot. Si l'objet **Recordset** est en mode de mise à jour immédiate, l'appel de la méthode **CancelBatch** sans **adAffectCurrent** génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="8402f-p102">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode. If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="8402f-p103">Si vous modifiez l'enregistrement actif ou que vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **CancelBatch**, ADO commence par appeler la méthode [CancelUpdate](cancelupdate-method-ado.md) pour annuler les modifications mises en cache. Ensuite, toutes les modifications en attente dans l'objet **Recordset** sont annulées.</span><span class="sxs-lookup"><span data-stu-id="8402f-p103">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes. After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="8402f-p104">Il se peut que l'enregistrement actif ne puisse pas être déterminé après un appel de la méthode **CancelBatch**, notamment si vous étiez en train d'ajouter un nouvel enregistrement. C'est pourquoi il est conseillé de définir la position de l'enregistrement actif à un emplacement connu de l'objet **Recordset** après avoir appelé la méthode **CancelBatch**. Appelez, par exemple, la méthode [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8402f-p104">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record. For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call. For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="8402f-p105">Si la tentative d’annulation des mises à jour en attente échoue à cause d’un conflit avec les données sous-jacentes (par exemple, un enregistrement a été supprimé par un autre utilisateur), le fournisseur retourne des avertissements dans la collection [Errors](errors-collection-ado.md), mais n’interrompt pas l’exécution. Une erreur d’exécution ne se produit qu’en cas de conflits dans tous les enregistrements demandés. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) et [Status](status-property-ado-recordset.md) pour localiser les enregistrements en conflit.</span><span class="sxs-lookup"><span data-stu-id="8402f-p105">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

