---
title: Propriété canonique PidTagSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEntryId
api_type:
- COM
ms.assetid: 9f311dd2-853e-46f7-966a-c2ab7a1fb6c5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f2e8ecba7c92dcbcb719591464e10fb4af2d2344
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591764"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="ca3cc-103">Propriété canonique PidTagSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="ca3cc-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ca3cc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca3cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca3cc-105">Contient l’identificateur d’entrée de l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca3cc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ca3cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca3cc-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ca3cc-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ca3cc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ca3cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca3cc-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="ca3cc-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="ca3cc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ca3cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca3cc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ca3cc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ca3cc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ca3cc-112">Area:</span></span>  <br/> |<span data-ttu-id="ca3cc-113">Address</span><span class="sxs-lookup"><span data-stu-id="ca3cc-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca3cc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca3cc-114">Remarks</span></span>

<span data-ttu-id="ca3cc-115">Cette propriété est une des propriétés d’adresse pour l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="ca3cc-116">Elle doit être définie par le fournisseur de transport sortant, qui ne doit jamais propager toutes les valeurs existantes.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="ca3cc-117">Si aucun fournisseur de transport n’a fourni les propriétés d’adresse de l’expéditeur, le spouleur MAPI tente de les remplir en appelant la méthode [IMAPISession::QueryIdentity](imapisession-queryidentity.md) pour un identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="ca3cc-118">Si aucune entrée d’identificateurs ont été fournies, le spouleur MAPI un identificateur correspondant à la chaîne « Inconnue » dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ca3cc-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ca3cc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca3cc-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ca3cc-120">Protocol specifications</span></span>

<span data-ttu-id="ca3cc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3cc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3cc-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca3cc-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3cc-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3cc-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="ca3cc-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3cc-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3cc-126">Spécifie les propriétés et les opérations qui représentent les éléments RSS.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="ca3cc-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3cc-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3cc-128">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ca3cc-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3cc-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3cc-130">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ca3cc-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3cc-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3cc-132">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="ca3cc-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca3cc-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca3cc-134">Spécifie les propriétés et les opérations qui sont autorisées pour publier des objets.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca3cc-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ca3cc-135">Header files</span></span>

<span data-ttu-id="ca3cc-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca3cc-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca3cc-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca3cc-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ca3cc-138">Mapitags.h</span></span>
  
> <span data-ttu-id="ca3cc-139">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ca3cc-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca3cc-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca3cc-140">See also</span></span>



[<span data-ttu-id="ca3cc-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ca3cc-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca3cc-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ca3cc-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca3cc-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ca3cc-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca3cc-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ca3cc-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

