---
title: Propriété canonique PidLidContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContacts
api_type:
- COM
ms.assetid: 709e701f-b24e-4cd5-8c55-3f9e67f67a4a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6182c9dfc0c4de24bd587e626fe74d02ed23968b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785102"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="95ca9-103">Propriété canonique PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="95ca9-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="95ca9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95ca9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95ca9-105">Contient les noms des contacts associés à l’élément.</span><span class="sxs-lookup"><span data-stu-id="95ca9-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="95ca9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="95ca9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95ca9-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="95ca9-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="95ca9-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="95ca9-108">Property set:</span></span>  <br/> |<span data-ttu-id="95ca9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="95ca9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="95ca9-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="95ca9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="95ca9-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="95ca9-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="95ca9-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="95ca9-112">Data type:</span></span>  <br/> |<span data-ttu-id="95ca9-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="95ca9-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="95ca9-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="95ca9-114">Area:</span></span>  <br/> |<span data-ttu-id="95ca9-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="95ca9-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95ca9-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="95ca9-116">Remarks</span></span>

<span data-ttu-id="95ca9-117">Cette propriété contient la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de chaque carnet d’adresses **EntryID** qui est référencée dans la valeur de propriété **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="95ca9-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="95ca9-118">Il peut inclure des noms non référencés dans **dispidContactLinkEntry**.</span><span class="sxs-lookup"><span data-stu-id="95ca9-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="95ca9-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="95ca9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95ca9-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="95ca9-120">Protocol specifications</span></span>

<span data-ttu-id="95ca9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95ca9-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95ca9-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="95ca9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="95ca9-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95ca9-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95ca9-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="95ca9-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="95ca9-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95ca9-125">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95ca9-126">Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="95ca9-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="95ca9-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95ca9-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95ca9-128">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="95ca9-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95ca9-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="95ca9-129">Header files</span></span>

<span data-ttu-id="95ca9-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95ca9-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="95ca9-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="95ca9-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95ca9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95ca9-132">See also</span></span>



[<span data-ttu-id="95ca9-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="95ca9-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95ca9-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="95ca9-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95ca9-135">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="95ca9-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95ca9-136">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="95ca9-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

