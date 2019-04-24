---
title: Détermination de la fin d'une table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316715"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="59710-103">Détermination de la fin d'une table</span><span class="sxs-lookup"><span data-stu-id="59710-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="59710-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59710-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="59710-105">Une erreur courante consiste à supposer que la fin de la table a été atteinte dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="59710-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="59710-106">[IMAPITable:: QueryRows](imapitable-queryrows.md) a été appelé dans une boucle, avec la fin de la boucle déterminée par le nombre de lignes renvoyé par la méthode [IMAPITable:: GetRowCount](imapitable-getrowcount.md).</span><span class="sxs-lookup"><span data-stu-id="59710-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="59710-107">Le nombre renvoyé par **GetRowCount** ne représente pas toujours le nombre exact de lignes dans le tableau; Il s'agit d'un nombre approximatif.</span><span class="sxs-lookup"><span data-stu-id="59710-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="59710-108">**QueryRows** a été appelé avec un nombre fixe de lignes et moins de lignes sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="59710-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="59710-109">Il n'est pas jusqu'à ce que **QueryRows** renvoie un jeu de lignes dont le nombre de lignes est égal à zéro, il n'y a plus de lignes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="59710-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="59710-110">Le seul moment où un appelant peut supposer que le curseur est positionné à la fin de la table pour un nombre positif de lignes ou au début de la table pour un nombre de lignes négatif est lorsque la valeur S_OK et zéro ligne sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="59710-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="59710-111">La valeur MAPI_E_NOT_FOUND n'est jamais renvoyée.</span><span class="sxs-lookup"><span data-stu-id="59710-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59710-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59710-112">See also</span></span>



[<span data-ttu-id="59710-113">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="59710-113">MAPI Tables</span></span>](mapi-tables.md)

