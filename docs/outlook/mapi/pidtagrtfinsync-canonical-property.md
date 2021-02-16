---
title: Propriété canonique PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357875"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="6f6b9-103">Propriété canonique PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="6f6b9-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="6f6b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f6b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f6b9-105">Contient TRUE si la **propriété PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) a le même contenu de texte que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) pour ce message.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f6b9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6f6b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f6b9-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="6f6b9-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="6f6b9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6f6b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f6b9-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="6f6b9-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="6f6b9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6f6b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f6b9-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6f6b9-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6f6b9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6f6b9-112">Area:</span></span>  <br/> |<span data-ttu-id="6f6b9-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="6f6b9-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f6b9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f6b9-114">Remarks</span></span>

<span data-ttu-id="6f6b9-115">La valeur TRUE signifie que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la version en texte simple de ce message et la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version RTF (Rich Text Format), sont identiques, sauf pour les espaces blancs dans **PR_BODY** et la mise en forme dans **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="6f6b9-116">Le texte des deux versions se compose des mêmes caractères dans la même séquence.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="6f6b9-117">La valeur FALSE signifie que les deux versions ne sont pas synchronisées pour le contenu de texte, mais sont capables d’être synchronisées par la [fonction RTFSync.](rtfsync.md)</span><span class="sxs-lookup"><span data-stu-id="6f6b9-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="6f6b9-118">Une version a été modifiée et l’autre version n’a pas été modifiée.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="6f6b9-119">Aucune valeur ne signifie que les deux versions, si elles existent ou existent déjà, ne peuvent pas être synchronisées.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="6f6b9-120">Une version a été supprimée ou modifiée de façon si radicale que la synchronisation n’est plus possible.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="6f6b9-121">Une application cliente qui a modifié **PR_RTF_COMPRESSED** doit définir la valeur FALSE dans cette propriété pour forcer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="6f6b9-122">Les magasins de messages rtF doivent effectuer la synchronisation à l’aide de **RTFSync** pendant un appel [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="6f6b9-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="6f6b9-123">Les clients rtF doivent vérifier  le paramètre de PR_RTF_IN_SYNC avant de lire **PR_RTF_COMPRESSED** et appeler **d’abord RTFSync** si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="6f6b9-124">Si **PR_BODY** des modifications ont été apportées à autre chose que son espace blanc, la boutique de messages doit supprimer PR_RTF_IN_SYNC **pour** mettre fin à la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6f6b9-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6f6b9-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f6b9-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6f6b9-126">Protocol specifications</span></span>

<span data-ttu-id="6f6b9-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f6b9-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f6b9-128">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f6b9-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f6b9-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f6b9-130">Gère les objets de message et de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f6b9-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6f6b9-131">Header files</span></span>

<span data-ttu-id="6f6b9-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f6b9-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f6b9-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f6b9-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f6b9-134">Mapitags.h</span></span>
  
> <span data-ttu-id="6f6b9-135">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="6f6b9-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f6b9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f6b9-136">See also</span></span>



[<span data-ttu-id="6f6b9-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6f6b9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f6b9-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6f6b9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f6b9-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6f6b9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f6b9-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6f6b9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

