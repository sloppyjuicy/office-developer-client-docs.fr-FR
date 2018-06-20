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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7d91ed369b3a6e8b4f62534d49b202b46c327baa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785800"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="393dd-103">Propriété canonique PidTagCommonViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="393dd-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="393dd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="393dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="393dd-105">Contient l’identificateur d’entrée du dossier commun affichage prédéfini.</span><span class="sxs-lookup"><span data-stu-id="393dd-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="393dd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="393dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="393dd-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="393dd-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="393dd-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="393dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="393dd-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="393dd-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="393dd-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="393dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="393dd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="393dd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="393dd-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="393dd-112">Area:</span></span>  <br/> |<span data-ttu-id="393dd-113">Application Outlook</span><span class="sxs-lookup"><span data-stu-id="393dd-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="393dd-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="393dd-114">Remarks</span></span>

<span data-ttu-id="393dd-115">Le dossier d’affichage communs contient un ensemble prédéfini des spécificateurs d’affichage standard, tandis que le dossier d’affichage contient des spécificateurs définis par un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="393dd-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="393dd-116">Ces dossiers, qui ne sont pas visibles dans la hiérarchie de message interpersonnel (IPM), peuvent contenir plusieurs spécificateurs d’affichage, chacune étant stockées sous forme de message.</span><span class="sxs-lookup"><span data-stu-id="393dd-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="393dd-117">Une application cliente pouvez choisir de fusionner les deux jeux de spécificateurs et les divulguer les deux.</span><span class="sxs-lookup"><span data-stu-id="393dd-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="393dd-118">Pour plus d’informations sur les affichages, voir [Afficher les dossiers](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="393dd-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="393dd-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="393dd-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="393dd-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="393dd-120">Header files</span></span>

<span data-ttu-id="393dd-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="393dd-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="393dd-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="393dd-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="393dd-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="393dd-123">Mapitags.h</span></span>
  
> <span data-ttu-id="393dd-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="393dd-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="393dd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="393dd-125">See also</span></span>



[<span data-ttu-id="393dd-126">Propriété canonique PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="393dd-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="393dd-127">Propriété canonique PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="393dd-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="393dd-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="393dd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="393dd-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="393dd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="393dd-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="393dd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="393dd-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="393dd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

