---
title: Commandes hybrides (référence de base de données du bureau Access)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 046d005eb4a9e1c8097908e0104b8d1e5c76e2af
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946911"
---
# <a name="hybrid-commands"></a>Commandes hybrides


**S’applique à**: Access 2013, Office 2013

Les commandes hybrides sont des commandes partiellement paramétrées. Par exemple :

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

Le comportement de mise en cache d'une commande hybride est identique à celui des commandes paramétrées standard.

