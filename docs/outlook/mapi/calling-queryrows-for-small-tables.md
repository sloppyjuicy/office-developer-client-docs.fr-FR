---
title: Appel de QueryRows pour les petites tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404175"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="6d772-103">Appel de QueryRows pour les petites tables</span><span class="sxs-lookup"><span data-stu-id="6d772-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="6d772-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d772-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d772-105">Lorsque vous récupérez des lignes à partir d’une petite table, appelez [IMAPITable::QueryRows](imapitable-queryrows.md) au lieu de créer d’abord une restriction.</span><span class="sxs-lookup"><span data-stu-id="6d772-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="6d772-106">La création d’une restriction a un impact sur les performances, car le fournisseur doit d’abord créer une table, rechercher les lignes correspondantes dans la table d’origine, puis copier les lignes dans la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="6d772-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="6d772-107">Si le nombre total de lignes du tableau est inférieur à 100, il est probablement plus efficace de lire toutes les lignes, puis d’appeler [IMAPITable::FindRow](imapitable-findrow.md) pour trouver la ligne appropriée.</span><span class="sxs-lookup"><span data-stu-id="6d772-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="6d772-108">Il s’agit d’une stratégie particulièrement efficace si ces informations ne sont nécessaires qu’occasionnellement.</span><span class="sxs-lookup"><span data-stu-id="6d772-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="6d772-109">Le moment approprié pour utiliser une restriction est le moment où les informations restreintes ou filtrées sont utilisées sur une période plus longue ou fréquemment.</span><span class="sxs-lookup"><span data-stu-id="6d772-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="6d772-110">Par exemple, si vous avez toujours besoin d’un affichage avec des messages non lus, une restriction est l’appel approprié à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6d772-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

