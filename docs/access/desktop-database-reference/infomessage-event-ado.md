---
title: InfoMessage, événement (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699897"
---
# <a name="infomessage-event-ado"></a>InfoMessage, événement (ADO)

**S’applique à**: Access 2013, Office 2013

L'événement **InfoMessage** est appelé à chaque avertissement généré lors d'une opération **ConnectionEvent**.

## <a name="syntax"></a>Syntaxe

InfoMessage*pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*pError* |Objet [Error](error-object-ado.md). Ce paramètre contient toutes les erreurs générées lors de l'opération. Si plusieurs erreurs sont retournées, énumérez la collection **Errors** pour les identifier.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.|
|*pConnection* |Objet [Connection](connection-object-ado.md). Connexion pour laquelle l'avertissement a été émis. Par exemple, des avertissements peuvent être générés lors de l'ouverture d'un objet **Connection** ou pendant l'exécution d'un objet [Command](command-object-ado.md) sur un objet **Connection**.|

