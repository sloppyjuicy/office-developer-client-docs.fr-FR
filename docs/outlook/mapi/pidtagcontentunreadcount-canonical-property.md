---
title: Propriété canonique PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ce7092840037345ae99b31c39cfbd4ac96b99ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785870"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="ebb45-103">Propriété canonique PidTagContentUnreadCount</span><span class="sxs-lookup"><span data-stu-id="ebb45-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="ebb45-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebb45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebb45-105">Contient le nombre de messages non lus dans un dossier, calculé par la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="ebb45-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ebb45-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ebb45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ebb45-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="ebb45-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="ebb45-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ebb45-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ebb45-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="ebb45-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="ebb45-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ebb45-110">Data type:</span></span>  <br/> |<span data-ttu-id="ebb45-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ebb45-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ebb45-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ebb45-112">Area:</span></span>  <br/> |<span data-ttu-id="ebb45-113">Folder</span><span class="sxs-lookup"><span data-stu-id="ebb45-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebb45-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebb45-114">Remarks</span></span>

<span data-ttu-id="ebb45-115">Cette propriété calculée par la banque de messages est utilisée pour les deux, même si associées, à des fins.</span><span class="sxs-lookup"><span data-stu-id="ebb45-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="ebb45-116">Dans un objet de dossier MAPI, il contient le nombre de messages dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="ebb45-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="ebb45-117">Dans une ligne d’en-tête dans les tableaux MAPI par catégorie, il contient le nombre de messages non lus non associés dans les catégories correspondant à cette ligne d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="ebb45-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="ebb45-118">Cette propriété contient le nombre de messages dans le tableau contenu de dossier pour lequel l’indicateur MSGFLAG_READ n’est pas définie dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ebb45-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="ebb45-119">La propriété **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contient le nombre total de messages pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="ebb45-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="ebb45-120">Le **PR_CONTENT_COUNT** et cette propriété sont en lecture seule aux clients.</span><span class="sxs-lookup"><span data-stu-id="ebb45-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="ebb45-121">Certaines applications clientes affichent la ligne d’en-tête d’une catégorie différemment selon la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ebb45-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="ebb45-122">Par exemple, un client peut afficher une catégorie qui inclut des messages non lus en gras.</span><span class="sxs-lookup"><span data-stu-id="ebb45-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="ebb45-123">Cette propriété ne peut pas être utilisée comme une catégorie et une tentative pour cela se traduit par la valeur MAPI_E_INVALID_PARAMETER est renvoyé par la méthode [IMAPITable::SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="ebb45-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ebb45-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ebb45-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ebb45-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ebb45-125">Protocol specifications</span></span>

<span data-ttu-id="ebb45-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebb45-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebb45-127">Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ebb45-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ebb45-128">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebb45-128">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebb45-129">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="ebb45-129">Handles folder operations.</span></span>
    
<span data-ttu-id="ebb45-130">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebb45-130">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebb45-131">Inclut les opérations autorisées pour les objets de la table principale.</span><span class="sxs-lookup"><span data-stu-id="ebb45-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ebb45-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ebb45-132">Header files</span></span>

<span data-ttu-id="ebb45-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebb45-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ebb45-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ebb45-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ebb45-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ebb45-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ebb45-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ebb45-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebb45-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebb45-137">See also</span></span>



[<span data-ttu-id="ebb45-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ebb45-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ebb45-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ebb45-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ebb45-140">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ebb45-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ebb45-141">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ebb45-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

