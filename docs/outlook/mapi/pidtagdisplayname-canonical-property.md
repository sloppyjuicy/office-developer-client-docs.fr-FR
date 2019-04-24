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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360801"
---
# <a name="pidtagdisplayname-canonical-property"></a><span data-ttu-id="489da-103">Propriété canonique PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="489da-103">PidTagDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="489da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="489da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="489da-105">Contient le nom complet d'un objet MAPI donné.</span><span class="sxs-lookup"><span data-stu-id="489da-105">Contains the display name for a given MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="489da-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="489da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="489da-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="489da-107">PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="489da-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="489da-108">Identifier:</span></span>  <br/> |<span data-ttu-id="489da-109">0x3001</span><span class="sxs-lookup"><span data-stu-id="489da-109">0x3001</span></span>  <br/> |
|<span data-ttu-id="489da-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="489da-110">Data type:</span></span>  <br/> |<span data-ttu-id="489da-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="489da-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="489da-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="489da-112">Area:</span></span>  <br/> |<span data-ttu-id="489da-113">MAPI commun</span><span class="sxs-lookup"><span data-stu-id="489da-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="489da-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="489da-114">Remarks</span></span>

<span data-ttu-id="489da-115">Les dossiers ont besoin de sous-dossiers frères pour avoir des noms complets uniques.</span><span class="sxs-lookup"><span data-stu-id="489da-115">Folders require sibling subfolders to have unique display names.</span></span> <span data-ttu-id="489da-116">Par exemple, si un dossier contient deux sous-dossiers, les deux sous-dossiers ne peuvent pas utiliser la même valeur pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="489da-116">For example, if a folder contains two subfolders, the two subfolders cannot use the same value for this property.</span></span> <span data-ttu-id="489da-117">Cette restriction ne s'applique pas aux autres conteneurs, tels que les carnets d'adresses et les listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="489da-117">This restriction does not apply to other containers, such as address books and distribution lists.</span></span> 
  
<span data-ttu-id="489da-118">Les fournisseurs de services doivent définir la valeur de cette propriété afin qu'elle contienne à la fois le type de fournisseur et les informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="489da-118">Service providers should set the value of this property so that it contains both the provider type and configuration information.</span></span> <span data-ttu-id="489da-119">Les informations supplémentaires permettent de faire la distinction entre les instances de fournisseurs du même type.</span><span class="sxs-lookup"><span data-stu-id="489da-119">The additional information helps to distinguish between instances of providers of the same type.</span></span> <span data-ttu-id="489da-120">Les fournisseurs non configurés doivent utiliser une chaîne qui nomme le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="489da-120">Unconfigured providers should use a string that names the provider.</span></span> <span data-ttu-id="489da-121">Les fournisseurs configurés doivent utiliser la même chaîne suivie d'une chaîne distinctive entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="489da-121">Configured providers should use the same string followed by a distinguishing string in parentheses.</span></span> <span data-ttu-id="489da-122">Par exemple, un fournisseur de banque de messages non configuré peut définir ces propriétés sur:</span><span class="sxs-lookup"><span data-stu-id="489da-122">For example, an unconfigured message store provider might set these properties to:</span></span> 
  
<span data-ttu-id="489da-123">Banque d'informations personnelles</span><span class="sxs-lookup"><span data-stu-id="489da-123">Personal Information Store</span></span>
  
<span data-ttu-id="489da-124">La version configurée peut ensuite définir ces propriétés sur:</span><span class="sxs-lookup"><span data-stu-id="489da-124">The configured version could then set these properties to:</span></span> 
  
<span data-ttu-id="489da-125">Banque d'informations personnelles (6 février 1998)</span><span class="sxs-lookup"><span data-stu-id="489da-125">Personal Information Store (February 6, 1998)</span></span>
  
<span data-ttu-id="489da-126">Pour les objets d'État, ces propriétés contiennent le nom du composant qui peut être affiché par l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="489da-126">For status objects, these properties contain the name of the component that can be displayed by the user interface.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="489da-127">Les points-virgules ne peuvent pas être utilisés dans les noms de destinataires de la messagerie MAPI.</span><span class="sxs-lookup"><span data-stu-id="489da-127">Semicolons cannot be used within recipient names in MAPI messaging.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="489da-128">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="489da-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="489da-129">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="489da-129">Protocol specifications</span></span>

<span data-ttu-id="489da-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="489da-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="489da-131">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="489da-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="489da-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="489da-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="489da-133">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="489da-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="489da-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="489da-134">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="489da-135">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="489da-135">Handles folder operations.</span></span>
    
<span data-ttu-id="489da-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="489da-136">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="489da-137">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="489da-137">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="489da-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="489da-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="489da-139">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="489da-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="489da-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="489da-140">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="489da-141">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="489da-141">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="489da-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="489da-142">[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="489da-143">Étend le protocole WebDAV qui spécifie comment demander et définir le descripteur de sécurité Exchange via les méthodes WebDAV.</span><span class="sxs-lookup"><span data-stu-id="489da-143">Extends the WebDAV protocol that specifies how to request and set the Exchange security descriptor via WebDAV methods.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="489da-144">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="489da-144">Header files</span></span>

<span data-ttu-id="489da-145">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="489da-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="489da-146">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="489da-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="489da-147">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="489da-147">Mapitags.h</span></span>
  
> <span data-ttu-id="489da-148">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="489da-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="489da-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="489da-149">See also</span></span>



[<span data-ttu-id="489da-150">Propriété canonique PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="489da-150">PidTagTransmittableDisplayName Canonical Property</span></span>](pidtagtransmittabledisplayname-canonical-property.md)


[<span data-ttu-id="489da-151">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="489da-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="489da-152">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="489da-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="489da-153">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="489da-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="489da-154">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="489da-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

