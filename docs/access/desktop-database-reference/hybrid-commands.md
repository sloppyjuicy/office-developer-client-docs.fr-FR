---
title: Commandes hybrides (référence de base de données de bureau Access)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7c7768ab15659abcf1ab49cb03524f4871616740
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552827"
---
# <a name="hybrid-commands"></a>Commandes hybrides


**S’applique à** : Access 2013, Office 2013

Les commandes hybrides sont des commandes partiellement paramétrées. Par exemple :

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

Le comportement de mise en cache d'une commande hybride est identique à celui des commandes paramétrées standard.

