---
title: CancelBatch, méthode (ADO)
TOCTitle: CancelBatch Method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cbc16d01e04bbcff7ff28ccc8e7cb4f3fd6f3dec
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471464"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="5d800-102">CancelBatch, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="5d800-102">CancelBatch Method (ADO)</span></span>


<span data-ttu-id="5d800-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d800-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="5d800-104">Annule une mise à jour par lot en attente.</span><span class="sxs-lookup"><span data-stu-id="5d800-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d800-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d800-105">Syntax</span></span>

<span data-ttu-id="5d800-106">*jeu d’enregistrements*. CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="5d800-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="5d800-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d800-107">Parameters</span></span>

  - <span data-ttu-id="5d800-108">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="5d800-108">*AffectRecords*</span></span>

  - <span data-ttu-id="5d800-p101">Facultatif. Valeur [AffectEnum](affectenum.md) qui indique le nombre d'enregistrements affectés par la méthode **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="5d800-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d800-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5d800-111">Remarks</span></span>

<span data-ttu-id="5d800-p102">Utilisez la méthode **CancelBatch** pour annuler toutes les mises à jour en attente dans un objet [Recordset](recordset-object-ado.md) en mode de mise à jour par lot. Si l'objet **Recordset** est en mode de mise à jour immédiate, l'appel de la méthode **CancelBatch** sans **adAffectCurrent** génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="5d800-p102">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode. If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="5d800-p103">Si vous modifiez l'enregistrement actif ou que vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **CancelBatch**, ADO commence par appeler la méthode [CancelUpdate](cancelupdate-method-ado.md) pour annuler les modifications mises en cache. Ensuite, toutes les modifications en attente dans l'objet **Recordset** sont annulées.</span><span class="sxs-lookup"><span data-stu-id="5d800-p103">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes. After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="5d800-p104">Il se peut que l'enregistrement actif ne puisse pas être déterminé après un appel de la méthode **CancelBatch**, notamment si vous étiez en train d'ajouter un nouvel enregistrement. C'est pourquoi il est conseillé de définir la position de l'enregistrement actif à un emplacement connu de l'objet **Recordset** après avoir appelé la méthode **CancelBatch**. Appelez, par exemple, la méthode [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5d800-p104">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record. For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call. For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="5d800-p105">Si la tentative d’annulation des mises à jour en attente échoue à cause d’un conflit avec les données sous-jacentes (par exemple, un enregistrement a été supprimé par un autre utilisateur), le fournisseur retourne des avertissements dans la collection [Errors](errors-collection-ado.md), mais n’interrompt pas l’exécution. Une erreur d’exécution ne se produit qu’en cas de conflits dans tous les enregistrements demandés. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) et [Status](status-property-ado-recordset.md) pour localiser les enregistrements en conflit.</span><span class="sxs-lookup"><span data-stu-id="5d800-p105">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

