---
title: Propriété canonique PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: eb04983015e8557541e69981ec130ebf07598655
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588369"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="5d186-103">Propriété canonique PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="5d186-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="5d186-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d186-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d186-105">Contient un masque de bits 32 bits d’indicateurs qui définissent l’état du dossier.</span><span class="sxs-lookup"><span data-stu-id="5d186-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d186-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5d186-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d186-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="5d186-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="5d186-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5d186-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d186-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="5d186-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="5d186-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5d186-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d186-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5d186-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5d186-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5d186-112">Area:</span></span>  <br/> |<span data-ttu-id="5d186-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="5d186-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d186-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d186-114">Remarks</span></span>

<span data-ttu-id="5d186-115">Cette propriété pour les dossiers est similaire à la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour les messages.</span><span class="sxs-lookup"><span data-stu-id="5d186-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="5d186-116">Ses indicateurs sont fournis pour l’application cliente uniquement et n’affectent pas la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="5d186-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="5d186-117">Les clients peuvent utiliser ou ignorer ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="5d186-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="5d186-118">Le client peut également définir ses propres valeurs pour les fichiers binaires client définissables de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5d186-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="5d186-119">Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits :</span><span class="sxs-lookup"><span data-stu-id="5d186-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="5d186-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="5d186-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="5d186-121">Le dossier est marqué pour suppression.</span><span class="sxs-lookup"><span data-stu-id="5d186-121">The folder is marked for deletion.</span></span> <span data-ttu-id="5d186-122">L’application cliente définit cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="5d186-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="5d186-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="5d186-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="5d186-124">Le dossier est masqué.</span><span class="sxs-lookup"><span data-stu-id="5d186-124">The folder is hidden.</span></span>
    
<span data-ttu-id="5d186-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="5d186-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="5d186-126">Le dossier est mis en surbrillance, par exemple, présentée dans l’ordre inverse vidéo.</span><span class="sxs-lookup"><span data-stu-id="5d186-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="5d186-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="5d186-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="5d186-128">Le dossier est marqué.</span><span class="sxs-lookup"><span data-stu-id="5d186-128">The folder is tagged.</span></span>
    
<span data-ttu-id="5d186-129">Fournisseurs de magasins message définir cette propriété sur un dossier pour une ou plusieurs de ces valeurs et les clients interprètent le statut en fonction de leurs applications.</span><span class="sxs-lookup"><span data-stu-id="5d186-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="5d186-130">Par exemple, un client peut utiliser l’état des dossiers pour différencier visuellement les dossiers dans une table de hiérarchie, en affichant les dossiers avec le même état de la même manière.</span><span class="sxs-lookup"><span data-stu-id="5d186-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="5d186-131">Dossiers en surbrillance puissent être affichés dans des dossiers vidéos, avec balise inverses dossiers marquées pour suppression peuvent être affichés avec une icône significative, et les dossiers cachés peuvent être masqués.</span><span class="sxs-lookup"><span data-stu-id="5d186-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="5d186-132">Bits 16 à 31 (« 0 x 10000 » par « 0 x 80000000 ») de cette propriété sont disponibles pour une utilisation par l’application cliente IPM.</span><span class="sxs-lookup"><span data-stu-id="5d186-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="5d186-133">Tous les autres bits sont réservés pour une utilisation par MAPI ; les paramètres non définis dans la liste précédente doivent initialement la valeur zéro et n’a pas été modifiés.</span><span class="sxs-lookup"><span data-stu-id="5d186-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5d186-134">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5d186-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d186-135">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5d186-135">Protocol specifications</span></span>

<span data-ttu-id="5d186-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d186-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d186-137">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="5d186-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d186-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d186-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d186-139">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="5d186-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d186-140">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5d186-140">Header files</span></span>

<span data-ttu-id="5d186-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d186-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d186-142">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5d186-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="5d186-143">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5d186-143">Mapitags.h</span></span>
  
> <span data-ttu-id="5d186-144">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="5d186-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d186-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d186-145">See also</span></span>



[<span data-ttu-id="5d186-146">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5d186-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d186-147">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5d186-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d186-148">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5d186-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d186-149">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5d186-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

