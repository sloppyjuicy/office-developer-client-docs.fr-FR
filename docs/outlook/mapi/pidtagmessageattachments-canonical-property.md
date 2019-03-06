---
title: Propriété canonique PidTagMessageAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 43cff5789e0a0a8cda11277c1a636c8b32d28cdb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30413972"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="9134a-103">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="9134a-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="9134a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9134a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9134a-105">Contient un tableau de pièces jointes pour un message.</span><span class="sxs-lookup"><span data-stu-id="9134a-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9134a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9134a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9134a-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="9134a-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="9134a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9134a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9134a-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="9134a-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="9134a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9134a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9134a-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="9134a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="9134a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9134a-112">Area:</span></span>  <br/> |<span data-ttu-id="9134a-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="9134a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9134a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9134a-114">Remarks</span></span>

<span data-ttu-id="9134a-115">Cette propriété peut être exclue dans [IMAPIProp:: CopyTo](imapiprop-copyto.md) Operations ou incluse dans [IMAPIProp:: CopyProps](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="9134a-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="9134a-116">En tant que propriété de type PT_OBJECT, elle ne peut pas être récupérée avec succès par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="9134a-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="9134a-117">Son contenu doit être accessible à l'aide de la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , qui demande l'identificateur d'interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="9134a-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="9134a-118">Les fournisseurs de services doivent le signaler à la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) s'il est défini, mais éventuellement le signaler ou non s'il n'est pas défini.</span><span class="sxs-lookup"><span data-stu-id="9134a-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="9134a-119">Pour récupérer le contenu de la table, une application cliente doit appeler la méthode [IMessage:: GetAttachmentTable](imessage-getattachmenttable.md) .</span><span class="sxs-lookup"><span data-stu-id="9134a-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="9134a-120">For more information, see [Tables des pi�ces jointes](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="9134a-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="9134a-121">Cette propriété peut être utilisée pour la restriction de sous-objet en la spécifiant dans la structure [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="9134a-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="9134a-122">Cela permet au client de limiter l'affichage d'un conteneur aux messages dont les pièces jointes répondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9134a-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="9134a-123">Un message qualifie l'affichage si au moins une ligne dans son tableau de pièces jointes, c'est-à-dire une pièce jointe, répond à la restriction de sous-objet.</span><span class="sxs-lookup"><span data-stu-id="9134a-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9134a-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="9134a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9134a-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9134a-125">Protocol specifications</span></span>

<span data-ttu-id="9134a-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9134a-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9134a-127">Définit les structures de données de base qui sont utilisées dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="9134a-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="9134a-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9134a-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9134a-129">Définit les structures de données de base qui sont utilisées dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="9134a-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="9134a-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9134a-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9134a-131">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="9134a-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9134a-132">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="9134a-132">Header files</span></span>

<span data-ttu-id="9134a-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9134a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="9134a-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9134a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="9134a-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9134a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="9134a-136">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="9134a-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9134a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9134a-137">See also</span></span>



[<span data-ttu-id="9134a-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9134a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9134a-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9134a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9134a-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9134a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9134a-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9134a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

