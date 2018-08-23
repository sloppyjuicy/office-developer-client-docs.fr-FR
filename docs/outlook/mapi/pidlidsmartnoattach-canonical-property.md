---
title: Propriété canonique PidLidSmartNoAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e4a0e87b24789e3ee4cb5ed6684d508b62e65b30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575972"
---
# <a name="pidlidsmartnoattach-canonical-property"></a><span data-ttu-id="df4de-103">Propriété canonique PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="df4de-103">PidLidSmartNoAttach Canonical Property</span></span>

  
  
<span data-ttu-id="df4de-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df4de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df4de-105">Indique si les pièces jointes d’un message sont considérés comme étant masquées.</span><span class="sxs-lookup"><span data-stu-id="df4de-105">Represents whether the attachments on a message are considered as hidden.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df4de-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="df4de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df4de-107">dispidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="df4de-107">dispidSmartNoAttach</span></span>  <br/> |
|<span data-ttu-id="df4de-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="df4de-108">Property set:</span></span>  <br/> |<span data-ttu-id="df4de-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="df4de-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="df4de-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="df4de-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="df4de-111">0x00008514</span><span class="sxs-lookup"><span data-stu-id="df4de-111">0x00008514</span></span>  <br/> |
|<span data-ttu-id="df4de-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="df4de-112">Data type:</span></span>  <br/> |<span data-ttu-id="df4de-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="df4de-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="df4de-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="df4de-114">Area:</span></span>  <br/> |<span data-ttu-id="df4de-115">Configuration d’exécution</span><span class="sxs-lookup"><span data-stu-id="df4de-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df4de-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="df4de-116">Remarks</span></span>

<span data-ttu-id="df4de-117">Cette propriété a la valeur TRUE si les pièces jointes du message sont considérés comme étant masquées.</span><span class="sxs-lookup"><span data-stu-id="df4de-117">This property is TRUE if the attachments of the message are considered as hidden.</span></span>
  
<span data-ttu-id="df4de-118">Il indique si l’objet message n’a pas les pièces jointes visible pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="df4de-118">It indicates whether the message object has no end-user visible attachments.</span></span> <span data-ttu-id="df4de-119">Cette propriété peut être annulée ; Dans ce cas, la valeur FALSE par défaut est supposée.</span><span class="sxs-lookup"><span data-stu-id="df4de-119">This property may be unset; if so, a default value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="df4de-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="df4de-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df4de-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="df4de-121">Protocol specifications</span></span>

<span data-ttu-id="df4de-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df4de-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df4de-123">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="df4de-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df4de-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df4de-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df4de-125">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="df4de-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df4de-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="df4de-126">Header files</span></span>

<span data-ttu-id="df4de-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df4de-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="df4de-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="df4de-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df4de-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df4de-129">See also</span></span>



[<span data-ttu-id="df4de-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="df4de-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df4de-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="df4de-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df4de-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="df4de-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df4de-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="df4de-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

