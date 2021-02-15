---
title: ConnectComplete and Disconnect events (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295988"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>ConnectComplete and Disconnect events (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **ConnectComplete** est appelé après l'*établissement* d'une connexion. L'événement **Disconnect** est pour sa part appelé à la *fin* de la connexion.

## <a name="syntax"></a>Syntaxe

ConnectComplete *pError*, *adStatus*, *pConnection*

Disconnect *adStatus*, *pConnection*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque **ConnectComplete** est appelé, ce paramètre est défini à **adStatusCancel** si un événement **WillConnect** a demandé l'annulation de la connexion en attente.<br/><br/>Avant qu'un de ces événements soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure. Notez toutefois que ces événements sont à nouveau générés si vous fermez et rouvrez l'objet [Connection](connection-object-ado.md).|
|*pConnection* |Objet **Connection** auquel l'événement se rapporte.|

