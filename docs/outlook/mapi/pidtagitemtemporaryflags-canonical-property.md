---
title: Propriété canonique PidTagItemTemporaryflags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: df2fa19656aa1bff810a082cda94a091e2c7fc9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786167"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="c75a8-103">Propriété canonique PidTagItemTemporaryflags</span><span class="sxs-lookup"><span data-stu-id="c75a8-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="c75a8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c75a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c75a8-105">Contient un indicateur qui indique qu’un message a été lu, mais ne pas marqué comme lus.</span><span class="sxs-lookup"><span data-stu-id="c75a8-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c75a8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c75a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c75a8-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="c75a8-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="c75a8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c75a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c75a8-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="c75a8-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="c75a8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c75a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="c75a8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c75a8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c75a8-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="c75a8-112">Area:</span></span>  <br/> |<span data-ttu-id="c75a8-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="c75a8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c75a8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c75a8-114">Remarks</span></span>

<span data-ttu-id="c75a8-115">Cette propriété est utilisée dans le dossier de recherche de Messages non lus d’Outlook pour suivre les messages qui ont été lus sans réellement les marquer comme lu, les supprimer à partir du dossier.</span><span class="sxs-lookup"><span data-stu-id="c75a8-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="c75a8-116">Lorsque cette propriété est supprimée les modifications d’affichage et de l’élément est marqué comme étant en lecture.</span><span class="sxs-lookup"><span data-stu-id="c75a8-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="c75a8-117">Cette propriété ne sera pas synchronisé sur le serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="c75a8-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c75a8-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c75a8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c75a8-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c75a8-119">Protocol specifications</span></span>

<span data-ttu-id="c75a8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c75a8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c75a8-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c75a8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c75a8-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c75a8-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c75a8-123">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="c75a8-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c75a8-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c75a8-124">Header files</span></span>

<span data-ttu-id="c75a8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c75a8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c75a8-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c75a8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c75a8-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c75a8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c75a8-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c75a8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c75a8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c75a8-129">See also</span></span>



[<span data-ttu-id="c75a8-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c75a8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c75a8-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c75a8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c75a8-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c75a8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c75a8-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c75a8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

