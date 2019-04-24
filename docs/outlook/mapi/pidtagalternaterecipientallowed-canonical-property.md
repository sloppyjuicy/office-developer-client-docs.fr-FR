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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0faeb12ee54ec5d1c584bacd51590b157035f4fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327985"
---
# <a name="pidtagalternaterecipientallowed-canonical-property"></a><span data-ttu-id="b0259-103">Propriété canonique PidTagAlternateRecipientAllowed</span><span class="sxs-lookup"><span data-stu-id="b0259-103">PidTagAlternateRecipientAllowed Canonical Property</span></span>

  
  
<span data-ttu-id="b0259-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0259-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0259-105">Contient la valeur TRUE si l'expéditeur autorise le transfert automatique de ce message.</span><span class="sxs-lookup"><span data-stu-id="b0259-105">Contains TRUE if the sender permits auto forwarding of this message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0259-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b0259-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0259-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="b0259-107">PR_ALTERNATE_RECIPIENT_ALLOWED</span></span>  <br/> |
|<span data-ttu-id="b0259-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b0259-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0259-109">0x0002</span><span class="sxs-lookup"><span data-stu-id="b0259-109">0x0002</span></span>  <br/> |
|<span data-ttu-id="b0259-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b0259-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0259-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b0259-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b0259-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b0259-112">Area:</span></span>  <br/> |<span data-ttu-id="b0259-113">Address</span><span class="sxs-lookup"><span data-stu-id="b0259-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0259-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0259-114">Remarks</span></span>

<span data-ttu-id="b0259-115">Si le transfert automatique n'est pas autorisé ou si aucun autre destinataire n'a été désigné, un rapport de non-remise doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b0259-115">If auto forwarding is not permitted or if no alternate recipient has been designated, a nondelivery report should be generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b0259-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="b0259-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0259-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b0259-117">Protocol specifications</span></span>

<span data-ttu-id="b0259-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0259-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0259-119">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b0259-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0259-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0259-120">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0259-121">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="b0259-121">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b0259-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0259-122">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0259-123">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="b0259-123">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b0259-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0259-124">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0259-125">Encode et décode les objets message et Attachment en une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="b0259-125">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0259-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="b0259-126">Header files</span></span>

<span data-ttu-id="b0259-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b0259-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0259-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b0259-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0259-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b0259-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b0259-130">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="b0259-130">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0259-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0259-131">See also</span></span>



[<span data-ttu-id="b0259-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b0259-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0259-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b0259-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0259-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b0259-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0259-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b0259-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

