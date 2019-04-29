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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438182"
---
# <a name="pidtagcreatetemplates-canonical-property"></a><span data-ttu-id="5a8a6-103">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="5a8a6-103">PidTagCreateTemplates Canonical Property</span></span>

  
  
<span data-ttu-id="5a8a6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a8a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a8a6-105">Contient un objet table incorporé qui contient des identificateurs d'entrée de modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5a8a6-105">Contains an embedded table object that contains dialog box template entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a8a6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5a8a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a8a6-107">PR_CREATE_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="5a8a6-107">PR_CREATE_TEMPLATES</span></span>  <br/> |
|<span data-ttu-id="5a8a6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5a8a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a8a6-109">0x3604</span><span class="sxs-lookup"><span data-stu-id="5a8a6-109">0x3604</span></span>  <br/> |
|<span data-ttu-id="5a8a6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5a8a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a8a6-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="5a8a6-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="5a8a6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5a8a6-112">Area:</span></span>  <br/> |<span data-ttu-id="5a8a6-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="5a8a6-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a8a6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5a8a6-114">Remarks</span></span>

<span data-ttu-id="5a8a6-115">Pour connaître les objets template pouvant être créés dans un conteneur, appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) sur cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5a8a6-115">To learn what template objects can be created inside a container, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on this property.</span></span> <span data-ttu-id="5a8a6-116">L'objet résultant est la table ponctuelle qui fournit les identificateurs d'entrée pour tous les modèles que vous pouvez créer à l'intérieur du conteneur.</span><span class="sxs-lookup"><span data-stu-id="5a8a6-116">The resulting object is the one-off table that gives the entry identifiers for all the templates that you can create inside the container.</span></span> 
  
<span data-ttu-id="5a8a6-117">Pour créer les objets template, appelez la méthode **CreateEntry** de l'objet Container sur les valeurs de la colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la table ponctuelle.</span><span class="sxs-lookup"><span data-stu-id="5a8a6-117">To create the template objects, call the container object's **CreateEntry** method on the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column values from the one-off table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a8a6-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5a8a6-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5a8a6-119">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="5a8a6-119">Header files</span></span>

<span data-ttu-id="5a8a6-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5a8a6-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a8a6-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5a8a6-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a8a6-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5a8a6-122">Mapitags.h</span></span>
  
> <span data-ttu-id="5a8a6-123">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5a8a6-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a8a6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a8a6-124">See also</span></span>



[<span data-ttu-id="5a8a6-125">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="5a8a6-125">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)


[<span data-ttu-id="5a8a6-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5a8a6-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a8a6-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5a8a6-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a8a6-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5a8a6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a8a6-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5a8a6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

