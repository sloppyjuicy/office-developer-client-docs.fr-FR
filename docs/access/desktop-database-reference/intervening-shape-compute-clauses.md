---
title: Clauses COMPUTE de forme intermédiaires
TOCTitle: Intervening Shape COMPUTE clauses
ms:assetid: 3e9dcef2-776c-0365-4a92-68e325f7dbb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249174(v=office.15)
ms:contentKeyID: 48544380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 456729bb93d6cfaf2844d71123cd850d7f719844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291247"
---
# <a name="intervening-shape-compute-clauses"></a><span data-ttu-id="b7a2c-102">Clauses COMPUTE de forme intermédiaires</span><span class="sxs-lookup"><span data-stu-id="b7a2c-102">Intervening Shape COMPUTE clauses</span></span>


<span data-ttu-id="b7a2c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7a2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7a2c-104">Vous pouvez intégrer une ou plusieurs clauses COMPUTE entre le parent et l'enfant dans une commande de mise en forme paramétrée, comme illustré dans l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b7a2c-104">It is valid to embed one or more COMPUTE clauses between the parent and child in a parameterized shape command, as in the following example:</span></span>

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

