---
title: Propriété canonique PidTagSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderSearchKey
api_type:
- COM
ms.assetid: e15599c5-f40f-46a6-a726-7359efd09ff8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3f73f1ef919bab15a8f89b7fddc43608411635e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573452"
---
# <a name="pidtagsendersearchkey-canonical-property"></a><span data-ttu-id="62b62-103">Propriété canonique PidTagSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="62b62-103">PidTagSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="62b62-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62b62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62b62-105">Contient une clé de recherche de l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="62b62-105">Contains the message sender's search key.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62b62-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="62b62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62b62-107">PR_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="62b62-107">PR_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="62b62-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="62b62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="62b62-109">0x0C1D</span><span class="sxs-lookup"><span data-stu-id="62b62-109">0x0C1D</span></span>  <br/> |
|<span data-ttu-id="62b62-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="62b62-110">Data type:</span></span>  <br/> |<span data-ttu-id="62b62-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="62b62-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="62b62-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="62b62-112">Area:</span></span>  <br/> |<span data-ttu-id="62b62-113">Address</span><span class="sxs-lookup"><span data-stu-id="62b62-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62b62-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="62b62-114">Remarks</span></span>

<span data-ttu-id="62b62-115">Cette propriété est une des propriétés d’adresse pour l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="62b62-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="62b62-116">Elle doit être définie par le fournisseur de transport sortant, qui ne doit jamais propager toutes les valeurs existantes.</span><span class="sxs-lookup"><span data-stu-id="62b62-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="62b62-117">Si aucun fournisseur de transport n’a fourni les propriétés d’adresse de l’expéditeur, le spouleur MAPI tente de les remplir en appelant la méthode [IMAPISession::QueryIdentity](imapisession-queryidentity.md) pour un identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="62b62-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="62b62-118">Si aucun identificateur d’entrée n’ont été fournies, le spouleur MAPI stocke une clé correspondant à la chaîne « Inconnue » dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="62b62-118">If no entry identifiers have been provided, the MAPI spooler stores a key corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="62b62-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="62b62-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62b62-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="62b62-120">Protocol specifications</span></span>

<span data-ttu-id="62b62-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62b62-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62b62-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="62b62-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62b62-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62b62-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62b62-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="62b62-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="62b62-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62b62-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62b62-126">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="62b62-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="62b62-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62b62-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62b62-128">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="62b62-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="62b62-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62b62-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62b62-130">Spécifie les propriétés et les opérations qui sont autorisées pour publier des objets.</span><span class="sxs-lookup"><span data-stu-id="62b62-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="62b62-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62b62-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62b62-132">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="62b62-132">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="62b62-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62b62-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62b62-134">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="62b62-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62b62-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="62b62-135">Header files</span></span>

<span data-ttu-id="62b62-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62b62-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="62b62-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="62b62-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="62b62-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="62b62-138">Mapitags.h</span></span>
  
> <span data-ttu-id="62b62-139">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="62b62-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62b62-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62b62-140">See also</span></span>



[<span data-ttu-id="62b62-141">Propriété canonique PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="62b62-141">PidTagSearchKey Canonical Property</span></span>](pidtagsearchkey-canonical-property.md)
  
[<span data-ttu-id="62b62-142">Propriété canonique PidTagSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="62b62-142">PidTagSentRepresentingSearchKey Canonical Property</span></span>](pidtagsentrepresentingsearchkey-canonical-property.md)


[<span data-ttu-id="62b62-143">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="62b62-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62b62-144">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="62b62-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62b62-145">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="62b62-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62b62-146">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="62b62-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

