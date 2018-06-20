---
title: Déterminer la fin d’une Table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7cbf11f16948d582ba36a0b4d20411549b723b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783156"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="52ad4-103">Déterminer la fin d’une Table</span><span class="sxs-lookup"><span data-stu-id="52ad4-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="52ad4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52ad4-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="52ad4-105">Une erreur fréquente consiste à supposent que la fin de la table a été atteinte lorsque :</span><span class="sxs-lookup"><span data-stu-id="52ad4-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="52ad4-106">[IMAPITable::QueryRows](imapitable-queryrows.md) a été appelée dans une boucle, à la fin de la boucle déterminée par le nombre de lignes renvoyé par [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span><span class="sxs-lookup"><span data-stu-id="52ad4-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="52ad4-107">Le nombre **GetRowCount** renvoie ne représente pas toujours le nombre exact de lignes de la table ; Il s’agit d’un nombre approximatif.</span><span class="sxs-lookup"><span data-stu-id="52ad4-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="52ad4-108">**QueryRows** a été appelée avec un nombre défini de lignes et moins de lignes sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="52ad4-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="52ad4-109">Il est pas **QueryRows** retourne une ligne avec un nombre de lignes égal à zéro qu’il n’y a plus aucune ligne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="52ad4-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="52ad4-110">La seule fois où un appelant peut supposer que le curseur est positionné à la fin de la table pour un nombre positif de lignes ou au début de la table pour un nombre de lignes négatif est lorsque la valeur S_OK et aucune ligne est renvoyés.</span><span class="sxs-lookup"><span data-stu-id="52ad4-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="52ad4-111">La valeur MAPI_E_NOT_FOUND n’est jamais retourné.</span><span class="sxs-lookup"><span data-stu-id="52ad4-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52ad4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52ad4-112">See also</span></span>



[<span data-ttu-id="52ad4-113">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="52ad4-113">MAPI Tables</span></span>](mapi-tables.md)

