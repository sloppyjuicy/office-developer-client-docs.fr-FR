---
title: Propriété canonique PidTagGender
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386613"
---
# <a name="pidtaggender-canonical-property"></a><span data-ttu-id="3c3f8-103">Propriété canonique PidTagGender</span><span class="sxs-lookup"><span data-stu-id="3c3f8-103">PidTagGender Canonical Property</span></span>

  
  
<span data-ttu-id="3c3f8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c3f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c3f8-105">Indique le sexe de l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-105">Contains the gender of the messaging user.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c3f8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3c3f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c3f8-107">PR_GENDER</span><span class="sxs-lookup"><span data-stu-id="3c3f8-107">PR_GENDER</span></span>  <br/> |
|<span data-ttu-id="3c3f8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3c3f8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c3f8-109">0x3A4D</span><span class="sxs-lookup"><span data-stu-id="3c3f8-109">0x3A4D</span></span>  <br/> |
|<span data-ttu-id="3c3f8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3c3f8-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c3f8-111">PT_I2</span><span class="sxs-lookup"><span data-stu-id="3c3f8-111">PT_I2</span></span>  <br/> |
|<span data-ttu-id="3c3f8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3c3f8-112">Area:</span></span>  <br/> |<span data-ttu-id="3c3f8-113">Utilisateur de messagerie MAPI</span><span class="sxs-lookup"><span data-stu-id="3c3f8-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c3f8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3c3f8-114">Remarks</span></span>

<span data-ttu-id="3c3f8-115">Cette propriété fournit des informations d’identification et l’accès sur un utilisateur de messagerie et du contenu.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-115">This property provides identification and access information about a messaging user and the content is.</span></span> <span data-ttu-id="3c3f8-116">Le contenu est défini par l’utilisateur de messagerie et l’organisation de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-116">The content is defined by the messaging user and the messaging user's organization.</span></span> 
  
<span data-ttu-id="3c3f8-117">Les valeurs possibles pour cette propriété sont définies dans l’énumération sexe.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-117">The possible values for this property are defined in the gender enumeration.</span></span> <span data-ttu-id="3c3f8-118">Ils sont répertoriés comme suit :</span><span class="sxs-lookup"><span data-stu-id="3c3f8-118">They are listed as follows:</span></span>
  
|<span data-ttu-id="3c3f8-119">**Énumération sexe**</span><span class="sxs-lookup"><span data-stu-id="3c3f8-119">**Gender enumeration**</span></span>|<span data-ttu-id="3c3f8-120">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3c3f8-120">**Value**</span></span>|<span data-ttu-id="3c3f8-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="3c3f8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3c3f8-122">genderUnspecified</span><span class="sxs-lookup"><span data-stu-id="3c3f8-122">genderUnspecified</span></span>  <br/> |<span data-ttu-id="3c3f8-123">0x0000</span><span class="sxs-lookup"><span data-stu-id="3c3f8-123">0x0000</span></span>  <br/> |<span data-ttu-id="3c3f8-124">Le sexe du contact n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-124">The contact's gender is unspecified.</span></span>  <br/> |
|<span data-ttu-id="3c3f8-125">genderFemale</span><span class="sxs-lookup"><span data-stu-id="3c3f8-125">genderFemale</span></span>  <br/> |<span data-ttu-id="3c3f8-126">0x0001</span><span class="sxs-lookup"><span data-stu-id="3c3f8-126">0x0001</span></span>  <br/> |<span data-ttu-id="3c3f8-127">Le contact est féminin.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-127">The contact is female.</span></span>  <br/> |
|<span data-ttu-id="3c3f8-128">genderMale</span><span class="sxs-lookup"><span data-stu-id="3c3f8-128">genderMale</span></span>  <br/> |<span data-ttu-id="3c3f8-129">0x0002</span><span class="sxs-lookup"><span data-stu-id="3c3f8-129">0x0002</span></span>  <br/> |<span data-ttu-id="3c3f8-130">Le contact est masculin.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-130">The contact is male.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3c3f8-131">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3c3f8-131">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c3f8-132">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3c3f8-132">Protocol specifications</span></span>

<span data-ttu-id="3c3f8-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c3f8-133">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c3f8-134">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-134">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c3f8-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c3f8-135">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c3f8-136">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-136">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="3c3f8-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c3f8-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c3f8-138">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c3f8-139">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3c3f8-139">Header files</span></span>

<span data-ttu-id="3c3f8-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c3f8-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c3f8-141">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c3f8-142">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3c3f8-142">Mapitags.h</span></span>
  
> <span data-ttu-id="3c3f8-143">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3c3f8-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c3f8-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c3f8-144">See also</span></span>



[<span data-ttu-id="3c3f8-145">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3c3f8-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c3f8-146">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3c3f8-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c3f8-147">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3c3f8-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c3f8-148">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3c3f8-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

