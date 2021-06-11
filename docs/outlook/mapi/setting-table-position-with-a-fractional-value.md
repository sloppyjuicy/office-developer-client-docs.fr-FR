---
title: Définition de la position du tableau avec une valeur fractionnaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437335"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="5ee2b-103">Définition de la position du tableau avec une valeur fractionnaire</span><span class="sxs-lookup"><span data-stu-id="5ee2b-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="5ee2b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ee2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ee2b-105">Les utilisateurs de tableau peuvent se déplacer vers une position qui représente un pourcentage approximatif de lignes par rapport au total.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="5ee2b-106">Plutôt que de passer à une ligne exacte, cette méthode de positionnement divise le tableau en parties en fractions.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="5ee2b-107">Les utilisateurs de tableau peuvent, par exemple, se déplacer vers le point à mi-chemin d’un tableau ou vers la ligne qui se trouve à 7/8 du chemin du tableau.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="5ee2b-108">**Pour déplacer le curseur un nombre approximatif de lignes**</span><span class="sxs-lookup"><span data-stu-id="5ee2b-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="5ee2b-109">Appelez [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="5ee2b-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="5ee2b-110">**SeekRowApprox** se déplace vers la ligne qui représente un pourcentage particulier de lignes par rapport au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="5ee2b-111">Ce pourcentage est spécifié dans les _paramètres ulNumerator_ et _ulDenominator._</span><span class="sxs-lookup"><span data-stu-id="5ee2b-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="5ee2b-112">**SeekRowApprox est fréquemment utilisé** pour implémenter des barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="5ee2b-113">**Pour déterminer la position approximative d’un tableau**</span><span class="sxs-lookup"><span data-stu-id="5ee2b-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="5ee2b-114">Appelez [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="5ee2b-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="5ee2b-115">**QueryPosition peut** être utilisé pour informer l’utilisateur de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="5ee2b-116">Il définit une valeur fractionnaire en fonction du nombre de lignes du tableau et du numéro de la ligne actuelle.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="5ee2b-117">Attendez-vous à ce que cette valeur représente une estimation.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="5ee2b-118">Les implémenteurs de tableau sont encouragés à ne pas calculer la position exacte, car les implémentations précises peuvent être coûteuses à appeler, en particulier sur les tableaux catégorisés.</span><span class="sxs-lookup"><span data-stu-id="5ee2b-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5ee2b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ee2b-119">See also</span></span>



[<span data-ttu-id="5ee2b-120">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="5ee2b-120">MAPI Tables</span></span>](mapi-tables.md)

