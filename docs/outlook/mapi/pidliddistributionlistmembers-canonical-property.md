---
title: Propriété canonique PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335069"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a><span data-ttu-id="3fb3d-103">Propriété canonique PidLidDistributionListMembers</span><span class="sxs-lookup"><span data-stu-id="3fb3d-103">PidLidDistributionListMembers Canonical Property</span></span>

  
  
<span data-ttu-id="3fb3d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fb3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fb3d-105">Spécifie la liste des identificateurs d'objet des objets qui correspondent aux membres de la liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-105">Specifies the list of EntryIds of the objects that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3fb3d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3fb3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3fb3d-107">dispidDLMembers</span><span class="sxs-lookup"><span data-stu-id="3fb3d-107">dispidDLMembers</span></span>  <br/> |
|<span data-ttu-id="3fb3d-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="3fb3d-108">Property set:</span></span>  <br/> |<span data-ttu-id="3fb3d-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3fb3d-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3fb3d-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="3fb3d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3fb3d-111">0x00008055</span><span class="sxs-lookup"><span data-stu-id="3fb3d-111">0x00008055</span></span>  <br/> |
|<span data-ttu-id="3fb3d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3fb3d-112">Data type:</span></span>  <br/> |<span data-ttu-id="3fb3d-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="3fb3d-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="3fb3d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3fb3d-114">Area:</span></span>  <br/> |<span data-ttu-id="3fb3d-115">Contact</span><span class="sxs-lookup"><span data-stu-id="3fb3d-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fb3d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3fb3d-116">Remarks</span></span>

<span data-ttu-id="3fb3d-117">Les membres de la liste de distribution personnelle peuvent être d'autres listes de distribution personnelles, des adresses électroniques contenues dans un contact, des listes de distribution ou des utilisateurs de liste d'adresses globale ou des adresses de messagerie uniques.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-117">Members of the personal distribution list can be other personal distribution lists, electronic addresses contained in a contact, Global Address List users or distribution lists, or one-off email addresses.</span></span> <span data-ttu-id="3fb3d-118">Le format de chaque EntryId doit être un EntryId unique, tel que spécifié dans [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) ou une EntryID incluse.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-118">The format of each EntryId must be either a one-off EntryId, as specified in [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) or a wrapped EntryId.</span></span> 
  
<span data-ttu-id="3fb3d-119">Lors de la définition de cette propriété, le client ou le serveur doit s'assurer que sa taille totale est inférieure à 15 000 octets.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-119">When setting this property, the client or the server must ensure its total size is less than 15,000 bytes.</span></span>
  
<span data-ttu-id="3fb3d-120">Cette propriété spécifie la liste des identificateurs d'identificateur uniques qui correspondent aux membres de la liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-120">This property specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span> <span data-ttu-id="3fb3d-121">Ces EntryID uniques encapsulent les noms complets et les adresses de messagerie des membres de la liste de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-121">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="3fb3d-122">Si le client ou le serveur définit cette propriété, il doit être synchronisé avec cette propriété **dispidDLMembers** pour chaque entrée dans la propriété **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), il doit y avoir une entrée dans le même position dans le **dispidDLOneOffMembers**.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-122">If the client or the server set this property, it must be synchronized with this property **dispidDLMembers** for each entry in the **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) property, there must be an entry in the same position in the **dispidDLOneOffMembers**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3fb3d-123">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="3fb3d-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3fb3d-124">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="3fb3d-124">Protocol specifications</span></span>

<span data-ttu-id="3fb3d-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fb3d-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fb3d-126">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3fb3d-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fb3d-127">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fb3d-128">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-128">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3fb3d-129">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="3fb3d-129">Header files</span></span>

<span data-ttu-id="3fb3d-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3fb3d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="3fb3d-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3fb3d-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3fb3d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fb3d-132">See also</span></span>



[<span data-ttu-id="3fb3d-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3fb3d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3fb3d-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3fb3d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3fb3d-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3fb3d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3fb3d-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3fb3d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

