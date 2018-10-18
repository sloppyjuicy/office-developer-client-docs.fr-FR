---
title: Status, propriété (objet Recordset ADO)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1979ad721a01ef72c08da1531a8826ec320915e5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604616"
---
# <a name="status-property-ado-recordset"></a>Status, propriété (objet Recordset ADO)


**S’applique à**: Access 2013 | Office 2013

Indique l'état de l'enregistrement actuel en ce qui concerne des mises à jour par lots ou autres opérations en bloc.

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie la somme d'une ou de plusieurs valeurs [RecordStatusEnum](recordstatusenum.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Status** pour connaître les modifications en attente sur les enregistrements modifiés lors de la mise à jour par lot. Vous pouvez aussi utiliser la propriété **Status** pour consulter l'état des enregistrements sur lesquels les opérations en bloc ont échoué, par exemple après avoir appelé les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md) ou définissez la propriété [Filter](filter-property-ado.md) d'un objet **Recordset** sur un tableau de signets. Avec cette propriété, vous pouvez déterminer pourquoi une opération a échoué sur un enregistrement donné et résoudre le problème.

