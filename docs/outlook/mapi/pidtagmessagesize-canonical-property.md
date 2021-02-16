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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355649"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="2e277-103">Propriété canonique PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="2e277-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="2e277-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e277-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e277-105">Contient la somme, en octets, de la taille de toutes les propriétés d’un objet message.</span><span class="sxs-lookup"><span data-stu-id="2e277-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e277-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2e277-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e277-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="2e277-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="2e277-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2e277-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e277-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="2e277-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="2e277-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2e277-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e277-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2e277-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2e277-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2e277-112">Area:</span></span>  <br/> |<span data-ttu-id="2e277-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="2e277-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e277-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e277-114">Remarks</span></span>

<span data-ttu-id="2e277-115">Il est recommandé que les objets de message exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2e277-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="2e277-116">La taille du message indique le nombre approximatif d’octets transférés lorsque le message est déplacé d’une magasin de messages vers une autre.</span><span class="sxs-lookup"><span data-stu-id="2e277-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="2e277-117">Étant la somme des tailles de toutes les propriétés de l’objet de message, elle est généralement beaucoup plus grande que le texte du message uniquement.</span><span class="sxs-lookup"><span data-stu-id="2e277-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="2e277-118">La plupart des fournisseurs de magasins de messages calculent cette propriété pour les messages qu’ils gèrent.</span><span class="sxs-lookup"><span data-stu-id="2e277-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="2e277-119">Toutefois, certains fournisseurs de magasins de messages ne la prise en charge de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2e277-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="2e277-120">Dans tous les cas, cette propriété n’est pas disponible tant que la méthode [IMAPIProp::SaveChanges ou](imapiprop-savechanges.md) [IMessage::SubmitMessage](imessage-submitmessage.md) n’a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="2e277-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e277-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2e277-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e277-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="2e277-122">Protocol specifications</span></span>

<span data-ttu-id="2e277-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e277-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e277-124">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="2e277-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e277-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e277-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e277-126">Gère les objets de message et de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2e277-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="2e277-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e277-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e277-128">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="2e277-128">Handles folder operations.</span></span>
    
<span data-ttu-id="2e277-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e277-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e277-130">Spécifie les opérations autorisées pour les objets principaux de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="2e277-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e277-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2e277-131">Header files</span></span>

<span data-ttu-id="2e277-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e277-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e277-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2e277-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e277-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e277-134">Mapitags.h</span></span>
  
> <span data-ttu-id="2e277-135">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="2e277-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e277-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e277-136">See also</span></span>



[<span data-ttu-id="2e277-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2e277-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e277-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2e277-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e277-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2e277-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e277-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2e277-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

