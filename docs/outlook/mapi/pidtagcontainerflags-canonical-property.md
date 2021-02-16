---
title: Propriété canonique PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357546"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="cd7e4-103">Propriété canonique PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="cd7e4-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="cd7e4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd7e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd7e4-105">Contient un masque de bits d’indicateurs décrivant les fonctionnalités d’un conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd7e4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cd7e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd7e4-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="cd7e4-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="cd7e4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cd7e4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd7e4-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="cd7e4-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="cd7e4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cd7e4-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd7e4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cd7e4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cd7e4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cd7e4-112">Area:</span></span>  <br/> |<span data-ttu-id="cd7e4-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="cd7e4-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd7e4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd7e4-114">Remarks</span></span>

<span data-ttu-id="cd7e4-115">Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits :</span><span class="sxs-lookup"><span data-stu-id="cd7e4-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="cd7e4-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="cd7e4-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="cd7e4-117">Affiche une boîte de dialogue pour demander une restriction avant d’afficher le contenu du conteneur.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="cd7e4-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="cd7e4-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="cd7e4-119">Les entrées peuvent être ajoutées au conteneur et supprimées.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="cd7e4-120">Cet indicateur n’indique pas si des entrées du conteneur peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="cd7e4-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="cd7e4-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="cd7e4-122">Le conteneur peut contenir des destinataires.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-122">The container can hold recipients.</span></span> <span data-ttu-id="cd7e4-123">Cet indicateur n’indique pas si des destinataires sont réellement présents dans le conteneur, ou s’ils peuvent être ajoutés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="cd7e4-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="cd7e4-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="cd7e4-125">Le conteneur peut contenir des conteneurs enfants.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-125">The container can hold child containers.</span></span> <span data-ttu-id="cd7e4-126">Cet indicateur n’indique pas si des sous-locataires sont réellement présents dans le conteneur, ni s’ils peuvent être ajoutés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="cd7e4-127">AB_SUBCONTAINERS être définie pour que le conteneur soit en charge [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span><span class="sxs-lookup"><span data-stu-id="cd7e4-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="cd7e4-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="cd7e4-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="cd7e4-129">Les entrées ne peuvent pas être ajoutées ou supprimées du conteneur.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="cd7e4-130">Cet indicateur n’indique pas si des entrées du conteneur peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="cd7e4-131">L AB_FIND_ON_OPEN est vivement recommandé pour les conteneurs utilisés avec des services en ligne ou avec des connexions lentes aux serveurs.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="cd7e4-132">Lorsqu’un conteneur est ouvert et AB_FIND_ON_OPEN,  une boîte de dialogue Rechercher est présentée à l’utilisateur pour restreindre les utilisateurs de messagerie affichés.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="cd7e4-133">Même une spécification partielle limitant les utilisateurs de messagerie peut accélérer considérablement l’affichage du contenu.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="cd7e4-134">L’AB_MODIFIABLE ou AB_UNMODIFIABLE’indicateur doit être définie.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="cd7e4-135">Les deux indicateurs peuvent être définies pour indiquer que le conteneur ne sait pas s’il peut être modifié ou non, par exemple si la modification dépend des droits d’accès de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="cd7e4-136">Dans ce cas, une application cliente doit tenter un appel et examiner le code de retour pour déterminer les fonctionnalités du conteneur.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="cd7e4-137">Un client commence généralement par examiner AB_MODIFIABLE.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="cd7e4-138">Si elle est définie, le client effectue un appel qui tente de modifier le conteneur et vérifie la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="cd7e4-139">L AB_MODIFIABLE n’indique pas les types d’entrées qui peuvent être ajoutés au conteneur.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="cd7e4-140">Pour le déterminer, le client doit utiliser la méthode [OpenProperty](imapiprop-openproperty.md) appropriée pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cd7e4-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="cd7e4-141">**L’PR_CREATE_TEMPLATES** entraîne le retour de la table du conteneur, répertoriant les types d’entrées qui peuvent être créées dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cd7e4-142">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cd7e4-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd7e4-143">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="cd7e4-143">Protocol specifications</span></span>

<span data-ttu-id="cd7e4-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd7e4-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd7e4-145">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd7e4-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd7e4-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd7e4-147">Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="cd7e4-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd7e4-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd7e4-149">Gère les communications d’un client avec un serveur NSPI (Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="cd7e4-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd7e4-150">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cd7e4-150">Header files</span></span>

<span data-ttu-id="cd7e4-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd7e4-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd7e4-152">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd7e4-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd7e4-153">Mapitags.h</span></span>
  
> <span data-ttu-id="cd7e4-154">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="cd7e4-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd7e4-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd7e4-155">See also</span></span>



[<span data-ttu-id="cd7e4-156">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cd7e4-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd7e4-157">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cd7e4-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd7e4-158">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cd7e4-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd7e4-159">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cd7e4-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

