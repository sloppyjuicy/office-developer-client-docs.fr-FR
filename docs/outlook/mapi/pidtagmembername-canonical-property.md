---
title: Propriété canonique PidTagMemberName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390890"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="d2034-103">Propriété canonique PidTagMemberName</span><span class="sxs-lookup"><span data-stu-id="d2034-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="d2034-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2034-105">Contient le nom complet d’un membre de la table de liste (ACL) du contrôle access.</span><span class="sxs-lookup"><span data-stu-id="d2034-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2034-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d2034-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2034-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="d2034-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="d2034-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d2034-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2034-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="d2034-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="d2034-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d2034-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2034-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d2034-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d2034-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d2034-112">Area:</span></span>  <br/> |<span data-ttu-id="d2034-113">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="d2034-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2034-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2034-114">Remarks</span></span>

<span data-ttu-id="d2034-115">Ces propriétés sont utilisées par le [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface pour afficher le nom d’un membre d’une table ACL, qui est une personne ou un rôle disposant de droits explicites sur un dossier ou d’une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="d2034-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d2034-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d2034-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d2034-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d2034-117">Protocol specifications</span></span>

<span data-ttu-id="d2034-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2034-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2034-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="d2034-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d2034-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d2034-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d2034-121">Gère la récupération des listes d’autorisations de dossier sont stockés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d2034-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d2034-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d2034-122">Header files</span></span>

<span data-ttu-id="d2034-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2034-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2034-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d2034-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2034-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d2034-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d2034-126">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="d2034-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2034-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2034-127">See also</span></span>



[<span data-ttu-id="d2034-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2034-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="d2034-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d2034-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2034-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d2034-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2034-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d2034-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2034-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d2034-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

