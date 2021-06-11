---
title: Propriété canonique PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437342"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="56b13-103">Propriété canonique PidTagCommonViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="56b13-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="56b13-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56b13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56b13-105">Contient l’identificateur d’entrée du dossier d’affichage commun prédéféré.</span><span class="sxs-lookup"><span data-stu-id="56b13-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56b13-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="56b13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56b13-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="56b13-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="56b13-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="56b13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="56b13-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="56b13-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="56b13-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="56b13-110">Data type:</span></span>  <br/> |<span data-ttu-id="56b13-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="56b13-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="56b13-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="56b13-112">Area:</span></span>  <br/> |<span data-ttu-id="56b13-113">Outlook application</span><span class="sxs-lookup"><span data-stu-id="56b13-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56b13-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="56b13-114">Remarks</span></span>

<span data-ttu-id="56b13-115">Le dossier d’affichage commun contient un ensemble prédéféré de specifieurs d’affichage standard, tandis que le dossier d’affichage contient des specifieurs définis par un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="56b13-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="56b13-116">Ces dossiers, qui ne sont pas visibles dans la hiérarchie des messages interpersonnels (IPM), peuvent contenir de nombreux spécifiés d’affichage, chacun étant stocké sous la mesure d’un message.</span><span class="sxs-lookup"><span data-stu-id="56b13-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="56b13-117">Une application cliente peut choisir de fusionner les deux ensembles de spécifiés et de les rendre disponibles.</span><span class="sxs-lookup"><span data-stu-id="56b13-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="56b13-118">Pour plus d’informations sur les [affichages, voir Afficher les dossiers.](mapi-view-folders.md)</span><span class="sxs-lookup"><span data-stu-id="56b13-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="56b13-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="56b13-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="56b13-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="56b13-120">Header files</span></span>

<span data-ttu-id="56b13-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56b13-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="56b13-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="56b13-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="56b13-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="56b13-123">Mapitags.h</span></span>
  
> <span data-ttu-id="56b13-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="56b13-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56b13-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56b13-125">See also</span></span>



[<span data-ttu-id="56b13-126">Propriété canonique PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="56b13-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="56b13-127">Propriété canonique PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="56b13-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="56b13-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="56b13-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56b13-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="56b13-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56b13-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="56b13-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56b13-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="56b13-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

