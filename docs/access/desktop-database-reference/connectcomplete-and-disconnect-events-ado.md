---
title: ConnectComplete and Disconnect events (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d46da971ed9cb59c83b91fbb12e2588c40685f47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602828"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>ConnectComplete and Disconnect events (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **ConnectComplete** est appelé après l'*établissement* d'une connexion. L'événement **Disconnect** est pour sa part appelé à la *fin* de la connexion.

## <a name="syntax"></a>Syntaxe

ConnectComplete *pError*, *adStatus*, *pConnection*

*Déconnecter adStatus*, *pConnection*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque **ConnectComplete** est appelé, ce paramètre est défini à **adStatusCancel** si un événement **WillConnect** a demandé l'annulation de la connexion en attente.<br/><br/>Avant qu'un de ces événements soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure. Notez toutefois que ces événements sont à nouveau générés si vous fermez et rouvrez l'objet [Connection](connection-object-ado.md).|
|*pConnection* |Objet **Connection** auquel l'événement se rapporte.|

