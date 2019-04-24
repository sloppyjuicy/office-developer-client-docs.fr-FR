---
title: Appel de QueryRows pour les tables de petite taille
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331631"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="24712-103">Appel de QueryRows pour les tables de petite taille</span><span class="sxs-lookup"><span data-stu-id="24712-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="24712-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24712-105">Lors de l'extraction de lignes d'une petite table, appelez [IMAPITable:: QueryRows](imapitable-queryrows.md) au lieu de commencer par créer une restriction.</span><span class="sxs-lookup"><span data-stu-id="24712-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="24712-106">La création d'une restriction a un impact sur les performances, car le fournisseur doit d'abord créer une table, trouver les lignes correspondantes dans la table d'origine, puis copier les lignes dans le nouveau tableau.</span><span class="sxs-lookup"><span data-stu-id="24712-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="24712-107">Si le nombre total de lignes dans le tableau est inférieur à 100, il est probablement plus efficace de lire toutes les lignes, puis de faire appel à la fonction [IMAPITable:: FindRow](imapitable-findrow.md) pour trouver la ligne appropriée.</span><span class="sxs-lookup"><span data-stu-id="24712-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="24712-108">Il s'agit d'une stratégie particulièrement intéressante si ces informations ne sont nécessaires qu'occasionnellement.</span><span class="sxs-lookup"><span data-stu-id="24712-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="24712-109">Le moment approprié pour utiliser une restriction est lorsque les informations restreintes ou filtrées seront utilisées sur une période plus longue ou fréquemment utilisées.</span><span class="sxs-lookup"><span data-stu-id="24712-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="24712-110">Par exemple, si vous avez toujours besoin d'une vue avec des messages non lus, une restriction est l'appel approprié à utiliser.</span><span class="sxs-lookup"><span data-stu-id="24712-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

