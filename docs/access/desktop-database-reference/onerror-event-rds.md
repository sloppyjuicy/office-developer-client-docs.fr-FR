---
title: événement onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49a9f5340ac12218ef2c1a85e9930566a147a3fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626259"
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

