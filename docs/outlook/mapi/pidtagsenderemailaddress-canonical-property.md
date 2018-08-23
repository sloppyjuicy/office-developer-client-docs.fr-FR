---
title: Propriété canonique PidTagSenderEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEmailAddress
api_type:
- COM
ms.assetid: 6e1531ac-489b-4224-921a-8fd13ace9497
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8efceed4910d057d6dcca742dfe9b8f0010c968e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578674"
---
# <a name="pidtagsenderemailaddress-canonical-property"></a><span data-ttu-id="ebd38-103">Propriété canonique PidTagSenderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ebd38-103">PidTagSenderEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="ebd38-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebd38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebd38-105">Contient l’adresse de messagerie de l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="ebd38-105">Contains the message sender's email address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ebd38-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ebd38-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ebd38-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="ebd38-107">PR_SENDER_EMAIL_ADDRESS, PR_SENDER_EMAIL_ADDRESS_A, PR_SENDER_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="ebd38-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ebd38-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ebd38-109">0x0C1F</span><span class="sxs-lookup"><span data-stu-id="ebd38-109">0x0C1F</span></span>  <br/> |
|<span data-ttu-id="ebd38-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ebd38-110">Data type:</span></span>  <br/> |<span data-ttu-id="ebd38-111">PT_UNICOIDE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ebd38-111">PT_UNICOIDE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ebd38-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ebd38-112">Area:</span></span>  <br/> |<span data-ttu-id="ebd38-113">Address</span><span class="sxs-lookup"><span data-stu-id="ebd38-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebd38-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebd38-114">Remarks</span></span>

<span data-ttu-id="ebd38-115">Ces propriétés sont des exemples de propriétés d’adresse pour l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="ebd38-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="ebd38-116">Elles doivent être définies par le fournisseur de transport sortant, qui ne doit jamais propager toutes les valeurs existantes.</span><span class="sxs-lookup"><span data-stu-id="ebd38-116">They must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="ebd38-117">Si aucun fournisseur de transport n’a fourni les propriétés d’adresse de l’expéditeur, le spouleur MAPI tente de les remplir en appelant la méthode [IMAPISession::QueryIdentity](imapisession-queryidentity.md) pour un identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ebd38-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="ebd38-118">Si aucun identificateur d’entrée n’ont été fournies, le spouleur MAPI stocke « Inconnue » dans toutes les propriétés d’adresse d’expéditeur de type PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="ebd38-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ebd38-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ebd38-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ebd38-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ebd38-120">Protocol specifications</span></span>

<span data-ttu-id="ebd38-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebd38-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebd38-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="ebd38-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ebd38-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebd38-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebd38-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="ebd38-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ebd38-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebd38-125">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebd38-126">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ebd38-126">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ebd38-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebd38-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebd38-128">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="ebd38-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ebd38-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebd38-129">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebd38-130">Spécifie les propriétés et les opérations qui sont autorisées pour publier des objets.</span><span class="sxs-lookup"><span data-stu-id="ebd38-130">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="ebd38-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebd38-131">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebd38-132">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les objets de liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="ebd38-132">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
<span data-ttu-id="ebd38-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebd38-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebd38-134">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="ebd38-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ebd38-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ebd38-135">Header files</span></span>

<span data-ttu-id="ebd38-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebd38-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ebd38-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ebd38-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ebd38-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ebd38-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ebd38-139">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ebd38-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebd38-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd38-140">See also</span></span>



[<span data-ttu-id="ebd38-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd38-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ebd38-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd38-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ebd38-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd38-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ebd38-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ebd38-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

