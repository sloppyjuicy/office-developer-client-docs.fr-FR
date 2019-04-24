---
title: Définition d'une position de table avec un filtre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d66124b-a018-4db4-b55b-a0e5ed467e14
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6b21d6746baf438af438787d966d9af886d4a74f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316043"
---
# <a name="setting-a-table-position-with-a-filter"></a><span data-ttu-id="16fb1-103">Définition d'une position de table avec un filtre</span><span class="sxs-lookup"><span data-stu-id="16fb1-103">Setting a Table Position with a Filter</span></span>

  
  
<span data-ttu-id="16fb1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16fb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16fb1-105">Tableau les utilisateurs peuvent déplacer le curseur vers une ligne qui correspond à un ensemble de critères de filtre.</span><span class="sxs-lookup"><span data-stu-id="16fb1-105">Table users can move the cursor to a row that matches a set of filter criteria.</span></span> <span data-ttu-id="16fb1-106">Les filtres peuvent être basés sur diverses instructions, telles que des valeurs de propriété de colonne, des masques de réplication ou des sous-objets.</span><span class="sxs-lookup"><span data-stu-id="16fb1-106">Filters can be based on a variety of guidelines such as column property values, bitmasks, or subobjects.</span></span> <span data-ttu-id="16fb1-107">Les filtres sont spécifiés dans MAPI à l'aide d'une structure [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="16fb1-107">Filters are specified in MAPI using an [SRestriction](srestriction.md) structure.</span></span> 
  
 <span data-ttu-id="16fb1-108">**Positionnement d'une table sur la première ligne correspondant aux critères établis dans une restriction**</span><span class="sxs-lookup"><span data-stu-id="16fb1-108">**To position a table to the first row that matches the criteria established in a restriction**</span></span>
  
- <span data-ttu-id="16fb1-109">Appelez la méthode [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="16fb1-109">Call the [IMAPITable::FindRow](imapitable-findrow.md) method.</span></span> <span data-ttu-id="16fb1-110">En commençant par la ligne représentée par un signet particulier, **FindRow** recherche dans une direction vers l'avant ou vers l'arrière pour trouver une ligne qui correspond aux critères spécifiés dans la restriction.</span><span class="sxs-lookup"><span data-stu-id="16fb1-110">Starting with the row represented by a particular bookmark, **FindRow** searches in either a forward or backward direction to locate a row that matches the criteria specified in the restriction.</span></span> <span data-ttu-id="16fb1-111">**FindRow** peut être utile pour implémenter une barre de défilement basée sur des chaînes de caractères, au lieu de valeurs fractionnaires.</span><span class="sxs-lookup"><span data-stu-id="16fb1-111">**FindRow** can be useful for implementing a scroll bar that is based on character strings, instead of fractional values.</span></span> <span data-ttu-id="16fb1-112">Par exemple, un client peut appeler la mise en œuvre de **FindRow** par MAPI lors de la recherche dans le carnet d'adresses intégré pour permettre à un utilisateur, en entrant un ou plusieurs caractères, de localiser le prénom qui commence par les caractères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="16fb1-112">For example, a client can call MAPI's implementation of **FindRow** when searching through the integrated address book to enable a user, by entering one or more characters, to locate the first name that begins with the specified characters.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="16fb1-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16fb1-113">See also</span></span>



[<span data-ttu-id="16fb1-114">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="16fb1-114">MAPI Tables</span></span>](mapi-tables.md)

