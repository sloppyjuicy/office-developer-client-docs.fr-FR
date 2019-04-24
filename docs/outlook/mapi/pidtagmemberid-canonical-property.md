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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342636"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="a1f7c-103">Propriété canonique PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="a1f7c-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="a1f7c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1f7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1f7c-105">Contient l'identificateur d'un membre de table qui possède les droits décrits sur un dossier ou une boîte aux lettres Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1f7c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a1f7c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1f7c-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="a1f7c-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="a1f7c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a1f7c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a1f7c-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="a1f7c-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="a1f7c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a1f7c-110">Data type:</span></span>  <br/> |<span data-ttu-id="a1f7c-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="a1f7c-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="a1f7c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a1f7c-112">Area:</span></span>  <br/> |<span data-ttu-id="a1f7c-113">Contrôle d'accès</span><span class="sxs-lookup"><span data-stu-id="a1f7c-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1f7c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a1f7c-114">Remarks</span></span>

<span data-ttu-id="a1f7c-115">Cette propriété renvoie un identificateur unique à la table.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="a1f7c-116">Un identificateur d'utilisateur d'annuaire est associé à chaque identificateur de membre et est donné par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="a1f7c-117">Cette propriété est utilisée par l'interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour récupérer l'identificateur d'entrée d'annuaire d'un membre avec des droits explicites sur un dossier.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a1f7c-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="a1f7c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1f7c-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a1f7c-119">Protocol specifications</span></span>

<span data-ttu-id="a1f7c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1f7c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1f7c-121">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1f7c-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1f7c-122">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1f7c-123">Gère la récupération des listes d'autorisations de dossier stockées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1f7c-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a1f7c-124">Header files</span></span>

<span data-ttu-id="a1f7c-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a1f7c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1f7c-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a1f7c-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a1f7c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a1f7c-128">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="a1f7c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1f7c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1f7c-129">See also</span></span>



[<span data-ttu-id="a1f7c-130">Propriété canonique PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="a1f7c-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="a1f7c-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a1f7c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1f7c-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a1f7c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1f7c-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a1f7c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1f7c-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a1f7c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

