---
title: Status, propriété (Recordset ADO)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 396188dcd959b229f7f7a58ccafb76b00508aa49
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944234"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="f33e8-102">Status, propriété (Recordset ADO)</span><span class="sxs-lookup"><span data-stu-id="f33e8-102">Status property (ADO Recordset)</span></span>


<span data-ttu-id="f33e8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f33e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f33e8-104">Indique l'état de l'enregistrement actuel en ce qui concerne des mises à jour par lots ou autres opérations en bloc.</span><span class="sxs-lookup"><span data-stu-id="f33e8-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

## <a name="return-value"></a><span data-ttu-id="f33e8-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f33e8-105">Return value</span></span>

<span data-ttu-id="f33e8-106">Renvoie la somme d'une ou de plusieurs valeurs [RecordStatusEnum](recordstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="f33e8-106">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f33e8-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f33e8-107">Remarks</span></span>

<span data-ttu-id="f33e8-p101">Utilisez la propriété **Status** pour connaître les modifications en attente sur les enregistrements modifiés lors de la mise à jour par lot. Vous pouvez aussi utiliser la propriété **Status** pour consulter l'état des enregistrements sur lesquels les opérations en bloc ont échoué, par exemple après avoir appelé les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md) ou définissez la propriété [Filter](filter-property-ado.md) d'un objet **Recordset** sur un tableau de signets. Avec cette propriété, vous pouvez déterminer pourquoi une opération a échoué sur un enregistrement donné et résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="f33e8-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

