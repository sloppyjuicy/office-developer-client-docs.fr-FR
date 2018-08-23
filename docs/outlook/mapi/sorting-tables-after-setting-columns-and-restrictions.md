---
title: Tri des tables après la définition des colonnes et des restrictions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9f975ed1b9036bce5ed225b2a9020262260f4f57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572143"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="284dc-103">Tri des tables après la définition des colonnes et des restrictions</span><span class="sxs-lookup"><span data-stu-id="284dc-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="284dc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="284dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="284dc-105">Lorsque vous avez besoin limiter l’affichage d’une table triée, constituent les appels **IMAPITable** suivants dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="284dc-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="284dc-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir l’ensemble de la colonne.</span><span class="sxs-lookup"><span data-stu-id="284dc-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="284dc-107">[IMAPITable](imapitable-restrict.md) pour imposer la restriction.</span><span class="sxs-lookup"><span data-stu-id="284dc-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="284dc-108">[IMAPITable::SortTable](imapitable-sorttable.md) pour effectuer le tri.</span><span class="sxs-lookup"><span data-stu-id="284dc-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="284dc-109">Si le tableau trié est classé, passer un appel à [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), si nécessaire, après l’appel de **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="284dc-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="284dc-110">Ce classement d’appels est important parce que la plupart des fournisseurs de services de trier un tableau en tant que la dernière tâche pour optimiser les performances.</span><span class="sxs-lookup"><span data-stu-id="284dc-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="284dc-111">Si, par exemple, un fournisseur de magasin de message doit classer un tableau contenu de dossier avant une restriction peut être imposée, cette catégorisation est supprimée lors du traitement de la restriction.</span><span class="sxs-lookup"><span data-stu-id="284dc-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="284dc-112">Une deuxième catégorisation est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="284dc-112">A second categorization will be necessary.</span></span> 
  

