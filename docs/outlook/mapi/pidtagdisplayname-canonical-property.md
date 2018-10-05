---
title: Propriété canonique PidTagDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386417"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="2bd30-103">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="2bd30-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="2bd30-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bd30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bd30-105">Contient le nom complet d’un objet MAPI donné.</span><span class="sxs-lookup"><span data-stu-id="2bd30-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2bd30-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2bd30-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2bd30-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="2bd30-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="2bd30-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2bd30-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2bd30-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="2bd30-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="2bd30-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2bd30-110">Data type:</span></span>  <br/> |<span data-ttu-id="2bd30-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2bd30-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2bd30-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2bd30-112">Area:</span></span>  <br/> |<span data-ttu-id="2bd30-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="2bd30-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bd30-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2bd30-114">Remarks</span></span>

<span data-ttu-id="2bd30-115">Dossiers nécessitent des sous-dossiers frère d’avoir des noms uniques.</span><span class="sxs-lookup"><span data-stu-id="2bd30-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="2bd30-116">Par exemple, si un dossier contient deux sous-dossiers, les deux sous-dossiers ne peuvent pas utiliser la même valeur pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2bd30-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="2bd30-117">Cette restriction ne s’applique pas aux autres conteneurs, tels que des carnets d’adresses et listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="2bd30-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="2bd30-118">Fournisseurs de services doivent définir la valeur de cette propriété afin qu’elle contienne à la fois les type et la configuration informations sur les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="2bd30-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="2bd30-119">Les informations supplémentaires permettent de faire la distinction entre des instances de fournisseurs du même type.</span><span class="sxs-lookup"><span data-stu-id="2bd30-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="2bd30-120">Fournisseurs non configurés doivent utiliser une chaîne qui nomme le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2bd30-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="2bd30-121">Fournisseurs configurés doivent utiliser la même chaîne de suivi d’une chaîne distinctive entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="2bd30-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="2bd30-122">Par exemple, un fournisseur de magasin de message non configuré peut définir ces propriétés :</span><span class="sxs-lookup"><span data-stu-id="2bd30-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="2bd30-123">Banque d’informations personnelles</span><span class="sxs-lookup"><span data-stu-id="2bd30-123">Personal Information Store</span></span>
  
<span data-ttu-id="2bd30-124">La version configurée peut ensuite définir ces propriétés :</span><span class="sxs-lookup"><span data-stu-id="2bd30-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="2bd30-125">Banque d’informations personnelles (6 février 1998)</span><span class="sxs-lookup"><span data-stu-id="2bd30-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="2bd30-126">Pour les objets d’état, ces propriétés contient le nom du composant qui peut être affiché par l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2bd30-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2bd30-127">Des points-virgules ne peut pas être utilisés dans les noms des destinataires de messagerie MAPI.</span><span class="sxs-lookup"><span data-stu-id="2bd30-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2bd30-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2bd30-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2bd30-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="2bd30-129">Protocol specifications</span></span>

<span data-ttu-id="2bd30-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd30-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd30-131">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="2bd30-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2bd30-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd30-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd30-133">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2bd30-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="2bd30-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd30-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd30-135">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="2bd30-135">Handles folder operations.</span></span>
    
<span data-ttu-id="2bd30-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd30-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd30-137">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="2bd30-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="2bd30-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd30-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd30-139">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="2bd30-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="2bd30-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd30-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd30-141">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="2bd30-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="2bd30-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2bd30-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2bd30-143">Étend le protocole WebDAV qui spécifie comment demander et définir le descripteur de sécurité Exchange via les méthodes WebDAV.</span><span class="sxs-lookup"><span data-stu-id="2bd30-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2bd30-144">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2bd30-144">Header files</span></span>

<span data-ttu-id="2bd30-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2bd30-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="2bd30-146">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2bd30-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="2bd30-147">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="2bd30-147">Mapitags.h</span></span>
  
> <span data-ttu-id="2bd30-148">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="2bd30-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2bd30-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bd30-149">See also</span></span>



[<span data-ttu-id="2bd30-150">Propriété canonique PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="2bd30-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="2bd30-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2bd30-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2bd30-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2bd30-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2bd30-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2bd30-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2bd30-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2bd30-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

