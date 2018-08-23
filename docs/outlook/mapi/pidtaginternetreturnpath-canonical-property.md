---
title: Propriété canonique PidTagInternetReturnPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReturnPath
api_type:
- HeaderDef
ms.assetid: 4530dbcf-9436-4f29-b79e-1bb0f791f60b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b3f108ff1053c0aa1046597cd2f11b74bc2dab0c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574173"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="07606-103">Propriété canonique PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="07606-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="07606-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07606-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07606-105">Contient la valeur du champ d’en-tête d’un message Multipurpose Internet Mail Extensions (MIME) chemin de retour.</span><span class="sxs-lookup"><span data-stu-id="07606-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="07606-106">L’adresse de messagerie de l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="07606-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07606-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="07606-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="07606-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="07606-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="07606-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="07606-109">Identifier:</span></span>  <br/> |<span data-ttu-id="07606-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="07606-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="07606-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="07606-111">Data type:</span></span>  <br/> |<span data-ttu-id="07606-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="07606-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="07606-113">Domaine :</span><span class="sxs-lookup"><span data-stu-id="07606-113">Area:</span></span>  <br/> |<span data-ttu-id="07606-114">MIME</span><span class="sxs-lookup"><span data-stu-id="07606-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07606-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="07606-115">Remarks</span></span>

<span data-ttu-id="07606-116">Pour récupérer la valeur de cette propriété, tout d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="07606-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="07606-117">Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="07606-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07606-118">lpGuid :</span><span class="sxs-lookup"><span data-stu-id="07606-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="07606-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="07606-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="07606-120">ulKind :</span><span class="sxs-lookup"><span data-stu-id="07606-120">ulKind:</span></span>  <br/> |<span data-ttu-id="07606-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="07606-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="07606-122">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="07606-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="07606-123">L « chemin de retour »</span><span class="sxs-lookup"><span data-stu-id="07606-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="07606-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="07606-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07606-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="07606-125">Protocol specifications</span></span>

<span data-ttu-id="07606-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07606-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07606-127">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="07606-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07606-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07606-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07606-129">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="07606-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07606-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="07606-130">Header files</span></span>

<span data-ttu-id="07606-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07606-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="07606-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="07606-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="07606-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="07606-133">Mapitags.h</span></span>
  
> <span data-ttu-id="07606-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="07606-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07606-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07606-135">See also</span></span>



[<span data-ttu-id="07606-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="07606-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07606-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="07606-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="07606-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="07606-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07606-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="07606-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07606-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="07606-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

