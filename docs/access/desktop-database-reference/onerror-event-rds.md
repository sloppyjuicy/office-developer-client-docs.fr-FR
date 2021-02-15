---
title: événement onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288475"
---
# <a name="onerror-event-rds"></a>événement onError (RDS)

**S’applique à** : Access 2013, Office 2013

L'événement **onError** est appelé chaque fois qu'une erreur se produit pendant une opération.

## <a name="syntax"></a>Syntaxe

onError *SCode*, *Description*, *Source*, *CancelDisplay*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*SCode* |Entier indiquant le code d'état de l'erreur.|
|*Description* |Valeur de type **String** reprenant une description de l'erreur.|
|*Source* |Valeur de type **String** indiquant la requête ou la commande à l'origine de l'erreur.|
|*CancelDisplay* |Valeur de type **Boolean**. Si la valeur est **True**, l'erreur n'est pas affichée dans une boîte de dialogue.|

