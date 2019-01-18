---
title: onError, événement (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712175"
---
# <a name="onerror-event-rds"></a>onError, événement (RDS)

**S’applique à**: Access 2013, Office 2013

L'événement **onError** est appelé chaque fois qu'une erreur se produit pendant une opération.

## <a name="syntax"></a>Syntaxe

onError*SCode*, *Description*, *Source*, *CancelDisplay*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*SCode* |Entier indiquant le code d'état de l'erreur.|
|*Description* |Valeur de type **String** reprenant une description de l'erreur.|
|*Source* |Valeur de type **String** indiquant la requête ou la commande à l'origine de l'erreur.|
|*CancelDisplay* |Valeur de type **Boolean**. Si la valeur est **True**, l'erreur n'est pas affichée dans une boîte de dialogue.|

