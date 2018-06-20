---
title: Propriété canonique PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786861"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="5fe01-103">Propriété canonique PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="5fe01-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5fe01-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fe01-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fe01-105">Contient un masque de bits d’indicateurs indiquant le plus d’informations sur un envoi de message.</span><span class="sxs-lookup"><span data-stu-id="5fe01-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5fe01-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5fe01-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5fe01-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5fe01-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="5fe01-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5fe01-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5fe01-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="5fe01-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="5fe01-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5fe01-110">Data type:</span></span>  <br/> |<span data-ttu-id="5fe01-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5fe01-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5fe01-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="5fe01-112">Area:</span></span>  <br/> |<span data-ttu-id="5fe01-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="5fe01-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fe01-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5fe01-114">Remarks</span></span>

<span data-ttu-id="5fe01-115">Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits **PR_SUBMIT_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="5fe01-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="5fe01-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="5fe01-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="5fe01-117">Le spouleur MAPI a actuellement le message verrouillé.</span><span class="sxs-lookup"><span data-stu-id="5fe01-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="5fe01-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="5fe01-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="5fe01-119">Le message doit prétraitement.</span><span class="sxs-lookup"><span data-stu-id="5fe01-119">The message needs preprocessing.</span></span> <span data-ttu-id="5fe01-120">Lorsque le spouleur MAPI est terminé prétraitement ce message, il doit appeler la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="5fe01-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="5fe01-121">Le fournisseur de banque de messages reconnaît que le spouleur, plutôt que l’application cliente, a appelé **SubmitMessage**, efface l’indicateur et continue d’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="5fe01-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5fe01-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5fe01-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5fe01-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5fe01-123">Protocol specifications</span></span>

<span data-ttu-id="5fe01-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fe01-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fe01-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="5fe01-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5fe01-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fe01-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fe01-127">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="5fe01-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5fe01-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5fe01-128">Header files</span></span>

<span data-ttu-id="5fe01-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5fe01-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5fe01-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5fe01-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="5fe01-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5fe01-131">Mapitags.h</span></span>
  
> <span data-ttu-id="5fe01-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="5fe01-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fe01-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fe01-133">See also</span></span>



[<span data-ttu-id="5fe01-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="5fe01-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="5fe01-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5fe01-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5fe01-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5fe01-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5fe01-137">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5fe01-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5fe01-138">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="5fe01-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

