---
title: Transmission et copie des propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1c225712e354d72b79313ee4c3f36da55f11b0a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587515"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="42f6f-103">Transmission et copie des propriétés nommées</span><span class="sxs-lookup"><span data-stu-id="42f6f-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="42f6f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42f6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42f6f-105">Envoi d’une propriété nommée, déplacé ou copié, le nom reste constant, mais l’identificateur doit changer pour respecter le mappage de l’objet de destination.</span><span class="sxs-lookup"><span data-stu-id="42f6f-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="42f6f-106">La seule exception à cette règle est lors de la source et destination ont la même signature de mappage, rendant remappage inutile.</span><span class="sxs-lookup"><span data-stu-id="42f6f-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="42f6f-107">Il est de la responsabilité du fournisseur de transport pour remapper les noms des propriétés nommées transmises aux identificateurs appropriés qui fonctionnent à la destination.</span><span class="sxs-lookup"><span data-stu-id="42f6f-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="42f6f-108">Le fournisseur de transport envoi ne peut pas savoir quel est le mappage correct à la destination ; Il doit transmettre les noms et s’appuient sur le fournisseur de transport de réception pour les mapper aux identificateurs qui fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="42f6f-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="42f6f-109">L’implémentation MAPI du format TNEF gère la reconfiguration des propriétés nommées fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="42f6f-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="42f6f-110">Fournisseurs de transport peuvent gérer le remappage manuellement ou utiliser la mise en œuvre TNEF.</span><span class="sxs-lookup"><span data-stu-id="42f6f-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="42f6f-111">Un remappage similaire des propriétés nommées doit se produire lorsque ces propriétés sont copiées entre les magasins de message.</span><span class="sxs-lookup"><span data-stu-id="42f6f-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="42f6f-112">Toutefois, étant donné que les fournisseurs de magasins de message peuvent récupérer le nom pour le mappage d’identificateur de la destination, ils peuvent remapper les propriétés immédiatement et n’ont pas à s’appuyer sur la banque de messages de destination.</span><span class="sxs-lookup"><span data-stu-id="42f6f-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42f6f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42f6f-113">See also</span></span>



[<span data-ttu-id="42f6f-114">MAPI des propri�t�s nomm�e</span><span class="sxs-lookup"><span data-stu-id="42f6f-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

