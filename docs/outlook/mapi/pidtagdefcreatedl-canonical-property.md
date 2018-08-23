---
title: Propriété canonique PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 48c068599506e5c050c69594caca46f28be83b0b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565801"
---
# <a name="pidtagdefcreatedl-canonical-property"></a><span data-ttu-id="0aa14-103">Propriété canonique PidTagDefCreateDl</span><span class="sxs-lookup"><span data-stu-id="0aa14-103">PidTagDefCreateDl Canonical Property</span></span>

  
  
<span data-ttu-id="0aa14-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aa14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aa14-105">Contient l’identificateur d’entrée de modèle pour une liste de distribution par défaut.</span><span class="sxs-lookup"><span data-stu-id="0aa14-105">Contains the template entry identifier for a default distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0aa14-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0aa14-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0aa14-107">PR_DEF_CREATE_DL</span><span class="sxs-lookup"><span data-stu-id="0aa14-107">PR_DEF_CREATE_DL</span></span>  <br/> |
|<span data-ttu-id="0aa14-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0aa14-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0aa14-109">0x3611</span><span class="sxs-lookup"><span data-stu-id="0aa14-109">0x3611</span></span>  <br/> |
|<span data-ttu-id="0aa14-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0aa14-110">Data type:</span></span>  <br/> |<span data-ttu-id="0aa14-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0aa14-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0aa14-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0aa14-112">Area:</span></span>  <br/> |<span data-ttu-id="0aa14-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="0aa14-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0aa14-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0aa14-114">Remarks</span></span>

<span data-ttu-id="0aa14-115">Applications clientes utilisent cette propriété pour créer une liste de distribution dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="0aa14-115">Client applications use this property to create a distribution list within a container.</span></span> <span data-ttu-id="0aa14-116">Prise en charge de la création de l’entrée est facultatif pour les conteneurs de carnet d’adresses ; ceux qui ne prennent pas en charge qu’il ne sont pas nécessaire d’exposer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0aa14-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="0aa14-117">Cette propriété spécifie une entrée qui peut s’afficher dans la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) pour les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="0aa14-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for distribution lists.</span></span> <span data-ttu-id="0aa14-118">Après avoir obtenu l’identificateur, le client utilise un appel à la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="0aa14-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="0aa14-119">L’entrée représente le modèle pour la liste de distribution par défaut.</span><span class="sxs-lookup"><span data-stu-id="0aa14-119">The entry represents the template for the default distribution list.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0aa14-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0aa14-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0aa14-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0aa14-121">Header files</span></span>

<span data-ttu-id="0aa14-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0aa14-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0aa14-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0aa14-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0aa14-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0aa14-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0aa14-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="0aa14-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0aa14-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aa14-126">See also</span></span>



[<span data-ttu-id="0aa14-127">IABLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="0aa14-127">IABLogon::CompareEntryIDs</span></span>](iablogon-compareentryids.md)


[<span data-ttu-id="0aa14-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0aa14-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0aa14-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0aa14-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0aa14-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0aa14-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0aa14-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0aa14-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

