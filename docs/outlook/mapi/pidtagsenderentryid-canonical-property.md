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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0bc8b8bd76d553cc4e12e331e9fe7047ef7aaf4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358911"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="c20c3-103">Propriété canonique PidTagSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="c20c3-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c20c3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c20c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c20c3-105">Contient l’identificateur d’entrée de l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="c20c3-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c20c3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c20c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c20c3-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c20c3-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c20c3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c20c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c20c3-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="c20c3-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="c20c3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c20c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c20c3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c20c3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c20c3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c20c3-112">Area:</span></span>  <br/> |<span data-ttu-id="c20c3-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="c20c3-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c20c3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c20c3-114">Remarks</span></span>

<span data-ttu-id="c20c3-115">Cette propriété est l’une des propriétés d’adresse de l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="c20c3-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="c20c3-116">Elle doit être définie par le fournisseur de transport sortant, qui ne doit jamais propager les valeurs existantes.</span><span class="sxs-lookup"><span data-stu-id="c20c3-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="c20c3-117">Si aucun fournisseur de transport n’a fourni de propriétés d’adresse d’expéditeur, lepooler MAPI tente de les remplir en appelant la méthode [IMAPISession::QueryIdentity](imapisession-queryidentity.md) pour un identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c20c3-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="c20c3-118">Si aucun identificateur d’entrée n’a été fourni, lepooler MAPI est un identificateur correspondant à la chaîne « Unknown » dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c20c3-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c20c3-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c20c3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c20c3-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="c20c3-120">Protocol specifications</span></span>

<span data-ttu-id="c20c3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c20c3-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c20c3-122">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="c20c3-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c20c3-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c20c3-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c20c3-124">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="c20c3-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c20c3-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c20c3-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c20c3-126">Spécifie les propriétés et les opérations qui représentent des éléments RSS.</span><span class="sxs-lookup"><span data-stu-id="c20c3-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="c20c3-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c20c3-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c20c3-128">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="c20c3-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c20c3-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c20c3-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c20c3-130">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="c20c3-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c20c3-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c20c3-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c20c3-132">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="c20c3-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c20c3-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c20c3-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c20c3-134">Spécifie les propriétés et opérations autorisées pour les objets de publication.</span><span class="sxs-lookup"><span data-stu-id="c20c3-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c20c3-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c20c3-135">Header files</span></span>

<span data-ttu-id="c20c3-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c20c3-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c20c3-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c20c3-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c20c3-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c20c3-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c20c3-139">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="c20c3-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c20c3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c20c3-140">See also</span></span>



[<span data-ttu-id="c20c3-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c20c3-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c20c3-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c20c3-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c20c3-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c20c3-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c20c3-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c20c3-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

