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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393515"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="b3992-103">Propriété canonique PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="b3992-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b3992-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3992-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3992-105">Contient l’identificateur d’entrée de l’affichage de par défaut d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="b3992-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3992-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b3992-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b3992-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b3992-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="b3992-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b3992-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b3992-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="b3992-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="b3992-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b3992-110">Data type:</span></span>  <br/> |<span data-ttu-id="b3992-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b3992-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b3992-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b3992-112">Area:</span></span>  <br/> |<span data-ttu-id="b3992-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="b3992-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3992-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3992-114">Remarks</span></span>

<span data-ttu-id="b3992-115">Cette propriété est l’identificateur d’entrée de l’affichage du dossier qui doit être défini en tant que la vue initiale.</span><span class="sxs-lookup"><span data-stu-id="b3992-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="b3992-116">La propriété ne doit pas être définie si l’affichage de « Normal » est utilisée en tant que la vue initiale.</span><span class="sxs-lookup"><span data-stu-id="b3992-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="b3992-117">Une application cliente peut obtenir cette propriété au moment où qu'il ouvre le dossier et réaliser des gains de performances.</span><span class="sxs-lookup"><span data-stu-id="b3992-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="b3992-118">Cette propriété peut être utilisée comme un raccourci pour obtenir la vue par défaut, au lieu d’ouvrir la table de contenu associé et lui en envoyer une restriction.</span><span class="sxs-lookup"><span data-stu-id="b3992-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="b3992-119">Implémentation d’un fournisseur de services de la méthode [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) peut copier cette propriété lors de la copie des dossiers.</span><span class="sxs-lookup"><span data-stu-id="b3992-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b3992-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b3992-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b3992-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b3992-121">Protocol specifications</span></span>

<span data-ttu-id="b3992-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3992-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3992-123">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="b3992-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b3992-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b3992-124">Header files</span></span>

<span data-ttu-id="b3992-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b3992-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b3992-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b3992-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="b3992-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b3992-127">Mapitags.h</span></span>
  
> <span data-ttu-id="b3992-128">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="b3992-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3992-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3992-129">See also</span></span>



[<span data-ttu-id="b3992-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b3992-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b3992-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b3992-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b3992-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b3992-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b3992-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b3992-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

