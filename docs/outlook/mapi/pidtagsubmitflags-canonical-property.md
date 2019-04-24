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
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339353"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="0861e-103">Propriété canonique PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="0861e-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="0861e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0861e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0861e-105">Contient un masque de masque des indicateurs qui indiquent les détails relatifs à l'envoi d'un message.</span><span class="sxs-lookup"><span data-stu-id="0861e-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0861e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0861e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0861e-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0861e-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="0861e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0861e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0861e-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="0861e-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="0861e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0861e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0861e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0861e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0861e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0861e-112">Area:</span></span>  <br/> |<span data-ttu-id="0861e-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="0861e-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0861e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0861e-114">Remarks</span></span>

<span data-ttu-id="0861e-115">Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de masque **PR_SUBMIT_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="0861e-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="0861e-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="0861e-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="0861e-117">Le spouleur MAPI contient actuellement un message verrouillé.</span><span class="sxs-lookup"><span data-stu-id="0861e-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="0861e-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="0861e-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="0861e-119">Le message doit être prétraité.</span><span class="sxs-lookup"><span data-stu-id="0861e-119">The message needs preprocessing.</span></span> <span data-ttu-id="0861e-120">Lorsque le spouleur MAPI est fini de prétraiter ce message, il doit appeler la méthode [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="0861e-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="0861e-121">Le fournisseur de banque de messages reconnaît que le spouleur, et non l'application cliente, a appelé **SubmitMessage**, efface l'indicateur et continue l'envoi des messages.</span><span class="sxs-lookup"><span data-stu-id="0861e-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="0861e-122">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="0861e-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0861e-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="0861e-123">Protocol specifications</span></span>

<span data-ttu-id="0861e-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0861e-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0861e-125">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0861e-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0861e-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0861e-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0861e-127">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="0861e-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0861e-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="0861e-128">Header files</span></span>

<span data-ttu-id="0861e-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0861e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0861e-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0861e-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="0861e-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0861e-131">Mapitags.h</span></span>
  
> <span data-ttu-id="0861e-132">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="0861e-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0861e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0861e-133">See also</span></span>



[<span data-ttu-id="0861e-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="0861e-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="0861e-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0861e-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0861e-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0861e-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0861e-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0861e-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0861e-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0861e-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

