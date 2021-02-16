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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331870"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="acd5a-103">Propriété canonique PidTagContentUnreadCount</span><span class="sxs-lookup"><span data-stu-id="acd5a-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="acd5a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acd5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acd5a-105">Contient le nombre de messages non lus dans un dossier, tel que calculé par la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="acd5a-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="acd5a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="acd5a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="acd5a-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="acd5a-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="acd5a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="acd5a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="acd5a-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="acd5a-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="acd5a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="acd5a-110">Data type:</span></span>  <br/> |<span data-ttu-id="acd5a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="acd5a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="acd5a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="acd5a-112">Area:</span></span>  <br/> |<span data-ttu-id="acd5a-113">Folder</span><span class="sxs-lookup"><span data-stu-id="acd5a-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acd5a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="acd5a-114">Remarks</span></span>

<span data-ttu-id="acd5a-115">Cette propriété calculée par la magasin de messages est utilisée à deux fins différentes, bien qu’associées.</span><span class="sxs-lookup"><span data-stu-id="acd5a-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="acd5a-116">Sur un objet de dossier MAPI, il contient le nombre de messages dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="acd5a-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="acd5a-117">Dans une ligne de titre des tableaux MAPI classés, il contient le nombre de messages non associés non lus dans la catégorie correspondant à cette ligne de titre.</span><span class="sxs-lookup"><span data-stu-id="acd5a-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="acd5a-118">Cette propriété contient le nombre de messages dans la table de contenu du dossier pour lesquels l’indicateur MSGFLAG_READ n’est pas définie dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="acd5a-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="acd5a-119">La **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contient le nombre total de messages pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="acd5a-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="acd5a-120">Les **PR_CONTENT_COUNT** et cette propriété sont en lecture seule pour les clients.</span><span class="sxs-lookup"><span data-stu-id="acd5a-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="acd5a-121">Certaines applications clientes affichent la ligne de titre d’une catégorie différemment en fonction de la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="acd5a-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="acd5a-122">Par exemple, un client peut afficher une catégorie qui inclut des messages non lus en gras.</span><span class="sxs-lookup"><span data-stu-id="acd5a-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="acd5a-123">Cette propriété ne peut pas être utilisée en tant que catégorie et si vous tentez de le faire, la valeur MAPI_E_INVALID_PARAMETER est renvoyée à partir de la méthode [IMAPITable::SortTable.](imapitable-sorttable.md)</span><span class="sxs-lookup"><span data-stu-id="acd5a-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="acd5a-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="acd5a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="acd5a-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="acd5a-125">Protocol specifications</span></span>

<span data-ttu-id="acd5a-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="acd5a-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="acd5a-127">Fournit des références aux spécifications Microsoft Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="acd5a-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="acd5a-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="acd5a-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="acd5a-129">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="acd5a-129">Handles folder operations.</span></span>
    
<span data-ttu-id="acd5a-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="acd5a-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="acd5a-131">Inclut les opérations autorisées pour les objets de table principale.</span><span class="sxs-lookup"><span data-stu-id="acd5a-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="acd5a-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="acd5a-132">Header files</span></span>

<span data-ttu-id="acd5a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="acd5a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="acd5a-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="acd5a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="acd5a-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="acd5a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="acd5a-136">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="acd5a-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="acd5a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acd5a-137">See also</span></span>



[<span data-ttu-id="acd5a-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="acd5a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="acd5a-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="acd5a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="acd5a-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="acd5a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="acd5a-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="acd5a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

