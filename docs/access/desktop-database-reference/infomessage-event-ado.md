---
title: Événement InfoMessage (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3a629511b87a182d659cba74de537edd15d27b5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631964"
---
# <a name="infomessage-event-ado"></a>Événement InfoMessage (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **InfoMessage** est appelé à chaque avertissement généré lors d'une opération **ConnectionEvent**.

## <a name="syntax"></a>Syntaxe

InfoMessage *pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*pError* |Objet [Error](error-object-ado.md). Ce paramètre contient toutes les erreurs générées lors de l'opération. Si plusieurs erreurs sont retournées, énumérez la collection **Errors** pour les identifier.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.|
|*pConnection* |Objet [Connection](connection-object-ado.md). Connexion pour laquelle l'avertissement a été émis. Par exemple, des avertissements peuvent être générés lors de l'ouverture d'un objet **Connection** ou pendant l'exécution d'un objet [Command](command-object-ado.md) sur un objet **Connection**.|

