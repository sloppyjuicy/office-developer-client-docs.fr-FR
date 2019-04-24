---
title: Status, propriété (Recordset ADO)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4017ff216c17479a69d6d07d0abe51b30fd5e680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308518"
---
# <a name="status-property-ado-recordset"></a>Status, propriété (Recordset ADO)


**S’applique à** : Access 2013, Office 2013

Indique l'état de l'enregistrement actuel en ce qui concerne des mises à jour par lots ou autres opérations en bloc.

## <a name="return-value"></a>Valeur renvoyée

Renvoie la somme d’une ou de plusieurs valeurs [RecordStatusEnum](recordstatusenum.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Status** pour connaître les modifications en attente sur les enregistrements modifiés lors de la mise à jour par lot. Vous pouvez aussi utiliser la propriété **Status** pour consulter l’état des enregistrements sur lesquels les opérations en bloc ont échoué, par exemple après avoir appelé les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md) ou définissez la propriété [Filter](filter-property-ado.md) d’un objet **Recordset** sur un tableau de signets. Avec cette propriété, vous pouvez déterminer pourquoi une opération a échoué sur un enregistrement donné et résoudre le problème.

