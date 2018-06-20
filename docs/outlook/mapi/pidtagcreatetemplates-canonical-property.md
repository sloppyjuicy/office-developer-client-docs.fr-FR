---
title: Propriété canonique PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 82da274670c9266a746defcf6bbd5dbcf621901b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785892"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="6967e-103">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="6967e-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="6967e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6967e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6967e-105">Contient un objet incorporé table qui contient les identificateurs d’entrée de boîte de dialogue zone modèle.</span><span class="sxs-lookup"><span data-stu-id="6967e-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6967e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6967e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6967e-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="6967e-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="6967e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6967e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6967e-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="6967e-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="6967e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6967e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6967e-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="6967e-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="6967e-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="6967e-112">Area:</span></span>  <br/> |<span data-ttu-id="6967e-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="6967e-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6967e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6967e-114">Remarks</span></span>

<span data-ttu-id="6967e-115">Pour savoir quel modèle d’objets peuvent être créés à l’intérieur d’un conteneur, appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6967e-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="6967e-116">L’objet résultant est la table unique qui fournit les identificateurs d’entrée pour tous les modèles que vous pouvez créer dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="6967e-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="6967e-117">Pour créer les objets du modèle, appeler la méthode **CreateEntry** de l’objet conteneur sur les valeurs de colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la table unique.</span><span class="sxs-lookup"><span data-stu-id="6967e-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6967e-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6967e-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6967e-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6967e-119">Header files</span></span>

<span data-ttu-id="6967e-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6967e-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="6967e-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6967e-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="6967e-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6967e-122">Mapitags.h</span></span>
  
> <span data-ttu-id="6967e-123">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="6967e-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6967e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6967e-124">See also</span></span>



[<span data-ttu-id="6967e-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="6967e-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="6967e-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6967e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6967e-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6967e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6967e-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6967e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6967e-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="6967e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

