---
title: Propriété canonique PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 33c62b81982aaac3659ad4d41ea2cf5298b42287
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785913"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="d1e6e-103">Propriété canonique PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="d1e6e-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="d1e6e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1e6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1e6e-105">Contient l’identificateur d’entrée de modèle pour l’objet utilisateur de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1e6e-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1e6e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d1e6e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1e6e-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="d1e6e-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="d1e6e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d1e6e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1e6e-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="d1e6e-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="d1e6e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d1e6e-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1e6e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d1e6e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d1e6e-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="d1e6e-112">Area:</span></span>  <br/> |<span data-ttu-id="d1e6e-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="d1e6e-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1e6e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1e6e-114">Remarks</span></span>

<span data-ttu-id="d1e6e-115">Applications clientes utilisent cette propriété pour créer un objet utilisateur de messagerie dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="d1e6e-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="d1e6e-116">Prise en charge de la création de l’entrée est facultatif pour les conteneurs de carnet d’adresses ; ceux qui ne prennent pas en charge qu’il ne sont pas nécessaire d’exposer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d1e6e-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="d1e6e-117">Cette propriété spécifie une entrée qui peut s’afficher dans la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) pour les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d1e6e-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="d1e6e-118">Après avoir obtenu l’identificateur, le client utilise un appel à la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e6e-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="d1e6e-119">L’entrée représente le modèle de l’utilisateur de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1e6e-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d1e6e-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d1e6e-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d1e6e-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d1e6e-121">Header files</span></span>

<span data-ttu-id="d1e6e-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1e6e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1e6e-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d1e6e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1e6e-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d1e6e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="d1e6e-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="d1e6e-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1e6e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1e6e-126">See also</span></span>



[<span data-ttu-id="d1e6e-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e6e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1e6e-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e6e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1e6e-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e6e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1e6e-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="d1e6e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

