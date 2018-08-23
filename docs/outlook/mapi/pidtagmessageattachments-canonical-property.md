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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b375ef279fc50aecca75b60d8379438c56f13420
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569336"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="b4608-103">Propriété canonique PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="b4608-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="b4608-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4608-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4608-105">Contient un tableau des restrictions qui peuvent être appliqués à un tableau de contenu pour trouver tous les messages qui contiennent les sous-objets de pièce jointe répondant aux restrictions.</span><span class="sxs-lookup"><span data-stu-id="b4608-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain attachment subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4608-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b4608-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4608-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="b4608-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="b4608-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b4608-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4608-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="b4608-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="b4608-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b4608-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4608-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b4608-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b4608-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b4608-112">Area:</span></span>  <br/> |<span data-ttu-id="b4608-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="b4608-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4608-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4608-114">Remarks</span></span>

<span data-ttu-id="b4608-115">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="b4608-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="b4608-116">En tant que propriété de type PT_OBJECT, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="b4608-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="b4608-117">Son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande l’identificateur d’interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="b4608-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="b4608-118">Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) si elle est définie, mais peut le signaler ou pas si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="b4608-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="b4608-119">Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) .</span><span class="sxs-lookup"><span data-stu-id="b4608-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="b4608-120">For more information, see [Tables des pi�ces jointes](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b4608-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="b4608-121">Cette propriété peut être utilisée pour la restriction sous-objet en le définissant dans la structure [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="b4608-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="b4608-122">Ainsi, le client limiter l’affichage d’un conteneur pour les messages contenant des pièces jointes de réunion critère donné.</span><span class="sxs-lookup"><span data-stu-id="b4608-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="b4608-123">Un message satisfait aux conditions requises pour l’affichage si au moins une ligne dans sa table de pièces jointes, c'est-à-dire, une pièce jointe, satisfait à la restriction sous-objet.</span><span class="sxs-lookup"><span data-stu-id="b4608-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b4608-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b4608-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4608-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b4608-125">Protocol specifications</span></span>

<span data-ttu-id="b4608-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4608-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4608-127">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="b4608-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="b4608-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4608-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4608-129">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="b4608-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="b4608-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4608-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4608-131">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="b4608-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4608-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b4608-132">Header files</span></span>

<span data-ttu-id="b4608-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4608-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4608-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b4608-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4608-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b4608-135">Mapitags.h</span></span>
  
> <span data-ttu-id="b4608-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="b4608-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4608-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4608-137">See also</span></span>



[<span data-ttu-id="b4608-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b4608-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4608-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b4608-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4608-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b4608-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4608-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b4608-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

