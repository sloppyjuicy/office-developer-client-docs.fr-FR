---
title: Propriété canonique PidTagReceivedBySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedBySearchKey
api_type:
- COM
ms.assetid: 4b37555a-1d07-4f42-95e3-b8fa37ed0c3b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bace518784bf24807cfca09032a4f3912f4e98ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359205"
---
# <a name="pidtagreceivedbysearchkey-canonical-property"></a><span data-ttu-id="f87d1-103">Propriété canonique PidTagReceivedBySearchKey</span><span class="sxs-lookup"><span data-stu-id="f87d1-103">PidTagReceivedBySearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="f87d1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f87d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f87d1-105">Contient la clé de recherche de l'utilisateur de messagerie qui reçoit le message.</span><span class="sxs-lookup"><span data-stu-id="f87d1-105">Contains the search key of the messaging user who receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f87d1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f87d1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f87d1-107">PR_RECEIVED_BY_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="f87d1-107">PR_RECEIVED_BY_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="f87d1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f87d1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f87d1-109">0x0051</span><span class="sxs-lookup"><span data-stu-id="f87d1-109">0x0051</span></span>  <br/> |
|<span data-ttu-id="f87d1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f87d1-110">Data type:</span></span>  <br/> |<span data-ttu-id="f87d1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f87d1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f87d1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f87d1-112">Area:</span></span>  <br/> |<span data-ttu-id="f87d1-113">Address</span><span class="sxs-lookup"><span data-stu-id="f87d1-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f87d1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f87d1-114">Remarks</span></span>

<span data-ttu-id="f87d1-115">Cette propriété est l'une des propriétés d'adresse de l'utilisateur de messagerie qui reçoit le message.</span><span class="sxs-lookup"><span data-stu-id="f87d1-115">This property is one of the address properties for the messaging user who receives the message.</span></span> <span data-ttu-id="f87d1-116">Il doit être défini par le fournisseur de transport entrant.</span><span class="sxs-lookup"><span data-stu-id="f87d1-116">It must be set by the incoming transport provider.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f87d1-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="f87d1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f87d1-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f87d1-118">Protocol specifications</span></span>

<span data-ttu-id="f87d1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f87d1-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f87d1-120">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f87d1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f87d1-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f87d1-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f87d1-122">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="f87d1-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="f87d1-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f87d1-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f87d1-124">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="f87d1-124">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f87d1-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f87d1-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f87d1-126">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="f87d1-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="f87d1-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f87d1-127">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f87d1-128">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets message et Calendar lorsqu'ils agissent pour le compte d'un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f87d1-128">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="f87d1-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f87d1-129">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f87d1-130">Encode et décode les objets message et Attachment en une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="f87d1-130">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f87d1-131">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="f87d1-131">Header files</span></span>

<span data-ttu-id="f87d1-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f87d1-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="f87d1-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f87d1-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="f87d1-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f87d1-134">Mapitags.h</span></span>
  
> <span data-ttu-id="f87d1-135">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="f87d1-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f87d1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f87d1-136">See also</span></span>



[<span data-ttu-id="f87d1-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f87d1-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f87d1-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f87d1-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f87d1-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f87d1-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f87d1-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f87d1-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

