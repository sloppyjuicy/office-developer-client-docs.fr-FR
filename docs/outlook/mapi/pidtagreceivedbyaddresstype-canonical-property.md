---
title: Propriété canonique PidTagReceivedByAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cd7a287a2240d372edf6cca6bac522266c0ca620
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581166"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="0f053-103">Propriété canonique PidTagReceivedByAddressType</span><span class="sxs-lookup"><span data-stu-id="0f053-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="0f053-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f053-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f053-105">Contient le type d’adresse e-mail, par exemple SMTP, de l’utilisateur de messagerie qui ne reçoive effectivement le message.</span><span class="sxs-lookup"><span data-stu-id="0f053-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f053-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0f053-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f053-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="0f053-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="0f053-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0f053-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f053-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="0f053-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="0f053-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0f053-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f053-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f053-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0f053-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0f053-112">Area:</span></span>  <br/> |<span data-ttu-id="0f053-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="0f053-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f053-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f053-114">Remarks</span></span>

<span data-ttu-id="0f053-115">Ces propriétés sont des exemples de propriétés d’adresse de l’utilisateur de messagerie qui ne reçoive effectivement le message.</span><span class="sxs-lookup"><span data-stu-id="0f053-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="0f053-116">Elles doivent être définies par le fournisseur de transport entrant.</span><span class="sxs-lookup"><span data-stu-id="0f053-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="0f053-117">La chaîne de type d’adresse peut contenir uniquement des caractères alphabétiques majuscules A à Z et les numéros de zéro à neuf.</span><span class="sxs-lookup"><span data-stu-id="0f053-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="0f053-118">Ces propriétés qualifier la propriété **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) en spécifiant un type d’adresse, tels que SMTP, en indiquant comment l’adresse doit être créée.</span><span class="sxs-lookup"><span data-stu-id="0f053-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f053-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0f053-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f053-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0f053-120">Protocol specifications</span></span>

<span data-ttu-id="0f053-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f053-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f053-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="0f053-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f053-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f053-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f053-124">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="0f053-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f053-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0f053-125">Header files</span></span>

<span data-ttu-id="0f053-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f053-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f053-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0f053-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f053-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0f053-128">Mapitags.h</span></span>
  
> <span data-ttu-id="0f053-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0f053-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f053-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f053-130">See also</span></span>



[<span data-ttu-id="0f053-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0f053-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f053-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0f053-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f053-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0f053-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f053-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0f053-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

