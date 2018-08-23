---
title: Propriété canonique PidTagHasAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 505f9bb80c86b956cd920348f2120f7fc8494d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587501"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="bc86c-103">Propriété canonique PidTagHasAttachments</span><span class="sxs-lookup"><span data-stu-id="bc86c-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="bc86c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc86c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc86c-105">Contient la valeur TRUE si un message contient au moins une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="bc86c-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc86c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bc86c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc86c-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="bc86c-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="bc86c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bc86c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc86c-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="bc86c-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="bc86c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bc86c-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc86c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bc86c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bc86c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bc86c-112">Area:</span></span>  <br/> |<span data-ttu-id="bc86c-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="bc86c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc86c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bc86c-114">Remarks</span></span>

<span data-ttu-id="bc86c-115">La banque de messages copie cette propriété à partir de l’indicateur **MSGFLAG_HASATTACH** de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bc86c-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="bc86c-116">Une application cliente pouvez ensuite utiliser **PR_HASATTACH** pour effectuer un tri sur les pièces jointes des messages dans l’Observateur d’un message.</span><span class="sxs-lookup"><span data-stu-id="bc86c-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="bc86c-117">La valeur de que cette propriété est mis à jour avec la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="bc86c-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bc86c-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bc86c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc86c-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="bc86c-119">Protocol specifications</span></span>

<span data-ttu-id="bc86c-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc86c-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc86c-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="bc86c-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc86c-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bc86c-122">Header files</span></span>

<span data-ttu-id="bc86c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc86c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc86c-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bc86c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc86c-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="bc86c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="bc86c-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="bc86c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc86c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc86c-127">See also</span></span>



[<span data-ttu-id="bc86c-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bc86c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc86c-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bc86c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc86c-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bc86c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc86c-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bc86c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

