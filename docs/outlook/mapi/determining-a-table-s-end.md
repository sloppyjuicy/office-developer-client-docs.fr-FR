---
title: Détermination de la fin d’une table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420086"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="cff3b-103">Détermination de la fin d’une table</span><span class="sxs-lookup"><span data-stu-id="cff3b-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="cff3b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cff3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="cff3b-105">Une erreur courante consiste à supposer que la fin du tableau a été atteinte dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="cff3b-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="cff3b-106">[IMAPITable::QueryRows](imapitable-queryrows.md) a été appelé dans une boucle, avec la fin de la boucle déterminée par le nombre de lignes renvoyé par [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span><span class="sxs-lookup"><span data-stu-id="cff3b-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="cff3b-107">Le nombre que **GetRowCount renvoie** ne représente pas toujours le nombre exact de lignes dans le tableau ; il s’agit d’un nombre approximatif.</span><span class="sxs-lookup"><span data-stu-id="cff3b-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="cff3b-108">**QueryRows a** été appelé avec un nombre fixe de lignes et moins de lignes sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="cff3b-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="cff3b-109">Ce n’est qu’après que **QueryRows** renvoie un jeu de lignes avec un nombre de lignes égal à zéro qu’il n’y a plus de lignes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cff3b-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="cff3b-110">La seule fois qu’un appelant peut supposer que le curseur est positionné à la fin du tableau pour un nombre de lignes positif ou au début du tableau pour un nombre de lignes négatif, c’est lorsque la valeur S_OK et zéro lignes sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="cff3b-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="cff3b-111">La valeur MAPI_E_NOT_FOUND n’est jamais renvoyée.</span><span class="sxs-lookup"><span data-stu-id="cff3b-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cff3b-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cff3b-112">See also</span></span>



[<span data-ttu-id="cff3b-113">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="cff3b-113">MAPI Tables</span></span>](mapi-tables.md)

