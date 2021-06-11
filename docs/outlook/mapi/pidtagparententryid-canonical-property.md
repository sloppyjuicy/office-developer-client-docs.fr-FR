---
title: Propriété canonique PidTagParentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 65f5e6c5da88267ec2e63d0acf3ef6f8e10c893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348229"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="1e035-103">Propriété canonique PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="1e035-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1e035-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e035-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e035-105">Contient l’identificateur d’entrée du dossier qui contient un dossier ou un message.</span><span class="sxs-lookup"><span data-stu-id="1e035-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e035-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1e035-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e035-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1e035-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1e035-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1e035-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e035-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="1e035-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="1e035-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1e035-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e035-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1e035-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1e035-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1e035-112">Area:</span></span>  <br/> |<span data-ttu-id="1e035-113">Propriétés de l’ID</span><span class="sxs-lookup"><span data-stu-id="1e035-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e035-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1e035-114">Remarks</span></span>

<span data-ttu-id="1e035-115">Cette propriété est calculée par les magasins de messages pour tous les dossiers et messages.</span><span class="sxs-lookup"><span data-stu-id="1e035-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="1e035-116">Pour un dossier racine de la boutique de messages, cette propriété contient le propre identificateur d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="1e035-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="1e035-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) et cette propriété ne sont pas liées les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="1e035-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="1e035-118">Ils appartiennent à des contextes totalement différents.</span><span class="sxs-lookup"><span data-stu-id="1e035-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1e035-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1e035-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e035-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="1e035-120">Protocol specifications</span></span>

<span data-ttu-id="1e035-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e035-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e035-122">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="1e035-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1e035-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e035-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e035-124">Définit les structures de données de base utilisées dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="1e035-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="1e035-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e035-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e035-126">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="1e035-126">Handles folder operations.</span></span>
    
<span data-ttu-id="1e035-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e035-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e035-128">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="1e035-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1e035-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e035-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e035-130">Permet la gestion des listes d’adresses de courriers électroniques indésirables et la détermination des listes d’adresses de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="1e035-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="1e035-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e035-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e035-132">Spécifie les propriétés et opérations permettant de créer et de localiser les dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="1e035-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="1e035-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e035-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e035-134">Spécifie la méthode de livraison des données de carnet d’adresses en mode hors connexion du serveur au client.</span><span class="sxs-lookup"><span data-stu-id="1e035-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e035-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1e035-135">Header files</span></span>

<span data-ttu-id="1e035-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e035-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e035-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1e035-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e035-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e035-138">Mapitags.h</span></span>
  
> <span data-ttu-id="1e035-139">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="1e035-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e035-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e035-140">See also</span></span>



[<span data-ttu-id="1e035-141">Propriété canonique PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="1e035-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="1e035-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1e035-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e035-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1e035-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e035-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1e035-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e035-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1e035-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

