---
title: Propriété canonique PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419253"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="0a01a-103">Propriété canonique PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="0a01a-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="0a01a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a01a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a01a-105">Contient un objet de tableau d’affichage incorporé.</span><span class="sxs-lookup"><span data-stu-id="0a01a-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a01a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0a01a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a01a-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="0a01a-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="0a01a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0a01a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a01a-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="0a01a-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="0a01a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0a01a-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a01a-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="0a01a-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="0a01a-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0a01a-112">Area:</span></span>  <br/> |<span data-ttu-id="0a01a-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="0a01a-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a01a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0a01a-114">Remarks</span></span>

<span data-ttu-id="0a01a-115">La transmission de cette propriété à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour l’objet renvoie une interface [IMAPITable](imapitableiunknown.md) qui permet la création du tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0a01a-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="0a01a-116">MAPI utilise ce tableau pour afficher les feuilles de propriétés d’un objet de carnet d’adresses en réponse à un appel [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="0a01a-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0a01a-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0a01a-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0a01a-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0a01a-118">Header files</span></span>

<span data-ttu-id="0a01a-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a01a-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a01a-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0a01a-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a01a-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0a01a-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0a01a-122">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="0a01a-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a01a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a01a-123">See also</span></span>



[<span data-ttu-id="0a01a-124">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="0a01a-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="0a01a-125">Propriété canonique PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="0a01a-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="0a01a-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0a01a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a01a-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0a01a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a01a-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0a01a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a01a-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0a01a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

