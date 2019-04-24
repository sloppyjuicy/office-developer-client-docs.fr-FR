---
title: Transmission et copie des propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356643"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="a5c31-103">Transmission et copie des propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="a5c31-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="a5c31-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5c31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5c31-105">Chaque fois qu'une propriété nommée est envoyée, déplacée ou copiée, le nom reste constant, mais l'identificateur doit être modifié pour adhérer au mappage de l'objet de destination.</span><span class="sxs-lookup"><span data-stu-id="a5c31-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="a5c31-106">La seule exception à cette règle est lorsque la source et la destination ont la même signature de mappage, ce qui rend superflu le remappage.</span><span class="sxs-lookup"><span data-stu-id="a5c31-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="a5c31-107">Il incombe au fournisseur de transport de remapper les noms des propriétés nommées transmises à des identificateurs appropriés qui fonctionnent à la destination.</span><span class="sxs-lookup"><span data-stu-id="a5c31-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="a5c31-108">Le fournisseur de transport d'envoi ne peut pas savoir quel mappage correct se trouve à la destination; il doit transmettre les noms et s'appuyer sur le fournisseur de transport de réception pour les mapper aux identificateurs qui fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="a5c31-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="a5c31-109">L'implémentation MAPI de TNEF gère le remappage des propriétés nommées pour les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="a5c31-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="a5c31-110">Les fournisseurs de transport peuvent gérer manuellement le remappage ou utiliser l'implémentation TNEF.</span><span class="sxs-lookup"><span data-stu-id="a5c31-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="a5c31-111">Un remappage similaire des propriétés nommées doit se produire lorsque ces propriétés sont copiées entre des magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="a5c31-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="a5c31-112">Toutefois, étant donné que les fournisseurs de banques de messages peuvent récupérer le mappage du nom au identificateur de la destination, ils peuvent remapper les propriétés immédiatement et ne pas avoir à se reposer sur la Banque de messages de destination.</span><span class="sxs-lookup"><span data-stu-id="a5c31-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5c31-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5c31-113">See also</span></span>



[<span data-ttu-id="a5c31-114">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="a5c31-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

