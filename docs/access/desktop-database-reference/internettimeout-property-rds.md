---
title: InternetTimeout, propriété (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fb247396b5e7e65c9fbfe86ab4f06b6a69037522
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631936"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout, propriété (RDS)


**S’applique à** : Access 2013, Office 2013

Indique le nombre de millisecondes s'écoulant avant l'expiration d'une requête.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **Long** qui représente le nombre de millisecondes s'écoulant avant l'expiration d'une requête.

## <a name="remarks"></a>Remarques

Cette propriété s'applique exclusivement aux requêtes envoyées avec les protocoles HTTP ou HTTPS.

Dans un environnement à trois niveaux, l'exécution des requêtes peut prendre plusieurs minutes. Utilisez cette propriété pour accorder du temps supplémentaire pour aux requêtes longues.

