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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ec092e6cc6174e156dbfe7784143c9d74715eef7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357700"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="b7bf3-103">Propriété canonique PidTagItemTemporaryflags</span><span class="sxs-lookup"><span data-stu-id="b7bf3-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="b7bf3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7bf3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7bf3-105">Contient un indicateur qui indique qu’un message a été lu, mais pas marqué comme lu.</span><span class="sxs-lookup"><span data-stu-id="b7bf3-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7bf3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b7bf3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7bf3-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="b7bf3-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="b7bf3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b7bf3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b7bf3-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="b7bf3-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="b7bf3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b7bf3-110">Data type:</span></span>  <br/> |<span data-ttu-id="b7bf3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b7bf3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b7bf3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b7bf3-112">Area:</span></span>  <br/> |<span data-ttu-id="b7bf3-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="b7bf3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7bf3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7bf3-114">Remarks</span></span>

<span data-ttu-id="b7bf3-115">Cette propriété est utilisée dans le dossier de recherche Messages non lus de Outlook pour effectuer le suivi des messages qui ont été lus sans les marquer comme lus, ce qui les supprimerait du dossier.</span><span class="sxs-lookup"><span data-stu-id="b7bf3-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="b7bf3-116">Lorsque l’affichage change, cette propriété est supprimée et l’élément est marqué comme lu.</span><span class="sxs-lookup"><span data-stu-id="b7bf3-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="b7bf3-117">Cette propriété ne sera pas synchronisée avec le Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b7bf3-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7bf3-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b7bf3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7bf3-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b7bf3-119">Protocol specifications</span></span>

<span data-ttu-id="b7bf3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7bf3-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7bf3-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="b7bf3-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7bf3-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7bf3-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7bf3-123">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="b7bf3-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7bf3-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b7bf3-124">Header files</span></span>

<span data-ttu-id="b7bf3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7bf3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7bf3-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b7bf3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="b7bf3-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b7bf3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="b7bf3-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="b7bf3-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7bf3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7bf3-129">See also</span></span>



[<span data-ttu-id="b7bf3-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b7bf3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7bf3-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b7bf3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7bf3-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b7bf3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7bf3-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b7bf3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

