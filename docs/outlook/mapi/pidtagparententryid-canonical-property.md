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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 65f5e6c5da88267ec2e63d0acf3ef6f8e10c893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348229"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="af315-103">Propriété canonique PidTagParentEntryId</span><span class="sxs-lookup"><span data-stu-id="af315-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="af315-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af315-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af315-105">Contient l'identificateur d'entrée du dossier qui contient un dossier ou un message.</span><span class="sxs-lookup"><span data-stu-id="af315-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af315-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="af315-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af315-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="af315-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="af315-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="af315-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af315-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="af315-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="af315-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="af315-110">Data type:</span></span>  <br/> |<span data-ttu-id="af315-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="af315-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="af315-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="af315-112">Area:</span></span>  <br/> |<span data-ttu-id="af315-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="af315-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af315-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="af315-114">Remarks</span></span>

<span data-ttu-id="af315-115">Cette propriété est calculée par les banques de messages pour tous les dossiers et messages.</span><span class="sxs-lookup"><span data-stu-id="af315-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="af315-116">Pour un dossier racine de banque de messages, cette propriété contient l'identificateur d'entrée propre au dossier.</span><span class="sxs-lookup"><span data-stu-id="af315-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="af315-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) et cette propriété ne sont pas liées les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="af315-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="af315-118">Elles appartiennent à des contextes entièrement différents.</span><span class="sxs-lookup"><span data-stu-id="af315-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af315-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="af315-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af315-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="af315-120">Protocol specifications</span></span>

<span data-ttu-id="af315-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af315-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af315-122">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="af315-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af315-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af315-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af315-124">Définit les structures de données de base qui sont utilisées dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="af315-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="af315-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af315-125">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af315-126">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="af315-126">Handles folder operations.</span></span>
    
<span data-ttu-id="af315-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af315-127">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af315-128">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="af315-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="af315-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af315-129">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af315-130">Active la gestion des listes d'autorisation/de blocage et la détermination des messages électroniques indésirables.</span><span class="sxs-lookup"><span data-stu-id="af315-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="af315-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af315-131">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af315-132">Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="af315-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="af315-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af315-133">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af315-134">Spécifie la méthode de remise des données du carnet d'adresses en mode hors connexion (OAB) entre le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="af315-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af315-135">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="af315-135">Header files</span></span>

<span data-ttu-id="af315-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="af315-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="af315-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="af315-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="af315-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="af315-138">Mapitags.h</span></span>
  
> <span data-ttu-id="af315-139">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="af315-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af315-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af315-140">See also</span></span>



[<span data-ttu-id="af315-141">Propriété canonique PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="af315-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="af315-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="af315-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af315-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="af315-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af315-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="af315-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af315-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="af315-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

