---
title: Propriété canonique PidTagMemberId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391744"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="d1215-103">Propriété canonique PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="d1215-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="d1215-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1215-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1215-105">Contient l’identificateur d’un membre de la table qui possède les droits décrits dans une boîte aux lettres ou un dossier Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d1215-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1215-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d1215-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1215-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="d1215-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="d1215-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d1215-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1215-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="d1215-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="d1215-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d1215-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1215-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="d1215-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="d1215-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d1215-112">Area:</span></span>  <br/> |<span data-ttu-id="d1215-113">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="d1215-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1215-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1215-114">Remarks</span></span>

<span data-ttu-id="d1215-115">Cette propriété renvoie un identificateur unique pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="d1215-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="d1215-116">Un identificateur d’annuaire utilisateur est associé à l’identificateur de chaque membre et est fourni par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d1215-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="d1215-117">Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour récupérer l’identificateur d’entrée de répertoire d’un membre disposant de droits explicites sur un dossier.</span><span class="sxs-lookup"><span data-stu-id="d1215-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d1215-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d1215-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1215-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d1215-119">Protocol specifications</span></span>

<span data-ttu-id="d1215-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1215-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1215-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="d1215-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1215-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1215-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1215-123">Gère la récupération des listes d’autorisations de dossier sont stockés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d1215-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1215-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d1215-124">Header files</span></span>

<span data-ttu-id="d1215-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1215-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1215-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d1215-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1215-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d1215-127">Mapitags.h</span></span>
  
> <span data-ttu-id="d1215-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="d1215-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1215-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1215-129">See also</span></span>



[<span data-ttu-id="d1215-130">Propriété canonique PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="d1215-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="d1215-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d1215-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1215-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d1215-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1215-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d1215-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1215-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d1215-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

