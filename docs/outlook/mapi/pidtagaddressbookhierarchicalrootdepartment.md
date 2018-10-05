---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382609"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a><span data-ttu-id="268b1-103">PidTagAddressBookHierarchicalRootDepartment</span><span class="sxs-lookup"><span data-stu-id="268b1-103">PidTagAddressBookHierarchicalRootDepartment</span></span>

  
  
<span data-ttu-id="268b1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="268b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="268b1-105">Contient le nom unique (DN) de la racine d’adresses hiérarchique (HAB).</span><span class="sxs-lookup"><span data-stu-id="268b1-105">Contains the distinguished name (DN) of the hierarchical address root (HAB).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="268b1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="268b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="268b1-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span><span class="sxs-lookup"><span data-stu-id="268b1-107">PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A</span></span>  <br/> |
|<span data-ttu-id="268b1-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="268b1-108">Property set:</span></span>  <br/> |<span data-ttu-id="268b1-109">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="268b1-109">Address Book</span></span>  <br/> |
|<span data-ttu-id="268b1-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="268b1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="268b1-111">0x8C98</span><span class="sxs-lookup"><span data-stu-id="268b1-111">0x8C98</span></span>  <br/> |
|<span data-ttu-id="268b1-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="268b1-112">Data type:</span></span>  <br/> |<span data-ttu-id="268b1-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="268b1-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="268b1-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="268b1-114">Area:</span></span>  <br/> |<span data-ttu-id="268b1-115">Carnet d’adresses Exchange</span><span class="sxs-lookup"><span data-stu-id="268b1-115">Exchange Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="268b1-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="268b1-116">Remarks</span></span>

<span data-ttu-id="268b1-117">Ceci est une propriété dans le conteneur de liste d’adresses global et représente le nom unique de la racine d’adresses hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="268b1-117">This is a property on the global address list (GAL) container and represents the distinguished name of the hierarchical address root.</span></span> <span data-ttu-id="268b1-118">Cette propriété n’est pas présente dans le carnet d’adresses en mode hors connexion et jamais dans les Services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="268b1-118">This property is only present in the offline address book and never in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="268b1-119">Les appelants doivent passer MAPI_CACHE_ONLY à l’appel de GetProps afin d’éviter un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="268b1-119">Callers should pass MAPI_CACHE_ONLY to the GetProps call to avoid a remote procedure call.</span></span> <span data-ttu-id="268b1-120">Si ce n’est pas présent, les appelants doivent utiliser PR_EMS_AB_HAB_ROOT_DEPARTMENT, qui est de type PT_OBJECT, pour trouver le service racine.</span><span class="sxs-lookup"><span data-stu-id="268b1-120">If this is not present, callers should use PR_EMS_AB_HAB_ROOT_DEPARTMENT, which is of type PT_OBJECT, to find the root department.</span></span> 
  
<span data-ttu-id="268b1-121">Une fois le service racine est obtenu, il peut avoir un type d’objet MAPI_MAILUSER ou MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="268b1-121">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="268b1-122">Si le type d’objet est MAPI_DISTLIST, le nouveau schéma est en cours employé.</span><span class="sxs-lookup"><span data-stu-id="268b1-122">If the object type is MAPI_DISTLIST, the new schema is being employed.</span></span> <span data-ttu-id="268b1-123">Si le type d’objet est MAPI_MAILUSER, le schéma précédent est en cours employé.</span><span class="sxs-lookup"><span data-stu-id="268b1-123">If the object type is MAPI_MAILUSER, the previous schema is being employed.</span></span> 
  
- <span data-ttu-id="268b1-124">Microsoft Office Outlook 2007 Service Pack 2 prend en charge les deux schémas.</span><span class="sxs-lookup"><span data-stu-id="268b1-124">Microsoft Office Outlook 2007 Service Pack 2 supports both schemas.</span></span> 
    
- <span data-ttu-id="268b1-125">Microsoft Outlook 2010 et Microsoft Outlook 2013 prend en charge le nouveau schéma.</span><span class="sxs-lookup"><span data-stu-id="268b1-125">Microsoft Outlook 2010 and Microsoft Outlook 2013 support the new schema.</span></span>
    
<span data-ttu-id="268b1-126">Dans le nouveau schéma, tous les groupes sont également les listes de distribution et sont de type MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="268b1-126">In the new schema, all departmental groups are also distribution lists and are of type MAPI_DISTLIST.</span></span> <span data-ttu-id="268b1-127">Les membres des groupes et services au sein de groupes sont obtenus à l’aide de PR_EMS_AB_MEMBER, exactement comme membres de liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="268b1-127">Members of departmental groups, and departments within departmental groups are obtained by using PR_EMS_AB_MEMBER, exactly like distribution list members.</span></span>
  
<span data-ttu-id="268b1-128">Une fois le service racine est obtenu, il peut avoir un type d’objet MAPI_MAILUSER ou MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="268b1-128">Once the root department is obtained, it can have an object type MAPI_MAILUSER or MAPI_DISTLIST.</span></span> <span data-ttu-id="268b1-129">Si le type d’objet est MAPI_DISTLIST, le nouveau schéma est utilisé.</span><span class="sxs-lookup"><span data-stu-id="268b1-129">If the object type is MAPI_DISTLIST, the new schema is being used.</span></span> <span data-ttu-id="268b1-130">Si le type d’objet est MAPI_MAILUSER, l’ancien schéma est utilisé.</span><span class="sxs-lookup"><span data-stu-id="268b1-130">If the object type is MAPI_MAILUSER, the old schema is being used.</span></span> 
  
<span data-ttu-id="268b1-131">Dans le nouveau schéma, tous les groupes sont également des listes de distribution et sont de type MAPI_DISTLIST.</span><span class="sxs-lookup"><span data-stu-id="268b1-131">In the new schema, all departmental groups are also DLs and are of type MAPI_DISTLIST.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="268b1-132">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="268b1-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="268b1-133">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="268b1-133">Protocol specifications</span></span>

<span data-ttu-id="268b1-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="268b1-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="268b1-135">Fournit des définitions de jeu de propriétés et des références pour les spécifications des protocoles Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="268b1-135">Provides property set definitions and references to related Microsoft Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="268b1-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="268b1-136">Header files</span></span>

<span data-ttu-id="268b1-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="268b1-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="268b1-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="268b1-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="268b1-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="268b1-139">See also</span></span>



[<span data-ttu-id="268b1-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="268b1-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="268b1-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="268b1-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="268b1-142">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="268b1-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="268b1-143">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="268b1-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

