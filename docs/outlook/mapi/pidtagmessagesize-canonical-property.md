---
title: Propriété canonique PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c52fd6d6caaec6f215856daead809ceb0bd76729
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574992"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="2eea5-103">Propriété canonique PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="2eea5-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="2eea5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2eea5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2eea5-105">Contient les fonctions sum, en octets, des tailles de toutes les propriétés sur un objet de message.</span><span class="sxs-lookup"><span data-stu-id="2eea5-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2eea5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2eea5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2eea5-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="2eea5-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="2eea5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2eea5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2eea5-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="2eea5-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="2eea5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2eea5-110">Data type:</span></span>  <br/> |<span data-ttu-id="2eea5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2eea5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2eea5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2eea5-112">Area:</span></span>  <br/> |<span data-ttu-id="2eea5-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="2eea5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2eea5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2eea5-114">Remarks</span></span>

<span data-ttu-id="2eea5-115">Il est recommandé que les objets message exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2eea5-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="2eea5-116">La taille du message indique le nombre approximatif d’octets qui sont transférées lorsque le message est déplacé à partir d’une banque d’informations à un autre.</span><span class="sxs-lookup"><span data-stu-id="2eea5-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="2eea5-117">En cours de la somme des tailles de toutes les propriétés de l’objet du message, il est généralement beaucoup plu nombreuses que seul le texte du message.</span><span class="sxs-lookup"><span data-stu-id="2eea5-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="2eea5-118">La base de la plupart des messages fournisseurs compute cette propriété pour les messages qu’ils gèrent.</span><span class="sxs-lookup"><span data-stu-id="2eea5-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="2eea5-119">Toutefois, certains fournisseurs de banque de messages ne prennent pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2eea5-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="2eea5-120">Dans tous les cas, cette propriété n’est pas disponible jusqu'à ce que la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMessage::SubmitMessage](imessage-submitmessage.md) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="2eea5-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2eea5-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2eea5-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2eea5-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="2eea5-122">Protocol specifications</span></span>

<span data-ttu-id="2eea5-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2eea5-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2eea5-124">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="2eea5-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2eea5-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2eea5-125">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2eea5-126">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2eea5-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="2eea5-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2eea5-127">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2eea5-128">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="2eea5-128">Handles folder operations.</span></span>
    
<span data-ttu-id="2eea5-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2eea5-129">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2eea5-130">Spécifie les opérations autorisées pour les objets de banque de messages principale.</span><span class="sxs-lookup"><span data-stu-id="2eea5-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2eea5-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2eea5-131">Header files</span></span>

<span data-ttu-id="2eea5-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2eea5-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="2eea5-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2eea5-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="2eea5-134">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="2eea5-134">Mapitags.h</span></span>
  
> <span data-ttu-id="2eea5-135">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="2eea5-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2eea5-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2eea5-136">See also</span></span>



[<span data-ttu-id="2eea5-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2eea5-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2eea5-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2eea5-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2eea5-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2eea5-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2eea5-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2eea5-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

