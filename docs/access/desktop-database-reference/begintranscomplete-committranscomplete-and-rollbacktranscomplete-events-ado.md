---
title: BeginTransComplete, CommitTransComplete, RollbackTransComplete,, événements (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6f86e17a44ec0813176a023a02710fded627488
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296821"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>Événements BeginTransComplete, CommitTransComplete et RollbackTransComplete, (ADO)

**S’applique à** : Access 2013, Office 2013

Ces événements sont appelés une fois l’opération associée à l’objet [Connection](connection-object-ado.md) terminée.

- **BeginTransComplete** est appelé après l’opération [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

- **CommitTransComplete** est appelé après l’opération [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

- **RollbackTransComplete** est appelé après l’opération [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md).

## <a name="syntax"></a>Syntaxe

BeginTransComplete*TransactionLevel*, *perror*, ** adStatus, *pConnection*

CommitTransComplete*perror*, ** adStatus, *pConnection*

RollbackTransComplete,*perror*, ** adStatus, *pConnection*

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*TransactionLevel* |Valeur de type **Long** contenant le nouveau niveau de transaction de l'événement **BeginTrans** qui a provoqué l'événement.|
|*pError* |Objet [Error](error-object-ado.md). Elle décrit l'erreur qui s'est produite si la valeur de EventStatusEnum est **adStatusErrorsOccurred**; Sinon, il n'est pas défini.|
|*Statu* |[EventStatusEnum](eventstatusenum.md). Ces événements peuvent empêcher la génération de notifications ultérieures en définissant ce paramètre à **adStatusUnwantedEvent** avant que l'événement soit retourné.|
|*pConnection* |Objet **Connection** pour lequel l'événement s'est produit.|

## <a name="remarks"></a>Remarques

En Visual C++, plusieurs objets **Connection** peuvent partager la même méthode de gestion des événements. Celle-ci utilise l'objet **Connection** retourné pour identifier l'objet à l'origine de l'événement.

Si la propriété [Attributes](attributes-property-ado.md) a la valeur **adXactCommitRetaining** ou **adXactAbortRetaining**, une nouvelle transaction est lancée après la validation ou la restauration d'une transaction. Utilisez l'événement **BeginTransComplete** pour ignorer tous les événements de début de transaction à l'exception du premier.

