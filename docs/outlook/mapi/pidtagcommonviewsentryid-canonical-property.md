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
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="472be-103">Propriété canonique PidTagCommonViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="472be-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="472be-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="472be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="472be-105">Contient l'identificateur d'entrée du dossier d'affichage commun prédéfini.</span><span class="sxs-lookup"><span data-stu-id="472be-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="472be-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="472be-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="472be-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="472be-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="472be-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="472be-108">Identifier:</span></span>  <br/> |<span data-ttu-id="472be-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="472be-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="472be-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="472be-110">Data type:</span></span>  <br/> |<span data-ttu-id="472be-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="472be-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="472be-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="472be-112">Area:</span></span>  <br/> |<span data-ttu-id="472be-113">Application Outlook</span><span class="sxs-lookup"><span data-stu-id="472be-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="472be-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="472be-114">Remarks</span></span>

<span data-ttu-id="472be-115">Le dossier d'affichage commun contient un ensemble prédéfini de spécificateurs d'affichage standard, tandis que le dossier d'affichage contient des spécificateurs définis par un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="472be-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="472be-116">Ces dossiers, qui ne sont pas visibles dans la hiérarchie des messages interpersonnels (IPM), peuvent contenir de nombreux spécificateurs d'affichage, chacun étant stocké sous forme de message.</span><span class="sxs-lookup"><span data-stu-id="472be-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="472be-117">Une application cliente peut choisir de fusionner les deux jeux de spécificateurs et les rendre disponibles.</span><span class="sxs-lookup"><span data-stu-id="472be-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="472be-118">Pour plus d'informations sur les affichages, consultez la rubrique [afficher les dossiers](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="472be-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="472be-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="472be-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="472be-120">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="472be-120">Header files</span></span>

<span data-ttu-id="472be-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="472be-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="472be-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="472be-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="472be-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="472be-123">Mapitags.h</span></span>
  
> <span data-ttu-id="472be-124">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="472be-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="472be-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="472be-125">See also</span></span>



[<span data-ttu-id="472be-126">Propriété canonique PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="472be-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="472be-127">Propriété canonique PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="472be-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="472be-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="472be-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="472be-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="472be-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="472be-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="472be-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="472be-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="472be-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

