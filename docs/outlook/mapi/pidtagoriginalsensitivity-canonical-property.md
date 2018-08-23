---
title: Propriété canonique PidTagOriginalSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3c921d2c9eee69148713408ec2e2a5510a27011a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582706"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="9077d-103">Propriété canonique PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="9077d-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="9077d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9077d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9077d-105">Contient la valeur de sensibilité attribuée par l’expéditeur de la première version d’un message, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="9077d-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9077d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9077d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9077d-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="9077d-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="9077d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9077d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9077d-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="9077d-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="9077d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9077d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9077d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9077d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9077d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9077d-112">Area:</span></span>  <br/> |<span data-ttu-id="9077d-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="9077d-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9077d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9077d-114">Remarks</span></span>

<span data-ttu-id="9077d-115">Une application cliente doit définir cette propriété sur la même valeur que la propriété **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) lorsque le message est le premier envoyé.</span><span class="sxs-lookup"><span data-stu-id="9077d-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="9077d-116">Il ne doit jamais être modifié par la suite.</span><span class="sxs-lookup"><span data-stu-id="9077d-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="9077d-117">Cette propriété est utilisée par le fournisseur de transport pour protéger la sensibilité sur les entrées copiées.</span><span class="sxs-lookup"><span data-stu-id="9077d-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="9077d-118">Elle lui permet, par exemple, pour empêcher la modification du texte des messages d’origine dans un transfert d’ou une réponse à un message qui a été initialement marqué **SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="9077d-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9077d-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9077d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9077d-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9077d-120">Protocol specifications</span></span>

<span data-ttu-id="9077d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9077d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9077d-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="9077d-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9077d-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9077d-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9077d-124">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="9077d-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9077d-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9077d-125">Header files</span></span>

<span data-ttu-id="9077d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9077d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="9077d-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9077d-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="9077d-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9077d-128">Mapitags.h</span></span>
  
> <span data-ttu-id="9077d-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="9077d-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9077d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9077d-130">See also</span></span>



[<span data-ttu-id="9077d-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9077d-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9077d-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9077d-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9077d-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9077d-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9077d-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9077d-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

