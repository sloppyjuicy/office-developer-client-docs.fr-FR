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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 10dd12522a635098908285f1a9ee16c93d96f728
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383547"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="e566f-103">Propriété canonique PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="e566f-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="e566f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e566f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e566f-105">Contient les noms des contacts associés à l’élément.</span><span class="sxs-lookup"><span data-stu-id="e566f-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e566f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e566f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e566f-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="e566f-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="e566f-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="e566f-108">Property set:</span></span>  <br/> |<span data-ttu-id="e566f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e566f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e566f-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="e566f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e566f-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="e566f-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="e566f-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e566f-112">Data type:</span></span>  <br/> |<span data-ttu-id="e566f-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e566f-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e566f-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e566f-114">Area:</span></span>  <br/> |<span data-ttu-id="e566f-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="e566f-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e566f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e566f-116">Remarks</span></span>

<span data-ttu-id="e566f-117">Cette propriété contient la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de chaque carnet d’adresses **EntryID** qui est référencée dans la valeur de propriété **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e566f-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="e566f-118">Il peut inclure des noms non référencés dans **dispidContactLinkEntry**.</span><span class="sxs-lookup"><span data-stu-id="e566f-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e566f-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e566f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e566f-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e566f-120">Protocol specifications</span></span>

<span data-ttu-id="e566f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e566f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e566f-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e566f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e566f-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e566f-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e566f-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="e566f-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e566f-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e566f-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e566f-126">Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="e566f-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="e566f-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e566f-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e566f-128">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e566f-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e566f-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e566f-129">Header files</span></span>

<span data-ttu-id="e566f-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e566f-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="e566f-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e566f-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e566f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e566f-132">See also</span></span>



[<span data-ttu-id="e566f-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e566f-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e566f-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e566f-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e566f-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e566f-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e566f-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e566f-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

