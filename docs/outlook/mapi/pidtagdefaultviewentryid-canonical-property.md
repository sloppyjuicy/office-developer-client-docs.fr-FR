---
title: Propriété canonique PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0db245efdd8aad73b0c094c35079f50925ca4478
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785915"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="ec6c2-103">Propriété canonique PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="ec6c2-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ec6c2-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec6c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec6c2-105">Contient l’identificateur d’entrée de l’affichage de par défaut d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec6c2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ec6c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec6c2-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ec6c2-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ec6c2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ec6c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ec6c2-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="ec6c2-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="ec6c2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ec6c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="ec6c2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ec6c2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ec6c2-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ec6c2-112">Area:</span></span>  <br/> |<span data-ttu-id="ec6c2-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="ec6c2-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec6c2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec6c2-114">Remarks</span></span>

<span data-ttu-id="ec6c2-115">Cette propriété est l’identificateur d’entrée de l’affichage du dossier qui doit être défini en tant que la vue initiale.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="ec6c2-116">La propriété ne doit pas être définie si l’affichage de « Normal » est utilisée en tant que la vue initiale.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="ec6c2-117">Une application cliente peut obtenir cette propriété au moment où qu'il ouvre le dossier et réaliser des gains de performances.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="ec6c2-118">Cette propriété peut être utilisée comme un raccourci pour obtenir la vue par défaut, au lieu d’ouvrir la table de contenu associé et lui en envoyer une restriction.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="ec6c2-119">Implémentation d’un fournisseur de services de la méthode [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) peut copier cette propriété lors de la copie des dossiers.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ec6c2-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ec6c2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec6c2-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ec6c2-121">Protocol specifications</span></span>

<span data-ttu-id="ec6c2-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec6c2-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec6c2-123">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec6c2-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ec6c2-124">Header files</span></span>

<span data-ttu-id="ec6c2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec6c2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec6c2-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ec6c2-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ec6c2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ec6c2-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec6c2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec6c2-129">See also</span></span>



[<span data-ttu-id="ec6c2-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ec6c2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec6c2-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ec6c2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec6c2-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ec6c2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec6c2-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ec6c2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

