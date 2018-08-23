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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fb048d622aaf3cfa97f380e21324749d7421603e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563687"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="03b22-103">Propriété canonique PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="03b22-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="03b22-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03b22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03b22-105">Contient un masque de bits d’indicateurs indiquant le plus d’informations sur un envoi de message.</span><span class="sxs-lookup"><span data-stu-id="03b22-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03b22-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="03b22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03b22-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="03b22-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="03b22-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="03b22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03b22-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="03b22-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="03b22-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="03b22-110">Data type:</span></span>  <br/> |<span data-ttu-id="03b22-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="03b22-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="03b22-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="03b22-112">Area:</span></span>  <br/> |<span data-ttu-id="03b22-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="03b22-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03b22-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="03b22-114">Remarks</span></span>

<span data-ttu-id="03b22-115">Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits **PR_SUBMIT_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="03b22-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="03b22-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="03b22-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="03b22-117">Le spouleur MAPI a actuellement le message verrouillé.</span><span class="sxs-lookup"><span data-stu-id="03b22-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="03b22-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="03b22-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="03b22-119">Le message doit prétraitement.</span><span class="sxs-lookup"><span data-stu-id="03b22-119">The message needs preprocessing.</span></span> <span data-ttu-id="03b22-120">Lorsque le spouleur MAPI est terminé prétraitement ce message, il doit appeler la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="03b22-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="03b22-121">Le fournisseur de banque de messages reconnaît que le spouleur, plutôt que l’application cliente, a appelé **SubmitMessage**, efface l’indicateur et continue d’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="03b22-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="03b22-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="03b22-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03b22-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="03b22-123">Protocol specifications</span></span>

<span data-ttu-id="03b22-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03b22-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03b22-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="03b22-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03b22-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03b22-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03b22-127">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="03b22-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03b22-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="03b22-128">Header files</span></span>

<span data-ttu-id="03b22-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03b22-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="03b22-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="03b22-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="03b22-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="03b22-131">Mapitags.h</span></span>
  
> <span data-ttu-id="03b22-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="03b22-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03b22-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03b22-133">See also</span></span>



[<span data-ttu-id="03b22-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="03b22-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="03b22-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="03b22-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03b22-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="03b22-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03b22-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="03b22-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03b22-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="03b22-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

