---
title: Propriété canonique PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431567"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="082d6-103">Propriété canonique PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="082d6-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="082d6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="082d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="082d6-105">Contient un indicateur true lorsque le fournisseur prend en charge plusieurs adresses de messagerie par élément de contact.</span><span class="sxs-lookup"><span data-stu-id="082d6-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="082d6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="082d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="082d6-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="082d6-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="082d6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="082d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="082d6-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="082d6-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="082d6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="082d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="082d6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="082d6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="082d6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="082d6-112">Area:</span></span>  <br/> |<span data-ttu-id="082d6-113">Carnet d’adresses de contact</span><span class="sxs-lookup"><span data-stu-id="082d6-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="082d6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="082d6-114">Remarks</span></span>

<span data-ttu-id="082d6-115">Si cette propriété a la valeur TRUE, le fournisseur n’autorise pas les contacts sans adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="082d6-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="082d6-116">Si la false, le fournisseur indique à tous les contacts s’ils ont ou non une adresse de messagerie principale.</span><span class="sxs-lookup"><span data-stu-id="082d6-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="082d6-117">Seule l’adresse de messagerie principale sera honorée.</span><span class="sxs-lookup"><span data-stu-id="082d6-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="082d6-118">Il s’agit d’une propriété d’un conteneur de carnet d’adresses de contact et d’une colonne dans la table des conteneurs de carnet d’adresses de contact.</span><span class="sxs-lookup"><span data-stu-id="082d6-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="082d6-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="082d6-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="082d6-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="082d6-120">Header files</span></span>

<span data-ttu-id="082d6-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="082d6-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="082d6-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="082d6-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="082d6-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="082d6-123">Mapitags.h</span></span>
  
> <span data-ttu-id="082d6-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="082d6-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="082d6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="082d6-125">See also</span></span>



[<span data-ttu-id="082d6-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="082d6-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="082d6-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="082d6-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="082d6-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="082d6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="082d6-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="082d6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

