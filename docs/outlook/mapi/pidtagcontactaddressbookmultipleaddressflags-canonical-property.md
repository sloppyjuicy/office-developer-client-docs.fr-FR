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
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357931"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="d5c7e-103">Propriété canonique PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="d5c7e-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d5c7e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5c7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5c7e-105">Contient des indicateurs qui indiquent si les fournisseurs prendront en charge plusieurs adresses de messagerie par élément de contact.</span><span class="sxs-lookup"><span data-stu-id="d5c7e-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5c7e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d5c7e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5c7e-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d5c7e-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="d5c7e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d5c7e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d5c7e-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="d5c7e-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="d5c7e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d5c7e-110">Data type:</span></span>  <br/> |<span data-ttu-id="d5c7e-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="d5c7e-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="d5c7e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d5c7e-112">Area:</span></span>  <br/> |<span data-ttu-id="d5c7e-113">Carnet d'adresses des contacts</span><span class="sxs-lookup"><span data-stu-id="d5c7e-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5c7e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d5c7e-114">Remarks</span></span>

<span data-ttu-id="d5c7e-115">Si les indicateurs de cette propriété ont la valeur TRUE, le fournisseur n'inclut pas de contacts sans adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d5c7e-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="d5c7e-116">Seule l'adresse de messagerie principale sera honorée.</span><span class="sxs-lookup"><span data-stu-id="d5c7e-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="d5c7e-117">Il s'agit d'une propriété dans la section profil de carnet d'adresses de contacts.</span><span class="sxs-lookup"><span data-stu-id="d5c7e-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d5c7e-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="d5c7e-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d5c7e-119">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="d5c7e-119">Header files</span></span>

<span data-ttu-id="d5c7e-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d5c7e-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5c7e-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d5c7e-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="d5c7e-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d5c7e-122">Mapitags.h</span></span>
  
> <span data-ttu-id="d5c7e-123">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="d5c7e-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5c7e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5c7e-124">See also</span></span>



[<span data-ttu-id="d5c7e-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d5c7e-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5c7e-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d5c7e-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5c7e-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d5c7e-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5c7e-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d5c7e-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

