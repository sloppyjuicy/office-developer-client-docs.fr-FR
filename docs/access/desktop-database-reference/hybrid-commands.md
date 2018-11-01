---
title: Commandes hybrides (référence de base de données du bureau Access)
TOCTitle: Hybrid Commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 363f305fee12cb2e46ab9d4c628030f7dc4bcd78
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873851"
---
# <a name="hybrid-commands"></a><span data-ttu-id="99a75-102">Commandes hybrides</span><span class="sxs-lookup"><span data-stu-id="99a75-102">Hybrid Commands</span></span>


<span data-ttu-id="99a75-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="99a75-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99a75-p101">Les commandes hybrides sont des commandes partiellement paramétrées. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="99a75-p101">Hybrid commands are partially parameterized commands. For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="99a75-106">Le comportement de mise en cache d'une commande hybride est identique à celui des commandes paramétrées standard.</span><span class="sxs-lookup"><span data-stu-id="99a75-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

