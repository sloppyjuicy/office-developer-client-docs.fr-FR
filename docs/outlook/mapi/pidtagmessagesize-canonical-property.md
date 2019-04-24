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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355649"
---
# <a name="pidtagmessagesize-canonical-property"></a><span data-ttu-id="111b9-103">Propriété canonique PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="111b9-103">PidTagMessageSize Canonical Property</span></span>

  
  
<span data-ttu-id="111b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="111b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="111b9-105">Contient la somme, en octets, des tailles de toutes les propriétés d'un objet message.</span><span class="sxs-lookup"><span data-stu-id="111b9-105">Contains the sum, in bytes, of the sizes of all properties on a message object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="111b9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="111b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="111b9-107">PR_MESSAGE_SIZE</span><span class="sxs-lookup"><span data-stu-id="111b9-107">PR_MESSAGE_SIZE</span></span>  <br/> |
|<span data-ttu-id="111b9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="111b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="111b9-109">0x0E08</span><span class="sxs-lookup"><span data-stu-id="111b9-109">0x0E08</span></span>  <br/> |
|<span data-ttu-id="111b9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="111b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="111b9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="111b9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="111b9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="111b9-112">Area:</span></span>  <br/> |<span data-ttu-id="111b9-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="111b9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="111b9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="111b9-114">Remarks</span></span>

<span data-ttu-id="111b9-115">Il est recommandé que les objets message exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="111b9-115">It is recommended that message objects expose this property.</span></span> <span data-ttu-id="111b9-116">La taille du message indique le nombre approximatif d'octets transférés lorsque le message est déplacé d'une banque de messages à une autre.</span><span class="sxs-lookup"><span data-stu-id="111b9-116">The message size indicates the approximate number of bytes that are transferred when the message is moved from one message store to another.</span></span> <span data-ttu-id="111b9-117">Étant la somme des tailles de toutes les propriétés de l'objet message, il est généralement beaucoup plus grand que le texte du message seul.</span><span class="sxs-lookup"><span data-stu-id="111b9-117">Being the sum of the sizes of all properties on the message object, it is usually considerably greater than the message text alone.</span></span> 
  
<span data-ttu-id="111b9-118">La plupart des fournisseurs de banques de messages calculent cette propriété pour les messages qu'elles gèrent.</span><span class="sxs-lookup"><span data-stu-id="111b9-118">Most message store providers compute this property for messages that they handle.</span></span> <span data-ttu-id="111b9-119">Toutefois, certains fournisseurs de banques de messages ne prennent pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="111b9-119">However, some message store providers do not support this property.</span></span> <span data-ttu-id="111b9-120">Dans tous les cas, cette propriété n'est pas disponible tant que la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ou [IMessage:: SubmitMessage](imessage-submitmessage.md) n'a pas été appelée.</span><span class="sxs-lookup"><span data-stu-id="111b9-120">In any case, this property is not available until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMessage::SubmitMessage](imessage-submitmessage.md) method has been called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="111b9-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="111b9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="111b9-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="111b9-122">Protocol specifications</span></span>

<span data-ttu-id="111b9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="111b9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="111b9-124">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="111b9-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="111b9-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="111b9-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="111b9-126">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="111b9-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="111b9-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="111b9-127">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="111b9-128">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="111b9-128">Handles folder operations.</span></span>
    
<span data-ttu-id="111b9-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="111b9-129">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="111b9-130">Spécifie les opérations admissibles pour les objets principaux de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="111b9-130">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="111b9-131">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="111b9-131">Header files</span></span>

<span data-ttu-id="111b9-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="111b9-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="111b9-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="111b9-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="111b9-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="111b9-134">Mapitags.h</span></span>
  
> <span data-ttu-id="111b9-135">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="111b9-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="111b9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="111b9-136">See also</span></span>



[<span data-ttu-id="111b9-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="111b9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="111b9-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="111b9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="111b9-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="111b9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="111b9-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="111b9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

