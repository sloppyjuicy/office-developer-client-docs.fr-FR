---
title: Propriété canonique PidTag7BitDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4ae7645e45efb461ac53b6718569d909cec76504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785650"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="71e97-103">Propriété canonique PidTag7BitDisplayName</span><span class="sxs-lookup"><span data-stu-id="71e97-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="71e97-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="71e97-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71e97-105">Contient une représentation de ASCII 7 bits du nom d’un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="71e97-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71e97-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="71e97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71e97-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="71e97-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="71e97-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="71e97-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71e97-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="71e97-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="71e97-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="71e97-110">Data type:</span></span>  <br/> |<span data-ttu-id="71e97-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="71e97-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="71e97-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="71e97-112">Area:</span></span>  <br/> |<span data-ttu-id="71e97-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="71e97-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71e97-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="71e97-114">Remarks</span></span>

<span data-ttu-id="71e97-115">Ces propriétés sont mappées à la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à un jeu de caractères 7 bits.</span><span class="sxs-lookup"><span data-stu-id="71e97-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="71e97-116">Certains systèmes de messagerie, tels que Internet et certains liens X.400, sont limitées à l’ensemble de code ASCII 128 caractères 7 bits.</span><span class="sxs-lookup"><span data-stu-id="71e97-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="71e97-117">Passerelles à ces systèmes de messagerie peuvent améliorer les performances en appelant la méthode [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directement pour récupérer la propriété, évitant ainsi un traitement supplémentaire pour la conversion du code.</span><span class="sxs-lookup"><span data-stu-id="71e97-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="71e97-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="71e97-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71e97-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="71e97-119">Protocol specifications</span></span>

<span data-ttu-id="71e97-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71e97-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71e97-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="71e97-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71e97-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71e97-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71e97-123">Spécifie les propriétés et les opérations sur les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="71e97-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="71e97-124">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71e97-124">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71e97-125">Gère les communications d’un client avec un serveur NSPI.</span><span class="sxs-lookup"><span data-stu-id="71e97-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="71e97-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71e97-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71e97-127">Gère la commande et flux de données qui sert à transfère les données entre client et serveur.</span><span class="sxs-lookup"><span data-stu-id="71e97-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="71e97-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71e97-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71e97-129">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="71e97-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="71e97-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71e97-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71e97-131">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="71e97-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71e97-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="71e97-132">Header files</span></span>

<span data-ttu-id="71e97-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="71e97-133">Mapitags.h</span></span>
  
> <span data-ttu-id="71e97-134">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="71e97-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="71e97-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71e97-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="71e97-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="71e97-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71e97-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71e97-137">See also</span></span>



[<span data-ttu-id="71e97-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="71e97-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71e97-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="71e97-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71e97-140">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="71e97-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71e97-141">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="71e97-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

