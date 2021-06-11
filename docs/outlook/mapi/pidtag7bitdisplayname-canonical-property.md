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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5177d47749c2f60a883bd12fbba27045114c601
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315812"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="9faa6-103">Propriété canonique PidTag7BitDisplayName</span><span class="sxs-lookup"><span data-stu-id="9faa6-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="9faa6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9faa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9faa6-105">Contient une représentation ASCII 7 bits du nom d’un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9faa6-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9faa6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9faa6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9faa6-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="9faa6-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="9faa6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9faa6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9faa6-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="9faa6-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="9faa6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9faa6-110">Data type:</span></span>  <br/> |<span data-ttu-id="9faa6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9faa6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9faa6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9faa6-112">Area:</span></span>  <br/> |<span data-ttu-id="9faa6-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="9faa6-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9faa6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9faa6-114">Remarks</span></span>

<span data-ttu-id="9faa6-115">Ces propriétés **m PR_DISPLAY_NAME** la propriété ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans un jeu de caractères 7 bits.</span><span class="sxs-lookup"><span data-stu-id="9faa6-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="9faa6-116">Certains systèmes de messagerie, tels qu’Internet et certains liens X.400, sont limités au jeu de codes ASCII 7 bits de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="9faa6-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="9faa6-117">Les passerelles vers ces systèmes de messagerie peuvent améliorer leurs performances en appelant directement la méthode [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) pour récupérer cette propriété, évitant ainsi un traitement supplémentaire pour la conversion de code.</span><span class="sxs-lookup"><span data-stu-id="9faa6-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9faa6-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9faa6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9faa6-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9faa6-119">Protocol specifications</span></span>

<span data-ttu-id="9faa6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9faa6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9faa6-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="9faa6-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9faa6-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9faa6-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9faa6-123">Spécifie les propriétés et les opérations sur les listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="9faa6-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="9faa6-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9faa6-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9faa6-125">Gère les communications d’un client avec un serveur NSPI.</span><span class="sxs-lookup"><span data-stu-id="9faa6-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="9faa6-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9faa6-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9faa6-127">Gère l’ordre et le flux de données utilisés pour transférer des données entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="9faa6-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="9faa6-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9faa6-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9faa6-129">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="9faa6-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9faa6-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9faa6-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9faa6-131">Spécifie les propriétés et opérations autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="9faa6-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9faa6-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9faa6-132">Header files</span></span>

<span data-ttu-id="9faa6-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9faa6-133">Mapitags.h</span></span>
  
> <span data-ttu-id="9faa6-134">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="9faa6-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="9faa6-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9faa6-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="9faa6-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9faa6-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9faa6-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9faa6-137">See also</span></span>



[<span data-ttu-id="9faa6-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9faa6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9faa6-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9faa6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9faa6-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9faa6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9faa6-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9faa6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

