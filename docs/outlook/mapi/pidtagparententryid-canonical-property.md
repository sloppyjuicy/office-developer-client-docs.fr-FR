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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 48627c6d6eb2100e7dfcab832c86c1ec2e4ec8bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582804"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="4c569-103">Propriété canonique PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="4c569-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4c569-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c569-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c569-105">Contient l’identificateur d’entrée du dossier qui contient un dossier ou un message.</span><span class="sxs-lookup"><span data-stu-id="4c569-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c569-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4c569-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c569-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4c569-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4c569-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4c569-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c569-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="4c569-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="4c569-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4c569-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c569-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4c569-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4c569-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4c569-112">Area:</span></span>  <br/> |<span data-ttu-id="4c569-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="4c569-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c569-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4c569-114">Remarks</span></span>

<span data-ttu-id="4c569-115">Cette propriété est calculée par les banques de messages de tous les dossiers et les messages.</span><span class="sxs-lookup"><span data-stu-id="4c569-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="4c569-116">Pour un dossier racine de la banque de messages, cette propriété contient l’identificateur d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="4c569-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="4c569-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) et cette propriété sont sans rapport avec les autres.</span><span class="sxs-lookup"><span data-stu-id="4c569-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="4c569-118">Ils appartiennent aux contextes totalement différents.</span><span class="sxs-lookup"><span data-stu-id="4c569-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4c569-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4c569-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c569-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4c569-120">Protocol specifications</span></span>

<span data-ttu-id="4c569-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c569-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c569-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="4c569-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4c569-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c569-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c569-124">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="4c569-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="4c569-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c569-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c569-126">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="4c569-126">Handles folder operations.</span></span>
    
<span data-ttu-id="4c569-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c569-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c569-128">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="4c569-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="4c569-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c569-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c569-130">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="4c569-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="4c569-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c569-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c569-132">Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4c569-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="4c569-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c569-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c569-134">Spécifie la méthode de livraison de données de carnet d’adresses en mode hors connexion à partir du serveur au client.</span><span class="sxs-lookup"><span data-stu-id="4c569-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c569-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4c569-135">Header files</span></span>

<span data-ttu-id="4c569-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c569-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c569-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4c569-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c569-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4c569-138">Mapitags.h</span></span>
  
> <span data-ttu-id="4c569-139">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4c569-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c569-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c569-140">See also</span></span>



[<span data-ttu-id="4c569-141">Propriété canonique PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="4c569-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="4c569-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4c569-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c569-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4c569-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c569-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4c569-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c569-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4c569-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

