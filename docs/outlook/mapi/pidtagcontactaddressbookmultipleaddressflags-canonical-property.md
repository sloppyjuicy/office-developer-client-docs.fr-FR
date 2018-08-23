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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588670"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="76785-103">Propriété canonique PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="76785-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="76785-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76785-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76785-105">Contient des indicateurs qui indique si les fournisseurs prendra en charge plusieurs e-mail addresses par élément de contact.</span><span class="sxs-lookup"><span data-stu-id="76785-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76785-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="76785-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76785-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="76785-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="76785-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="76785-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76785-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="76785-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="76785-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="76785-110">Data type:</span></span>  <br/> |<span data-ttu-id="76785-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="76785-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="76785-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="76785-112">Area:</span></span>  <br/> |<span data-ttu-id="76785-113">Carnet d’adresses de contacts</span><span class="sxs-lookup"><span data-stu-id="76785-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76785-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="76785-114">Remarks</span></span>

<span data-ttu-id="76785-115">Si les indicateurs de cette propriété soient TRUE, le fournisseur n’inclut pas les contacts sans les adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="76785-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="76785-116">Uniquement l’adresse de messagerie principale sera respectée.</span><span class="sxs-lookup"><span data-stu-id="76785-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="76785-117">Il s’agit d’une propriété sur une section de profil du carnet d’adresses de contacts.</span><span class="sxs-lookup"><span data-stu-id="76785-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="76785-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="76785-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="76785-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="76785-119">Header files</span></span>

<span data-ttu-id="76785-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76785-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="76785-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="76785-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="76785-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="76785-122">Mapitags.h</span></span>
  
> <span data-ttu-id="76785-123">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="76785-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76785-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76785-124">See also</span></span>



[<span data-ttu-id="76785-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="76785-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76785-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="76785-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76785-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="76785-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76785-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="76785-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

