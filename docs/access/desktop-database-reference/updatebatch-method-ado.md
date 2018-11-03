---
title: UpdateBatch, méthode (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2e998bb49fab57927a8bb233d9eeb3245a1a3876
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929936"
---
# <a name="updatebatch-method-ado"></a><span data-ttu-id="0b6f5-102">UpdateBatch, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="0b6f5-102">UpdateBatch method (ADO)</span></span>


<span data-ttu-id="0b6f5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b6f5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b6f5-104">Écrit toutes les mises à jour par lot en attente sur le disque.</span><span class="sxs-lookup"><span data-stu-id="0b6f5-104">Writes all pending batch updates to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b6f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b6f5-105">Syntax</span></span>

<span data-ttu-id="0b6f5-106">*jeu d’enregistrements*. UpdateBatch*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="0b6f5-106">*recordset*.UpdateBatch*AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="0b6f5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b6f5-107">Parameters</span></span>

  - <span data-ttu-id="0b6f5-108">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="0b6f5-108">*AffectRecords*</span></span>

  - <span data-ttu-id="0b6f5-p101">Facultatif. Valeur [AffectEnum](affectenum.md) indiquant le nombre d'enregistrements affectés par la méthode **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="0b6f5-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **UpdateBatch** method will affect.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b6f5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0b6f5-111">Remarks</span></span>

<span data-ttu-id="0b6f5-112">Utilisez la méthode **UpdateBatch** lorsque vous modifiez un objet **Recordset** en mode de mise à jour par lot pour transmettre toutes les modifications apportées à un objet **Recordset** dans la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="0b6f5-112">Use the **UpdateBatch** method when modifying a **Recordset** object in batch update mode to transmit all changes made in a **Recordset** object to the underlying database.</span></span>

<span data-ttu-id="0b6f5-p102">Si l'objet **Recordset** prend en charge la mise à jour par lot, vous pouvez mettre localement en cache plusieurs modifications apportées à un ou plusieurs enregistrements, jusqu'à ce que vous appeliez la méthode **UpdateBatch**. Si vous modifiez l'enregistrement actif ou si vous ajoutez un nouvel enregistrement lorsque vous appelez la méthode **UpdateBatch**, ADO appelle automatiquement la méthode [Update](update-method-ado.md) pour enregistrer les modifications en attente apportées à l'enregistrement actif avant de transmettre les modifications par lot au fournisseur. Vous ne devez utiliser la mise à jour par lot qu'avec un curseur statique ou jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="0b6f5-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the [Update](update-method-ado.md) method to save any pending changes to the current record before transmitting the batched changes to the provider. You should use batch updating with either a keyset or static cursor only.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0b6f5-116">[!REMARQUE] Si vous spécifiez <STRONG>adAffectGroup</STRONG> comme valeur de ce paramètre, une erreur est générée lorsqu'il n'y a pas d'enregistrement visible dans l'objet <STRONG>Recordset</STRONG> actif (par exemple, un filtre qui ne donne aucun enregistrement correspondant).</span><span class="sxs-lookup"><span data-stu-id="0b6f5-116">Specifying <STRONG>adAffectGroup</STRONG> as the value for this parameter will result in an error when there are no visible records in the current <STRONG>Recordset</STRONG> (such as a filter for which no records match).</span></span></P>



<span data-ttu-id="0b6f5-p103">Si la transmission des modifications échoue pour un ou tous les enregistrements en raison d’un conflit avec les données sous-jacentes (par exemple, un enregistrement déjà supprimé par un autre utilisateur), le fournisseur renvoie des avertissements dans la collection [Errors](errors-collection-ado.md) et une erreur d’exécution est générée. Utilisez les propriétés [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) et [Status](status-property-ado-recordset.md) pour rechercher les enregistrements à l’origine de conflits.</span><span class="sxs-lookup"><span data-stu-id="0b6f5-p103">If the attempt to transmit changes fails for any or all records because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="0b6f5-119">Pour annuler les mises à jour par lot en attente, utilisez la méthode [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0b6f5-119">To cancel all pending batch updates, use the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="0b6f5-120">Si les propriétés dynamiques [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) et [Update Resync](update-resync-property-dynamic-ado.md) sont définies et que l'objet **Recordset** est le résultat de l'exécution d'une opération JOIN sur plusieurs tables, l'exécution de la méthode **UpdateBatch** est implicitement suivie par la méthode [Resync](resync-method-ado.md) en fonction des paramètres définis dans la propriété **Update Resync**.</span><span class="sxs-lookup"><span data-stu-id="0b6f5-120">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Update Resync](update-resync-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the execution of the **UpdateBatch** method is implicitly followed by the [Resync](resync-method-ado.md) method depending on the settings of the **Update Resync** property.</span></span>

<span data-ttu-id="0b6f5-p104">L'ordre dans lequel les mises à jour individuelles d'un lot sont effectuées sur la source de données ne correspond pas forcément à celui de leur exécution dans l'objet **Recordset** local. L'ordre de mises à jour dépend du fournisseur. Ne l'oubliez pas lorsque vous codez des mises à jour associées entre elles, comme des contraintes de clé externe en cas d'insertion ou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0b6f5-p104">The order in which the individual updates of a batch are performed on the data source is not necessarily the same as the order in which they were performed on the local **Recordset**. Update order is dependent upon the provider. Take this into account when coding updates that are related to one another, such as foreign key constraints on an insert or update.</span></span>

