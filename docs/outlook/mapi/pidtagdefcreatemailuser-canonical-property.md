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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407479"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="e00db-103">Propriété canonique PidTagDefCreateMailuser</span><span class="sxs-lookup"><span data-stu-id="e00db-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="e00db-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e00db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e00db-105">Contient l’identificateur d’entrée de modèle pour un objet utilisateur de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="e00db-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e00db-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e00db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e00db-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="e00db-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="e00db-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e00db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e00db-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="e00db-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="e00db-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e00db-110">Data type:</span></span>  <br/> |<span data-ttu-id="e00db-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e00db-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e00db-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e00db-112">Area:</span></span>  <br/> |<span data-ttu-id="e00db-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="e00db-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e00db-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e00db-114">Remarks</span></span>

<span data-ttu-id="e00db-115">Les applications clientes utilisent cette propriété pour créer un objet utilisateur de messagerie dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="e00db-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="e00db-116">La prise en charge de la création d’entrées est facultative pour les conteneurs de carnet d’adresses . ceux qui ne la prisent pas en charge ne sont pas obligés d’exposer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e00db-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="e00db-117">Cette propriété spécifie une entrée qui peut apparaître dans la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) pour les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e00db-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="e00db-118">Une fois l’identificateur obtenu, le client l’utilise dans un appel à la méthode [IABContainer::CreateEntry.](iabcontainer-createentry.md)</span><span class="sxs-lookup"><span data-stu-id="e00db-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="e00db-119">L’entrée représente le modèle de l’utilisateur de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="e00db-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e00db-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e00db-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e00db-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e00db-121">Header files</span></span>

<span data-ttu-id="e00db-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e00db-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="e00db-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e00db-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="e00db-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e00db-124">Mapitags.h</span></span>
  
> <span data-ttu-id="e00db-125">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="e00db-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e00db-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e00db-126">See also</span></span>



[<span data-ttu-id="e00db-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e00db-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e00db-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e00db-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e00db-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e00db-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e00db-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e00db-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

