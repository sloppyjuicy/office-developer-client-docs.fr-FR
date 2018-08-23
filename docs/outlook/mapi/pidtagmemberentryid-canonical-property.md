---
title: Propriété canonique PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 27659b69e0ae050206de18c1258ee593737fbd3b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592947"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="f41e0-103">Propriété canonique PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="f41e0-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f41e0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f41e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f41e0-105">Contient l’identificateur d’entrée directory objet d’un membre de table système access contrôle liste (SACL).</span><span class="sxs-lookup"><span data-stu-id="f41e0-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f41e0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f41e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f41e0-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f41e0-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f41e0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f41e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f41e0-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="f41e0-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="f41e0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f41e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="f41e0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f41e0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f41e0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f41e0-112">Area:</span></span>  <br/> |<span data-ttu-id="f41e0-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="f41e0-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f41e0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f41e0-114">Remarks</span></span>

<span data-ttu-id="f41e0-115">Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour identifier de manière unique une personne ou un rôle auquel s’applique la liste.</span><span class="sxs-lookup"><span data-stu-id="f41e0-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="f41e0-116">Après la création d’un membre de la table SACL, **propriété ENTRYID** ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="f41e0-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="f41e0-117">Pour le modifier, vous devez supprimer le membre de la table et recréer avec un autre **ID d’entrée**.</span><span class="sxs-lookup"><span data-stu-id="f41e0-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f41e0-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f41e0-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f41e0-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f41e0-119">Header files</span></span>

<span data-ttu-id="f41e0-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f41e0-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="f41e0-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f41e0-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="f41e0-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f41e0-122">Mapitags.h</span></span>
  
> <span data-ttu-id="f41e0-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f41e0-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f41e0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f41e0-124">See also</span></span>



[<span data-ttu-id="f41e0-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f41e0-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f41e0-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f41e0-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f41e0-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f41e0-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f41e0-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f41e0-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

