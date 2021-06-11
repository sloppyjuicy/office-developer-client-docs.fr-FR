---
title: Propriété canonique PidTagSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a9361f3027453742acbe50c3de01d860289cd0ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356685"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="1e4b5-103">Propriété canonique PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="1e4b5-103">PidTagSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="1e4b5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e4b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e4b5-105">Contient la clé de recherche de l’utilisateur de messagerie représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-105">Contains the search key for the messaging user represented by the sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e4b5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1e4b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e4b5-107">PR_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="1e4b5-107">PR_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="1e4b5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1e4b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e4b5-109">0x003B</span><span class="sxs-lookup"><span data-stu-id="1e4b5-109">0x003B</span></span>  <br/> |
|<span data-ttu-id="1e4b5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1e4b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e4b5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1e4b5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1e4b5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1e4b5-112">Area:</span></span>  <br/> |<span data-ttu-id="1e4b5-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="1e4b5-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e4b5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1e4b5-114">Remarks</span></span>

<span data-ttu-id="1e4b5-115">Cette propriété est l’une des propriétés d’adresse de l’utilisateur de messagerie représenté par l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-115">This property is one of the address properties for the messaging user who is being represented by the sender.</span></span> <span data-ttu-id="1e4b5-116">Lorsqu’une application cliente envoie un message pour le compte d’un autre client, elle doit définir toutes les propriétés d’expéditeur représentées sur les valeurs de ce client.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-116">When a client application sends a message on behalf of another client, it should set all the represented sender properties to the values for that client.</span></span> <span data-ttu-id="1e4b5-117">Un utilisateur de messagerie envoyant en son propre nom laisse généralement les propriétés de l’expéditeur représenté non jeu.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-117">A messaging user sending on its own behalf typically leaves the represented sender properties unset.</span></span>
  
<span data-ttu-id="1e4b5-118">Le fournisseur de transport sortant doit toujours laisser cette propriété inchangée si elle a été définie par le client d’envoi.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-118">The outgoing transport provider must always leave this property unchanged if it has been set by the sending client.</span></span> <span data-ttu-id="1e4b5-119">Si elle n’est pas définie, le fournisseur de transport doit la définir sur **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) sur la copie sortante du message et la laisser non définie sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-119">If it is unset, the transport provider should set it to **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) on the outbound copy of the message, and leave it unset on the local copy.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1e4b5-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1e4b5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e4b5-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="1e4b5-121">Protocol specifications</span></span>

<span data-ttu-id="1e4b5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e4b5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e4b5-123">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1e4b5-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e4b5-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e4b5-125">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-125">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="1e4b5-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e4b5-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e4b5-127">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-127">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="1e4b5-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e4b5-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e4b5-129">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1e4b5-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e4b5-130">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e4b5-131">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-131">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="1e4b5-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e4b5-132">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e4b5-133">Spécifie les propriétés et opérations autorisées pour les objets de publication.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-133">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="1e4b5-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e4b5-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e4b5-135">Spécifie les propriétés et opérations autorisées pour les listes de distribution personnelles et de contacts.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-135">Specifies the properties and operations that are permissible for contact and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e4b5-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1e4b5-136">Header files</span></span>

<span data-ttu-id="1e4b5-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e4b5-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e4b5-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e4b5-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e4b5-139">Mapitags.h</span></span>
  
> <span data-ttu-id="1e4b5-140">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="1e4b5-140">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e4b5-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e4b5-141">See also</span></span>



[<span data-ttu-id="1e4b5-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1e4b5-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e4b5-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1e4b5-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e4b5-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1e4b5-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e4b5-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1e4b5-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

