---
title: Propriété canonique PidTagOriginalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: eab72c5b49ba501d8ab5516bf5a5eae9ea82abe0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588705"
---
# <a name="pidtagoriginalentryid-canonical-property"></a><span data-ttu-id="5fe13-103">Propriété canonique PidTagOriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="5fe13-103">PidTagOriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="5fe13-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fe13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fe13-105">Contient l’identificateur d’entrée d’origine pour une entrée copiée à partir d’un carnet d’adresses à un carnet d’adresses personnel ou autre carnet d’adresses accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="5fe13-105">Contains the original entry identifier for an entry copied from an address book to a personal address book or other writeable address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5fe13-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5fe13-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5fe13-107">PR_ORIGINAL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5fe13-107">PR_ORIGINAL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="5fe13-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5fe13-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5fe13-109">0x3A12</span><span class="sxs-lookup"><span data-stu-id="5fe13-109">0x3A12</span></span>  <br/> |
|<span data-ttu-id="5fe13-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5fe13-110">Data type:</span></span>  <br/> |<span data-ttu-id="5fe13-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5fe13-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5fe13-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5fe13-112">Area:</span></span>  <br/> |<span data-ttu-id="5fe13-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="5fe13-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fe13-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5fe13-114">Remarks</span></span>

<span data-ttu-id="5fe13-115">Cette propriété est une des propriétés qui contiennent des informations sur la source d’origine d’une entrée copiée.</span><span class="sxs-lookup"><span data-stu-id="5fe13-115">This property is one of the properties that contain information about the original source of a copied entry.</span></span>
  
<span data-ttu-id="5fe13-116">Pour un rapport nonread, cette propriété contient une copie de l’identificateur d’entrée du destinataire du message d’origine pour lequel le rapport est généré.</span><span class="sxs-lookup"><span data-stu-id="5fe13-116">For a nonread report, this property contains a copy of the entry identifier of the original message recipient for which the report is generated.</span></span> <span data-ttu-id="5fe13-117">Lorsque le destinataire d’origine fait partie d’une liste de distribution, l’identificateur d’entrée de la liste de distribution est conservé pour le rapport.</span><span class="sxs-lookup"><span data-stu-id="5fe13-117">When the original recipient is part of a distribution list, the entry identifier of the distribution list is preserved for the report.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5fe13-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5fe13-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5fe13-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5fe13-119">Protocol specifications</span></span>

<span data-ttu-id="5fe13-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fe13-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fe13-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="5fe13-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5fe13-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fe13-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fe13-123">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="5fe13-123">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="5fe13-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5fe13-124">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5fe13-125">Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="5fe13-125">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5fe13-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5fe13-126">Header files</span></span>

<span data-ttu-id="5fe13-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5fe13-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5fe13-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5fe13-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="5fe13-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5fe13-129">Mapitags.h</span></span>
  
> <span data-ttu-id="5fe13-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="5fe13-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fe13-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fe13-131">See also</span></span>



[<span data-ttu-id="5fe13-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5fe13-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5fe13-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5fe13-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5fe13-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5fe13-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5fe13-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5fe13-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

