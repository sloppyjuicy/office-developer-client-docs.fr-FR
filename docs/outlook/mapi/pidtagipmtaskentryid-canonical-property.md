---
title: Propriété canonique PidTagIpmTaskEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aa1c4979ce66a0e32aea7b04ef4412679545b3de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786158"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="d934c-103">Propriété canonique PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="d934c-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d934c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d934c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d934c-105">Contient **propriété EntryID** du dossier tâches Outlook.</span><span class="sxs-lookup"><span data-stu-id="d934c-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d934c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d934c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d934c-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d934c-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d934c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d934c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d934c-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="d934c-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="d934c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d934c-110">Data type:</span></span>  <br/> |<span data-ttu-id="d934c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d934c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d934c-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="d934c-112">Area:</span></span>  <br/> |<span data-ttu-id="d934c-113">Folder</span><span class="sxs-lookup"><span data-stu-id="d934c-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d934c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d934c-114">Remarks</span></span>

<span data-ttu-id="d934c-115">Cette propriété est lu ou écrite à l’aide du protocole de la propriété et l’objet Stream.</span><span class="sxs-lookup"><span data-stu-id="d934c-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="d934c-116">Il est lu à partir d’et écrit dans le dossier boîte de réception ou racine.</span><span class="sxs-lookup"><span data-stu-id="d934c-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="d934c-117">L’implémentation doit utiliser le dossier boîte de réception lorsque le magasin est celui de l’utilisateur de messagerie principale, et elle doit utiliser le dossier racine lorsque la banque est celui d’un utilisateur délégué.</span><span class="sxs-lookup"><span data-stu-id="d934c-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d934c-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d934c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d934c-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d934c-119">Protocol specifications</span></span>

<span data-ttu-id="d934c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d934c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d934c-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="d934c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d934c-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d934c-122">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d934c-123">Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="d934c-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="d934c-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d934c-124">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d934c-125">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d934c-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d934c-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d934c-126">Header files</span></span>

<span data-ttu-id="d934c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d934c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d934c-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d934c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d934c-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d934c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d934c-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="d934c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d934c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d934c-131">See also</span></span>



[<span data-ttu-id="d934c-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d934c-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d934c-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d934c-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d934c-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d934c-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d934c-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="d934c-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

