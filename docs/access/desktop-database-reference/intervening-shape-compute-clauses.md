---
title: Clauses de forme COMPUTE intermédiaires
TOCTitle: Intervening Shape COMPUTE clauses
ms:assetid: 3e9dcef2-776c-0365-4a92-68e325f7dbb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249174(v=office.15)
ms:contentKeyID: 48544380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f8edc3b1e873234b04eca0feb7a4e9c36e71e9c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945879"
---
# <a name="intervening-shape-compute-clauses"></a>Clauses de forme COMPUTE intermédiaires


**S’applique à**: Access 2013, Office 2013

Vous pouvez intégrer une ou plusieurs clauses COMPUTE entre le parent et l'enfant dans une commande de mise en forme paramétrée, comme illustré dans l'exemple suivant :

```vb 
 
SHAPE {select au_lname, state from authors} APPEND 
 ((SHAPE 
 (SHAPE 
 {select * from authors where state = ?} rs 
 COMPUTE rs, ANY(rs.state) state, ANY(rs.au_lname) au_lname 
 BY au_id) rs2 
 COMPUTE rs2, ANY(rs2.state) BY au_lname) 
RELATE state TO PARAMETER 0) 
```

