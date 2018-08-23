---
title: Définition d’une position de table avec un filtre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6c4db9c67fc712143657fe66b86ea33ef2b9c272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565591"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="6c90b-103">Définition d’une position de table avec un filtre</span><span class="sxs-lookup"><span data-stu-id="6c90b-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="6c90b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c90b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c90b-105">Les utilisateurs de tableau peuvent déplacer le curseur à une ligne qui correspond à un ensemble de critères de filtre.</span><span class="sxs-lookup"><span data-stu-id="6c90b-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="6c90b-106">Filtres peuvent reposer sur un grand nombre d’instructions telles que les valeurs de propriété de colonne, les masques de bits ou les sous-objets.</span><span class="sxs-lookup"><span data-stu-id="6c90b-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="6c90b-107">Les filtres sont spécifiés dans MAPI à l’aide d’une structure [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="6c90b-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="6c90b-108">**Pour positionner un tableau à la première ligne qui établit une correspondance avec les critères définis dans une restriction**</span><span class="sxs-lookup"><span data-stu-id="6c90b-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="6c90b-109">Appelez la méthode [IMAPITable::FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="6c90b-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="6c90b-110">**FindRow** commençant par la ligne représentée par un signet particulier, recherche dans une direction avancer ou reculer pour localiser une ligne qui correspond aux critères spécifiés dans la restriction.</span><span class="sxs-lookup"><span data-stu-id="6c90b-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="6c90b-111">**FindRow** peut être utile pour l’implémentation d’une barre de défilement est basée sur des chaînes de caractères, au lieu des fractions.</span><span class="sxs-lookup"><span data-stu-id="6c90b-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="6c90b-112">Par exemple, un client peut appeler la mise en œuvre de MAPI de **FindRow** lors de la recherche par le biais du carnet d’adresses intégré pour permettre à un utilisateur, en entrant un ou plusieurs caractères, pour rechercher le premier nom commence par les caractères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="6c90b-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6c90b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c90b-113">See also</span></span>



[<span data-ttu-id="6c90b-114">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="6c90b-114">MAPI Tables</span></span>](mapi-tables.md)

