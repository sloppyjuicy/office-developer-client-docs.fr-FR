---
title: Status, propriété (objet Recordset ADO)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ce4e3fc2d879521bbe1bbdb34d203a640fbe06c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469356"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="459db-102">Status, propriété (objet Recordset ADO)</span><span class="sxs-lookup"><span data-stu-id="459db-102">Status Property (ADO Recordset)</span></span>


<span data-ttu-id="459db-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="459db-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="459db-104">Indique l'état de l'enregistrement actuel en ce qui concerne des mises à jour par lots ou autres opérations en bloc.</span><span class="sxs-lookup"><span data-stu-id="459db-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

## <a name="return-value"></a><span data-ttu-id="459db-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="459db-105">Return Value</span></span>

<span data-ttu-id="459db-106">Renvoie la somme d'une ou de plusieurs valeurs [RecordStatusEnum](recordstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="459db-106">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="459db-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="459db-107">Remarks</span></span>

<span data-ttu-id="459db-p101">Utilisez la propriété **Status** pour connaître les modifications en attente sur les enregistrements modifiés lors de la mise à jour par lot. Vous pouvez aussi utiliser la propriété **Status** pour consulter l'état des enregistrements sur lesquels les opérations en bloc ont échoué, par exemple après avoir appelé les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md) ou définissez la propriété [Filter](filter-property-ado.md) d'un objet **Recordset** sur un tableau de signets. Avec cette propriété, vous pouvez déterminer pourquoi une opération a échoué sur un enregistrement donné et résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="459db-p101">Use the **Status** property to see what changes are pending for records modified during batch updating. You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks. With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

