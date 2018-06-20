---
title: Position de la Table paramètre avec une valeur décimale
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 104de38a41408091a6fbb69995de4f41f6fea6a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787140"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="30b60-103">Position de la Table paramètre avec une valeur décimale</span><span class="sxs-lookup"><span data-stu-id="30b60-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="30b60-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30b60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30b60-105">Les utilisateurs de tableau peuvent déplacer vers une position qui représente un pourcentage approximatif de lignes par rapport au total.</span><span class="sxs-lookup"><span data-stu-id="30b60-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="30b60-106">Au lieu de passer à une ligne exacte, cette méthode de positionnement divise la table en portions basée sur des fractions.</span><span class="sxs-lookup"><span data-stu-id="30b60-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="30b60-107">Les utilisateurs de tableau peuvent déplacer, par exemple, à mi-chemin d’une table ou à la ligne qui est 7/8 de la façon dont la table.</span><span class="sxs-lookup"><span data-stu-id="30b60-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="30b60-108">**Pour déplacer le curseur du nombre de lignes approximatif**</span><span class="sxs-lookup"><span data-stu-id="30b60-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="30b60-109">Appelez [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span><span class="sxs-lookup"><span data-stu-id="30b60-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="30b60-110">**SeekRowApprox** se déplace sur la ligne qui représente un pourcentage de lignes par rapport au début de la table.</span><span class="sxs-lookup"><span data-stu-id="30b60-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="30b60-111">Ce pourcentage est spécifié dans les paramètres _ulNumerator_ et _ulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="30b60-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="30b60-112">**SeekRowApprox** est fréquemment utilisé pour implémenter des barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="30b60-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="30b60-113">**Pour déterminer la position approximative d’une table**</span><span class="sxs-lookup"><span data-stu-id="30b60-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="30b60-114">Appelez [IMAPITable::QueryPosition](imapitable-queryposition.md).</span><span class="sxs-lookup"><span data-stu-id="30b60-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="30b60-115">**QueryPosition** peut être utilisé pour informer l’utilisateur de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="30b60-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="30b60-116">Il définit une valeur décimale basée sur le nombre de lignes dans le tableau et le nombre de la ligne active.</span><span class="sxs-lookup"><span data-stu-id="30b60-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="30b60-117">Attendez que cette valeur représente une estimation.</span><span class="sxs-lookup"><span data-stu-id="30b60-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="30b60-118">L’implémentation de la table est encouragées ne pas à calculer la position exacte étant donné que les implémentations précises coûteuses à appeler, en particulier sur les tableaux, voir.</span><span class="sxs-lookup"><span data-stu-id="30b60-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="30b60-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30b60-119">See also</span></span>



[<span data-ttu-id="30b60-120">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="30b60-120">MAPI Tables</span></span>](mapi-tables.md)

