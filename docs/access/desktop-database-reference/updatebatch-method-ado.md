---
title: UpdateBatch, méthode (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ce946d3354f6bbf05ac3819efc5f96c436fa174
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950124"
---
# <a name="updatebatch-method-ado"></a><span data-ttu-id="5f846-102">UpdateBatch, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="5f846-102">UpdateBatch method (ADO)</span></span>

<span data-ttu-id="5f846-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f846-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f846-104">Écrit toutes les mises à jour par lot en attente sur le disque.</span><span class="sxs-lookup"><span data-stu-id="5f846-104">Writes all pending batch updates to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f846-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f846-105">Syntax</span></span>

<span data-ttu-id="5f846-106">*jeu d’enregistrements*. UpdateBatch*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="5f846-106">*recordset*.UpdateBatch*AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="5f846-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f846-107">Parameters</span></span>

|<span data-ttu-id="5f846-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5f846-108">Parameter</span></span>|<span data-ttu-id="5f846-109">Description</span><span class="sxs-lookup"><span data-stu-id="5f846-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5f846-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="5f846-110">*AffectRecords*</span></span> |<span data-ttu-id="5f846-p101">Facultatif. Valeur [AffectEnum](affectenum.md) indiquant le nombre d'enregistrements affectés par la méthode **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="5f846-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **UpdateBatch** method will affect.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5f846-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5f846-113">Remarks</span></span>

<span data-ttu-id="5f846-114">Utilisez la méthode **UpdateBatch** lorsque vous modifiez un objet **Recordset** en mode de mise à jour par lot pour transmettre toutes les modifications apportées à un objet **Recordset** dans la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="5f846-114">Use the **UpdateBatch** method when modifying a **Recordset** object in batch update mode to transmit all changes made in a **Recordset** object to the underlying database.</span></span>

<span data-ttu-id="5f846-p102">Si l'objet **Recordset** prend en charge la mise à jour par lot, vous pouvez mettre localement en cache plusieurs modifications apportées à un ou plusieurs enregistrements, jusqu'à ce que vous appeliez la méthode **UpdateBatch**. Si vous modifiez l'enregistrement actif ou si vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **UpdateBatch**, ADO appelle automatiquement la méthode [Update](update-method-ado.md) pour enregistrer les modifications en attente apportées à l'enregistrement actif avant de transmettre les modifications par lot au fournisseur. Vous ne devez utiliser la mise à jour par lot qu'avec un curseur statique ou jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="5f846-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the [Update](update-method-ado.md) method to save any pending changes to the current record before transmitting the batched changes to the provider. You should use batch updating with either a keyset or static cursor only.</span></span>

> [!NOTE]
> <span data-ttu-id="5f846-118">[!REMARQUE] Si vous spécifiez **adAffectGroup** comme valeur de ce paramètre, une erreur est générée lorsqu'il n'y a pas d'enregistrement visible dans l'objet **Recordset** actif (par exemple, un filtre qui ne donne aucun enregistrement correspondant).</span><span class="sxs-lookup"><span data-stu-id="5f846-118">Specifying **adAffectGroup** as the value for this parameter will result in an error when there are no visible records in the current **Recordset** (such as a filter for which no records match).</span></span>

<span data-ttu-id="5f846-p103">Si la transmission des modifications échoue pour un ou tous les enregistrements en raison d’un conflit avec les données sous-jacentes (par exemple, un enregistrement déjà supprimé par un autre utilisateur), le fournisseur renvoie des avertissements dans la collection [Errors](errors-collection-ado.md) et une erreur d’exécution est générée. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) et [Status](status-property-ado-recordset.md) pour rechercher les enregistrements à l’origine de conflits.</span><span class="sxs-lookup"><span data-stu-id="5f846-p103">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="5f846-121">Pour annuler les mises à jour par lot en attente, utilisez la méthode [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5f846-121">To cancel all pending batch updates, use the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="5f846-122">Si les propriétés dynamiques [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) et [Update Resync](update-resync-property-dynamic-ado.md) sont définies et que l'objet **Recordset** est le résultat de l'exécution d'une opération JOIN sur plusieurs tables, l'exécution de la méthode **UpdateBatch** est implicitement suivie par la méthode [Resync](resync-method-ado.md) en fonction des paramètres définis dans la propriété **Update Resync**.</span><span class="sxs-lookup"><span data-stu-id="5f846-122">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Update Resync](update-resync-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the execution of the **UpdateBatch** method is implicitly followed by the [Resync](resync-method-ado.md) method depending on the settings of the **Update Resync** property.</span></span>

<span data-ttu-id="5f846-p104">L'ordre dans lequel les mises à jour individuelles d'un lot sont effectuées sur la source de données ne correspond pas forcément à celui de leur exécution dans l'objet **Recordset** local. L'ordre de mises à jour dépend du fournisseur. Ne l'oubliez pas lorsque vous codez des mises à jour associées entre elles, comme des contraintes de clé externe en cas d'insertion ou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5f846-p104">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local **Recordset**. Update order is dependent upon the provider. Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</span></span>

