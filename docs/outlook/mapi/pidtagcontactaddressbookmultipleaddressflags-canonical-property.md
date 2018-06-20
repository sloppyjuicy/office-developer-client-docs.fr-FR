---
title: Propriété canonique PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fbe955d3e7a509edf6ba10678e1e2538c9185193
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785808"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="92759-103">Propriété canonique PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="92759-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="92759-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92759-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92759-105">Contient des indicateurs qui indique si les fournisseurs prendra en charge plusieurs e-mail addresses par élément de contact.</span><span class="sxs-lookup"><span data-stu-id="92759-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92759-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="92759-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92759-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="92759-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="92759-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="92759-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92759-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="92759-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="92759-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="92759-110">Data type:</span></span>  <br/> |<span data-ttu-id="92759-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="92759-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="92759-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="92759-112">Area:</span></span>  <br/> |<span data-ttu-id="92759-113">Carnet d’adresses de contacts</span><span class="sxs-lookup"><span data-stu-id="92759-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92759-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="92759-114">Remarks</span></span>

<span data-ttu-id="92759-115">Si les indicateurs de cette propriété soient TRUE, le fournisseur n’inclut pas les contacts sans les adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="92759-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="92759-116">Uniquement l’adresse de messagerie principale sera respectée.</span><span class="sxs-lookup"><span data-stu-id="92759-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="92759-117">Il s’agit d’une propriété sur une section de profil du carnet d’adresses de contacts.</span><span class="sxs-lookup"><span data-stu-id="92759-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92759-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="92759-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="92759-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="92759-119">Header files</span></span>

<span data-ttu-id="92759-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92759-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="92759-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="92759-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="92759-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="92759-122">Mapitags.h</span></span>
  
> <span data-ttu-id="92759-123">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="92759-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92759-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92759-124">See also</span></span>



[<span data-ttu-id="92759-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="92759-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92759-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="92759-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92759-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="92759-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92759-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="92759-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

