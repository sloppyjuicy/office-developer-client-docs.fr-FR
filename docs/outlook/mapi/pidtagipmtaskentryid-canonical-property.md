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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c3845c745dcd2c18525f147308233b94fbce70d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327842"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a><span data-ttu-id="af4fb-103">Propriété canonique PidTagIpmTaskEntryId</span><span class="sxs-lookup"><span data-stu-id="af4fb-103">PidTagIpmTaskEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="af4fb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af4fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af4fb-105">Contient **l’EntryID** du dossier Outlook tâches.</span><span class="sxs-lookup"><span data-stu-id="af4fb-105">Contains the **EntryID** of the Outlook Tasks folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af4fb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="af4fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af4fb-107">PR_IPM_TASK_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="af4fb-107">PR_IPM_TASK_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="af4fb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="af4fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af4fb-109">0x36D4</span><span class="sxs-lookup"><span data-stu-id="af4fb-109">0x36D4</span></span>  <br/> |
|<span data-ttu-id="af4fb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="af4fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="af4fb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="af4fb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="af4fb-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="af4fb-112">Area:</span></span>  <br/> |<span data-ttu-id="af4fb-113">Dossier</span><span class="sxs-lookup"><span data-stu-id="af4fb-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af4fb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="af4fb-114">Remarks</span></span>

<span data-ttu-id="af4fb-115">Cette propriété est lue ou écrite à l’aide du protocole Property et Stream Object.</span><span class="sxs-lookup"><span data-stu-id="af4fb-115">This property is read or written by using the Property and Stream Object protocol.</span></span> <span data-ttu-id="af4fb-116">Il est lu et écrit dans la boîte de réception ou le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="af4fb-116">It is read from and written to the Inbox or Root folder.</span></span> <span data-ttu-id="af4fb-117">L’implémentation doit utiliser le dossier Boîte de réception lorsque le magasin est celui de l’utilisateur de messagerie principal, et doit utiliser le dossier racine lorsque le magasin est celui d’un utilisateur délégué.</span><span class="sxs-lookup"><span data-stu-id="af4fb-117">The implementation must use the Inbox folder when the store is that of the primary messaging user, and it must use the Root folder when the store is that of a delegate user.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af4fb-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="af4fb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af4fb-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="af4fb-119">Protocol specifications</span></span>

<span data-ttu-id="af4fb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af4fb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af4fb-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="af4fb-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af4fb-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af4fb-122">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af4fb-123">Spécifie les propriétés et opérations permettant de créer et de localiser les dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="af4fb-123">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="af4fb-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af4fb-124">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af4fb-125">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="af4fb-125">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af4fb-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="af4fb-126">Header files</span></span>

<span data-ttu-id="af4fb-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af4fb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="af4fb-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="af4fb-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="af4fb-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af4fb-129">Mapitags.h</span></span>
  
> <span data-ttu-id="af4fb-130">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="af4fb-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af4fb-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af4fb-131">See also</span></span>



[<span data-ttu-id="af4fb-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="af4fb-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af4fb-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="af4fb-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af4fb-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="af4fb-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af4fb-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="af4fb-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

