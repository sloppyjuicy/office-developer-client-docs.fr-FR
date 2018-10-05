---
title: Propriété canonique PidTagAlternateRecipientAllowed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipientAllowed
api_type:
- HeaderDef
ms.assetid: dbbdeb54-3d14-4601-a77b-55ee31f33416
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0faeb12ee54ec5d1c584bacd51590b157035f4fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385955"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="9336f-103">Propriété canonique PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="9336f-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="9336f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9336f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9336f-105">Contient la valeur TRUE si l’expéditeur permet le transfert automatique de ce message.</span><span class="sxs-lookup"><span data-stu-id="9336f-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9336f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9336f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9336f-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="9336f-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="9336f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9336f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9336f-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="9336f-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="9336f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9336f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9336f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9336f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9336f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9336f-112">Area:</span></span>  <br/> |<span data-ttu-id="9336f-113">Address</span><span class="sxs-lookup"><span data-stu-id="9336f-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9336f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9336f-114">Remarks</span></span>

<span data-ttu-id="9336f-115">Si le transfert automatique n’est pas autorisé ou si aucune autre destinataire n’a été désigné, un rapport de non-remise doit être généré.</span><span class="sxs-lookup"><span data-stu-id="9336f-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9336f-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9336f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9336f-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9336f-117">Protocol specifications</span></span>

<span data-ttu-id="9336f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9336f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9336f-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="9336f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9336f-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9336f-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9336f-121">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="9336f-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9336f-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9336f-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9336f-123">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="9336f-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="9336f-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9336f-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9336f-125">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="9336f-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9336f-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9336f-126">Header files</span></span>

<span data-ttu-id="9336f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9336f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9336f-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9336f-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="9336f-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9336f-129">Mapitags.h</span></span>
  
> <span data-ttu-id="9336f-130">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="9336f-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9336f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9336f-131">See also</span></span>



[<span data-ttu-id="9336f-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9336f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9336f-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9336f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9336f-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9336f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9336f-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9336f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

