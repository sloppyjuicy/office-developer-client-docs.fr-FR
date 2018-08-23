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
ms.openlocfilehash: 34975677bedccf3f9111985d371e21d482b45584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589335"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="96aa8-103">Appel de QueryRows pour les petites tables</span><span class="sxs-lookup"><span data-stu-id="96aa8-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="96aa8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96aa8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96aa8-105">Lors de l’extraction des lignes d’une table de petite taille, appel [IMAPITable::QueryRows](imapitable-queryrows.md) au lieu de la première création d’une restriction.</span><span class="sxs-lookup"><span data-stu-id="96aa8-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="96aa8-106">Création d’une restriction affecte les performances, car le fournisseur doit d’abord créer un tableau, recherchez les lignes correspondantes dans la table d’origine et puis copiez les lignes à la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="96aa8-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="96aa8-107">Si le nombre total de lignes dans le tableau est inférieure à 100, il est probablement plus efficace lire toutes les lignes et ensuite appeler [IMAPITable::FindRow](imapitable-findrow.md) pour trouver la ligne adéquate.</span><span class="sxs-lookup"><span data-stu-id="96aa8-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="96aa8-108">Il s’agit d’une stratégie particulièrement si ces informations sont nécessaires seulement occasionnellement.</span><span class="sxs-lookup"><span data-stu-id="96aa8-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="96aa8-109">Moment propice pour utiliser une restriction est lorsque les informations restreintes ou filtrées seront utilisées sur une période plus longue ou fréquemment utilisées.</span><span class="sxs-lookup"><span data-stu-id="96aa8-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="96aa8-110">Par exemple, si vous avez toujours besoin d’un affichage avec des messages non lus, une restriction est l’appel appropriée à utiliser.</span><span class="sxs-lookup"><span data-stu-id="96aa8-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

