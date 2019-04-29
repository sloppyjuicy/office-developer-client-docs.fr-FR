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
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409880"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="7fe1d-103">Tri des tables après la définition des colonnes et des restrictions</span><span class="sxs-lookup"><span data-stu-id="7fe1d-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="7fe1d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fe1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fe1d-105">Lorsque vous devez limiter l'affichage d'un tableau trié, effectuez toujours les appels **IMAPITable** suivants dans l'ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="7fe1d-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="7fe1d-106">[IMAPITable:: SetColumns](imapitable-setcolumns.md) pour définir le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="7fe1d-107">[IMAPITable:: restreindre](imapitable-restrict.md) pour imposer la restriction.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="7fe1d-108">[IMAPITable:: SortTable](imapitable-sorttable.md) pour effectuer le tri.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="7fe1d-109">Si le tableau trié est classé, effectuez un appel à [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md), si nécessaire, après l'appel de **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="7fe1d-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="7fe1d-110">Cette classification des appels est importante, car la plupart des fournisseurs de services trient un tableau en tant que dernière tâche pour obtenir les meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="7fe1d-111">Si, par exemple, un fournisseur de banque de messages doit catégoriser une table de contenu de dossier avant qu'une restriction puisse être imposée, cette catégorisation sera supprimée lors du traitement de la restriction.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="7fe1d-112">Une deuxième catégorisation sera nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-112">A second categorization will be necessary.</span></span> 
  

