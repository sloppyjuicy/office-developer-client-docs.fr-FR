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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 83a645b49e5bb48051bbaedb26058d2da053348b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433037"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="60cf5-103">Propriété canonique PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="60cf5-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="60cf5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60cf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60cf5-105">Contient l’identificateur d’entrée d’objet d’annuaire d’un membre de la table liste de contrôle d’accès système (SACL).</span><span class="sxs-lookup"><span data-stu-id="60cf5-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="60cf5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="60cf5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="60cf5-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="60cf5-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="60cf5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="60cf5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="60cf5-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="60cf5-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="60cf5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="60cf5-110">Data type:</span></span>  <br/> |<span data-ttu-id="60cf5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="60cf5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="60cf5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="60cf5-112">Area:</span></span>  <br/> |<span data-ttu-id="60cf5-113">Règles côté serveur</span><span class="sxs-lookup"><span data-stu-id="60cf5-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60cf5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="60cf5-114">Remarks</span></span>

<span data-ttu-id="60cf5-115">Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour identifier de manière unique une personne ou un rôle auquel la SACL s’applique.</span><span class="sxs-lookup"><span data-stu-id="60cf5-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="60cf5-116">Une fois qu’un membre est créé dans la table SACL, **l’ENTRYID** ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="60cf5-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="60cf5-117">Pour le modifier, vous devez supprimer le membre de la table et le créer à nouveau avec un **autre ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="60cf5-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="60cf5-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="60cf5-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="60cf5-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="60cf5-119">Header files</span></span>

<span data-ttu-id="60cf5-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60cf5-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="60cf5-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="60cf5-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="60cf5-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="60cf5-122">Mapitags.h</span></span>
  
> <span data-ttu-id="60cf5-123">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="60cf5-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="60cf5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60cf5-124">See also</span></span>



[<span data-ttu-id="60cf5-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="60cf5-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="60cf5-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="60cf5-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="60cf5-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="60cf5-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="60cf5-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="60cf5-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

