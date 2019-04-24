---
title: Définition de la position de la table avec une valeur fractionnaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339262"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="c4318-103">Définition de la position de la table avec une valeur fractionnaire</span><span class="sxs-lookup"><span data-stu-id="c4318-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="c4318-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4318-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4318-105">Tableau les utilisateurs peuvent passer à une position qui représente un pourcentage approximatif de lignes par rapport au total.</span><span class="sxs-lookup"><span data-stu-id="c4318-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="c4318-106">Au lieu de passer à une ligne exacte, cette méthode de positionnement divise le tableau en portions en fonction de fractions.</span><span class="sxs-lookup"><span data-stu-id="c4318-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="c4318-107">Tableau les utilisateurs peuvent déplacer, par exemple, vers le point de la moitié d'un tableau ou vers la ligne 7/8 du tableau.</span><span class="sxs-lookup"><span data-stu-id="c4318-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="c4318-108">**Pour déplacer le curseur d'un nombre approximatif de lignes**</span><span class="sxs-lookup"><span data-stu-id="c4318-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="c4318-109">Appeler [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="c4318-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="c4318-110">**SeekRowApprox** passe à la ligne qui représente un pourcentage particulier de lignes par rapport au début de la table.</span><span class="sxs-lookup"><span data-stu-id="c4318-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="c4318-111">Ce pourcentage est spécifié dans les paramètres _ulNumerator_ et _ulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="c4318-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="c4318-112">**SeekRowApprox** est fréquemment utilisé pour implémenter des barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="c4318-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="c4318-113">**Pour déterminer la position approximative d'une table**</span><span class="sxs-lookup"><span data-stu-id="c4318-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="c4318-114">Appeler [IMAPITable:: QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="c4318-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="c4318-115">**QueryPosition** peut être utilisé pour informer l'utilisateur de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="c4318-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="c4318-116">Il définit une valeur fractionnaire basée sur le nombre de lignes du tableau et le numéro de la ligne active.</span><span class="sxs-lookup"><span data-stu-id="c4318-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="c4318-117">Attendez que cette valeur représente une approximation.</span><span class="sxs-lookup"><span data-stu-id="c4318-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="c4318-118">Les implémenteurs de tableaux sont encouragés à ne pas calculer la position exacte, car les implémentations précises peuvent être coûteuses à appeler, en particulier dans les tables catégorisées.</span><span class="sxs-lookup"><span data-stu-id="c4318-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c4318-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4318-119">See also</span></span>



[<span data-ttu-id="c4318-120">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="c4318-120">MAPI Tables</span></span>](mapi-tables.md)

