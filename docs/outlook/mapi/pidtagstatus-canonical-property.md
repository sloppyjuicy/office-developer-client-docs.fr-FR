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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278791"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="43909-103">Propriété canonique PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="43909-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="43909-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43909-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43909-105">Contient un masque de bits 32 bits des indicateurs qui définissent l'état du dossier.</span><span class="sxs-lookup"><span data-stu-id="43909-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43909-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="43909-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43909-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="43909-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="43909-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="43909-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43909-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="43909-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="43909-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="43909-110">Data type:</span></span>  <br/> |<span data-ttu-id="43909-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="43909-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="43909-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="43909-112">Area:</span></span>  <br/> |<span data-ttu-id="43909-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="43909-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43909-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="43909-114">Remarks</span></span>

<span data-ttu-id="43909-115">Cette propriété pour les dossiers est analogue à la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) pour les messages.</span><span class="sxs-lookup"><span data-stu-id="43909-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="43909-116">Ses indicateurs sont fournis uniquement pour l'application cliente et n'affectent pas la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="43909-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="43909-117">Les clients peuvent utiliser ou ignorer ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="43909-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="43909-118">Le client peut également définir ses propres valeurs pour les bits définissables par le client de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="43909-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="43909-119">Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de masques:</span><span class="sxs-lookup"><span data-stu-id="43909-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="43909-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="43909-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="43909-121">Le dossier est marqué pour suppression.</span><span class="sxs-lookup"><span data-stu-id="43909-121">The folder is marked for deletion.</span></span> <span data-ttu-id="43909-122">L'application cliente définit cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="43909-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="43909-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="43909-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="43909-124">Le dossier est masqué.</span><span class="sxs-lookup"><span data-stu-id="43909-124">The folder is hidden.</span></span>
    
<span data-ttu-id="43909-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="43909-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="43909-126">Le dossier est mis en surbrillance, par exemple, affiché dans la vidéo inversée.</span><span class="sxs-lookup"><span data-stu-id="43909-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="43909-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="43909-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="43909-128">Le dossier est balisé.</span><span class="sxs-lookup"><span data-stu-id="43909-128">The folder is tagged.</span></span>
    
<span data-ttu-id="43909-129">Les fournisseurs de banque de messages définissent cette propriété d'un dossier sur une ou plusieurs de ces valeurs et les clients interprètent l'État comme approprié pour leurs applications.</span><span class="sxs-lookup"><span data-stu-id="43909-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="43909-130">Par exemple, un client peut utiliser l'état du dossier pour faire la distinction visuelle entre les dossiers d'une table de hiérarchie, en affichant les dossiers présentant le même état de la même façon.</span><span class="sxs-lookup"><span data-stu-id="43909-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="43909-131">Les dossiers en surBrillance peuvent être affichés dans la vidéo inversée, les dossiers et les dossiers balisés marqués pour suppression peuvent être affichés avec une icône significative, et les dossiers masqués peuvent être masqués.</span><span class="sxs-lookup"><span data-stu-id="43909-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="43909-132">Les bits 16 à 31 («0x10000» à «0x80000000») de cette propriété peuvent être utilisés par l'application cliente IPM.</span><span class="sxs-lookup"><span data-stu-id="43909-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="43909-133">Tous les autres bits sont réservés à l'usage de MAPI; ceux qui ne sont pas définis dans la liste précédente doivent être initialement définis sur zéro et ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="43909-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="43909-134">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="43909-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43909-135">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="43909-135">Protocol specifications</span></span>

<span data-ttu-id="43909-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43909-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43909-137">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="43909-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43909-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43909-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43909-139">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="43909-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43909-140">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="43909-140">Header files</span></span>

<span data-ttu-id="43909-141">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="43909-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="43909-142">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="43909-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="43909-143">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="43909-143">Mapitags.h</span></span>
  
> <span data-ttu-id="43909-144">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="43909-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43909-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43909-145">See also</span></span>



[<span data-ttu-id="43909-146">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="43909-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43909-147">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="43909-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43909-148">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="43909-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43909-149">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="43909-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

