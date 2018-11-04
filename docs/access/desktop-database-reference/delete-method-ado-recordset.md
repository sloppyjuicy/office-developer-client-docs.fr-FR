---
title: Delete, méthode (Recordset ADO)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a7ab998052cc08aa57320d05e46542b84282e6c
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949508"
---
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="915ac-102">Delete, méthode (Recordset ADO)</span><span class="sxs-lookup"><span data-stu-id="915ac-102">Delete method (ADO Recordset)</span></span>

<span data-ttu-id="915ac-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="915ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="915ac-104">Supprime l'enregistrement actif ou un groupe d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="915ac-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="915ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="915ac-105">Syntax</span></span>

<span data-ttu-id="915ac-106">*jeu d’enregistrements*. Supprimer *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="915ac-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="915ac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="915ac-107">Parameters</span></span>

|<span data-ttu-id="915ac-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="915ac-108">Parameter</span></span>|<span data-ttu-id="915ac-109">Description</span><span class="sxs-lookup"><span data-stu-id="915ac-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="915ac-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="915ac-110">*AffectRecords*</span></span> |<span data-ttu-id="915ac-p101">Valeur [AffectEnum](affectenum.md) qui détermine le nombre d'enregistrements concernés par la méthode **Delete**. La valeur par défaut est **adAffectCurrent**.</span><span class="sxs-lookup"><span data-stu-id="915ac-p101">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect. The default value is **adAffectCurrent**.</span></span>|

> [!NOTE]
> <span data-ttu-id="915ac-113">[!REMARQUE] **adAffectAll** et **adAffectAllChapters** ne sont pas des arguments valides de la méthode **Delete**.</span><span class="sxs-lookup"><span data-stu-id="915ac-113">**adAffectAll** and **adAffectAllChapters** are not valid arguments to **Delete**.</span></span>

## <a name="remarks"></a><span data-ttu-id="915ac-114">Notes</span><span class="sxs-lookup"><span data-stu-id="915ac-114">Remarks</span></span>

<span data-ttu-id="915ac-p102">L'utilisation de la méthode **Delete** marque pour suppression l'enregistrement actif ou un groupe d'enregistrements d'un objet [Recordset](recordset-object-ado.md). Si l'objet **Recordset** n'autorise pas la suppression d'enregistrements, une erreur se produit. Si vous êtes en mode de mise à jour immédiate, les suppressions sont effectuées immédiatement dans la base de données. S'il est impossible de supprimer un enregistrement (en raison de violations d'intégrité de la base de données, par exemple), l'enregistrement reste en mode édition après l'appel de la méthode **Update**. Cela signifie que vous devez annuler la mise à jour avec [CancelUpdate](cancelupdate-method-ado.md) avant de quitter l'enregistrement actif (par exemple, avec les méthodes [Close](close-method-ado.md), [Move](move-method-ado.md) ou [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="915ac-p102">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion. If the **Recordset** object doesn't allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="915ac-p103">Si vous êtes en mode de mise à jour par lot, les enregistrements sont marqués pour suppression dans le cache et la suppression effective intervient lorsque vous appelez la méthode [UpdateBatch](updatebatch-method-ado.md). (Utilisez la propriété [Filter](filter-property-ado.md) pour consulter les enregistrements supprimés.)</span><span class="sxs-lookup"><span data-stu-id="915ac-p103">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method. (Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="915ac-p104">Une tentative de récupération des valeurs des champs de l'enregistrement supprimé génère une erreur. Après la suppression de l'enregistrement actif, l'enregistrement supprimé reste actif jusqu'à ce que vous accédiez à un autre enregistrement. Dès que vous avez quitté l'enregistrement supprimé, ce dernier n'est plus accessible.</span><span class="sxs-lookup"><span data-stu-id="915ac-p104">Retrieving field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="915ac-p105">Si vous imbriquez des suppressions dans une transaction, vous pouvez récupérer des enregistrements supprimés avec la méthode [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). En mode de mise à jour par lot, vous pouvez annuler une suppression en attente ou un groupe de suppressions en attente avec la méthode [Cancel Batch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="915ac-p105">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="915ac-p106">Si la tentative de suppression des enregistrements échoue en raison d'un conflit avec les données sous-jacentes (par exemple, si un autre utilisateur a déjà supprimé un enregistrement), le fournisseur retourne des avertissements dans la collection [Errors](errors-collection-ado.md) sans pour autant interrompre l'exécution du programme. Une erreur d'exécution se produit uniquement en cas de conflits sur tous les enregistrements demandés.</span><span class="sxs-lookup"><span data-stu-id="915ac-p106">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="915ac-129">Si la propriété dynamique [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) est définie et que l'objet **Recordset** résulte de l'exécution d'une opération JOIN sur plusieurs tables, la méthode **Delete** supprime uniquement les lignes de la table nommée dans la propriété [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="915ac-129">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>

