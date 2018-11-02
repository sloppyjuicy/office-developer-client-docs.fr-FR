---
title: InternetTimeout, propriété (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1287289de5ef303e41a342ef84822d3a14083470
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918806"
---
# <a name="internettimeout-property-rds"></a>InternetTimeout, propriété (RDS)


**S’applique à**: Access 2013, Office 2013

Indique le nombre de millisecondes s'écoulant avant l'expiration d'une requête.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **Long** qui représente le nombre de millisecondes s'écoulant avant l'expiration d'une requête.

## <a name="remarks"></a>Remarques

Cette propriété s'applique exclusivement aux requêtes envoyées avec les protocoles HTTP ou HTTPS.

Dans un environnement à trois niveaux, l'exécution des requêtes peut prendre plusieurs minutes. Utilisez cette propriété pour accorder du temps supplémentaire pour aux requêtes longues.

