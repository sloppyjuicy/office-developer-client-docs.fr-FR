---
title: BeginTransComplete, CommitTransComplete, RollbackTransComplete, événements (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 216f5a92ea4095d78b8df2b196a1607e40ae58d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472428"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>BeginTransComplete, CommitTransComplete et RollbackTransComplete, événements (ADO)


**S’applique à**: Access 2013 | Office 2013


Ces événements sont appelés une fois l'opération associée à l'objet [Connection](connection-object-ado.md) terminée.

  - **BeginTransComplete** est appelé après l'opération [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

  - **CommitTransComplete** est appelé après l'opération [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

  - **RollbackTransComplete** est appelé après l'opération [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

## <a name="syntax"></a>Syntaxe

De le BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*

CommitTransComplete*pError*, *adStatus*, *pConnection*

RollbackTransComplete*pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Paramètres

  - *TransactionLevel*

  - Valeur de type **Long** contenant le nouveau niveau de transaction de l'événement **BeginTrans** qui a provoqué l'événement.

  - *pError*

  - Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si EventStatusEnum a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Ces événements peuvent empêcher la génération de notifications ultérieures en définissant ce paramètre à **adStatusUnwantedEvent** avant que l'événement soit retourné.

  - *pConnection*

  - Objet **Connection** pour lequel l'événement s'est produit.

## <a name="remarks"></a>Notes

En Visual C++, plusieurs objets **Connection** peuvent partager la même méthode de gestion des événements. Celle-ci utilise l'objet **Connection** retourné pour identifier l'objet à l'origine de l'événement.

Si la propriété [Attributes](attributes-property-ado.md) a la valeur **adXactCommitRetaining** ou **adXactAbortRetaining**, une nouvelle transaction est lancée après la validation ou la restauration d'une transaction. Utilisez l'événement **BeginTransComplete** pour ignorer tous les événements de début de transaction à l'exception du premier.

