---
title: Propriété canonique PidTagReceivedByEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByEntryId
api_type:
- COM
ms.assetid: 737f8584-fc52-4324-ac40-2fc554a3095d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2f0203fc787ced9a0198be10c238f6245cb15144
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359219"
---
# <a name="pidtagreceivedbyentryid-canonical-property"></a><span data-ttu-id="3cbcc-103">Propriété canonique PidTagReceivedByEntryId</span><span class="sxs-lookup"><span data-stu-id="3cbcc-103">PidTagReceivedByEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3cbcc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cbcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cbcc-105">Contient l’identificateur d’entrée de l’utilisateur de messagerie qui reçoit réellement le message.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-105">Contains the entry identifier of the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3cbcc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3cbcc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cbcc-107">PR_RECEIVED_BY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3cbcc-107">PR_RECEIVED_BY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="3cbcc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3cbcc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3cbcc-109">0x003F</span><span class="sxs-lookup"><span data-stu-id="3cbcc-109">0x003F</span></span>  <br/> |
|<span data-ttu-id="3cbcc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3cbcc-110">Data type:</span></span>  <br/> |<span data-ttu-id="3cbcc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3cbcc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3cbcc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3cbcc-112">Area:</span></span>  <br/> |<span data-ttu-id="3cbcc-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="3cbcc-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cbcc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3cbcc-114">Remarks</span></span>

<span data-ttu-id="3cbcc-115">Cette propriété est l’une des propriétés d’adresse de l’utilisateur de messagerie qui reçoit le message.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="3cbcc-116">Elle doit être définie par le fournisseur de transport entrant.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-116">It must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="3cbcc-117">Cette propriété correspond à une enveloppe de remise X.400 par attribut MH_T_ message.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-117">This property corresponds to an X.400 delivery envelope per-message MH_T_ attribute.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3cbcc-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3cbcc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cbcc-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="3cbcc-119">Protocol specifications</span></span>

<span data-ttu-id="3cbcc-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cbcc-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cbcc-121">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3cbcc-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cbcc-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cbcc-123">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="3cbcc-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cbcc-124">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cbcc-125">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-125">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="3cbcc-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cbcc-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cbcc-127">Convertit les éléments RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les éléments de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
<span data-ttu-id="3cbcc-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cbcc-128">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cbcc-129">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-129">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="3cbcc-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cbcc-130">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cbcc-131">Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-131">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cbcc-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3cbcc-132">Header files</span></span>

<span data-ttu-id="3cbcc-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cbcc-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cbcc-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="3cbcc-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3cbcc-135">Mapitags.h</span></span>
  
> <span data-ttu-id="3cbcc-136">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="3cbcc-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cbcc-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cbcc-137">See also</span></span>



[<span data-ttu-id="3cbcc-138">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="3cbcc-138">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)


[<span data-ttu-id="3cbcc-139">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3cbcc-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cbcc-140">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3cbcc-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cbcc-141">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3cbcc-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cbcc-142">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3cbcc-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

