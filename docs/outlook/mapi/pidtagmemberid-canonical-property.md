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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342636"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="b0c18-103">Propriété canonique PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="b0c18-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="b0c18-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0c18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0c18-105">Contient l’identificateur d’un membre de table qui dispose des droits décrits sur Microsoft Exchange Server dossier ou boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="b0c18-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0c18-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b0c18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0c18-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="b0c18-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="b0c18-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b0c18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0c18-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="b0c18-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="b0c18-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b0c18-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0c18-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="b0c18-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="b0c18-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b0c18-112">Area:</span></span>  <br/> |<span data-ttu-id="b0c18-113">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="b0c18-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0c18-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0c18-114">Remarks</span></span>

<span data-ttu-id="b0c18-115">Cette propriété renvoie un identificateur propre au tableau.</span><span class="sxs-lookup"><span data-stu-id="b0c18-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="b0c18-116">Un identificateur d’utilisateur d’annuaire est associé à chaque identificateur de membre et est attribué par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="b0c18-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="b0c18-117">Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour récupérer l’identificateur d’entrée d’annuaire d’un membre avec des droits explicites sur un dossier.</span><span class="sxs-lookup"><span data-stu-id="b0c18-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b0c18-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b0c18-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0c18-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b0c18-119">Protocol specifications</span></span>

<span data-ttu-id="b0c18-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0c18-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0c18-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="b0c18-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0c18-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0c18-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0c18-123">Gère la récupération des listes d’autorisations de dossier stockées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b0c18-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0c18-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b0c18-124">Header files</span></span>

<span data-ttu-id="b0c18-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0c18-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0c18-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b0c18-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0c18-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0c18-127">Mapitags.h</span></span>
  
> <span data-ttu-id="b0c18-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="b0c18-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0c18-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0c18-129">See also</span></span>



[<span data-ttu-id="b0c18-130">Propriété canonique PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="b0c18-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="b0c18-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b0c18-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0c18-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b0c18-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0c18-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b0c18-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0c18-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b0c18-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

