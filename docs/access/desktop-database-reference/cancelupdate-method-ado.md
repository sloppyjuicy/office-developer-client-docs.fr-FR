---
title: CancelUpdate, méthode (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d5414f6f604392d64baba7e67c8b66d13afc94d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922586"
---
# <a name="cancelupdate-method-ado"></a><span data-ttu-id="df58c-102">CancelUpdate, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="df58c-102">CancelUpdate method (ADO)</span></span>


<span data-ttu-id="df58c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df58c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df58c-104">Annule toutes les modifications apportées à la ligne active ou à une nouvelle ligne d'un objet [Recordset](recordset-object-ado.md) ou dans la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md) avant que la méthode [Update](update-method-ado.md) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="df58c-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, before calling the [Update](update-method-ado.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="df58c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df58c-105">Syntax</span></span>

<span data-ttu-id="df58c-106">*jeu d’enregistrements*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="df58c-106">*recordset*.CancelUpdate</span></span>

<span data-ttu-id="df58c-107">*enregistrement*. *Champs*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="df58c-107">*record*.*Fields*.CancelUpdate</span></span>

## <a name="remarks"></a><span data-ttu-id="df58c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="df58c-108">Remarks</span></span>

<span data-ttu-id="df58c-109">**Objet Recordset**</span><span class="sxs-lookup"><span data-stu-id="df58c-109">**Recordset**</span></span>

<span data-ttu-id="df58c-p101">Faites appel à la méthode **CancelUpdate** pour annuler les modifications apportées à la ligne active ou pour supprimer la ligne que vous venez d'ajouter. Vous ne pouvez pas effectuer ces opérations après avoir appelé la méthode **Update** sauf si ces modifications font partie d'une transaction que vous pouvez annuler à l'aide de la méthode [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) ou d'une mise à jour par lot. Dans ce dernier cas, vous pouvez annuler la méthode **Update** à l'aide de la méthode **CancelUpdate** ou [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="df58c-p101">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row. You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method, or part of a batch update. In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="df58c-113">Si vous ajoutez une nouvelle ligne, lorsque vous appelez la méthode **CancelUpdate**, la ligne active représente celle qui était active avant l'appel de la méthode [AddNew](addnew-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="df58c-113">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the [AddNew](addnew-method-ado.md) call.</span></span>

<span data-ttu-id="df58c-p102">Si vous êtes en mode édition et que vous voulez quitter l'enregistrement actif (par exemple, en utilisant [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md)), vous pouvez faire appel à la méthode **CancelUpdate** pour annuler les modifications en attente. Cette opération est nécessaire si la mise à jour ne peut pas être publiée dans la source de données (par exemple, une tentative de suppression qui échoue suite à des violations de l'intégrité du référentiel laisse l'objet **Recordset** en mode édition après un appel de [Delete](delete-method-ado-recordset.md)).</span><span class="sxs-lookup"><span data-stu-id="df58c-p102">If you are in edit mode and want to move off the current record (for example, with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md)), you can use **CancelUpdate** to cancel any pending changes. You may need to do this if the update cannot successfully be posted to the data source (for example, an attempted delete that fails due to referential integrity violations will leave the **Recordset** in edit mode after a call to [Delete](delete-method-ado-recordset.md)).</span></span>

<span data-ttu-id="df58c-116">**Objet Record**</span><span class="sxs-lookup"><span data-stu-id="df58c-116">**Record**</span></span>

<span data-ttu-id="df58c-p103">La méthode **CancelUpdate** annule toute insertion ou suppression en attente d'objets [Field](field-object-ado.md), ainsi que les mises à jour en attente des champs existants et rétablit leurs valeurs d'origine. La propriété [Status](status-property-ado-recordset.md) de tous les champs de la collection **Fields** a la valeur **adFieldOK**.</span><span class="sxs-lookup"><span data-stu-id="df58c-p103">The **CancelUpdate** method cancels any pending insertions or deletions of [Field](field-object-ado.md) objects, and cancels pending updates of existing fields and restores them to their original values. The [Status](status-property-ado-recordset.md) property of all fields in the **Fields** collection is set to **adFieldOK**.</span></span>

