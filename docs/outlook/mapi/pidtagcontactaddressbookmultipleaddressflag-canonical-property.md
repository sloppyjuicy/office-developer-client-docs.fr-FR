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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785819"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a><span data-ttu-id="3f44e-103">Propriété canonique PidTagContactAddressBookMultipleAddressFlag</span><span class="sxs-lookup"><span data-stu-id="3f44e-103">PidTagContactAddressBookMultipleAddressFlag Canonical Property</span></span>

  
  
<span data-ttu-id="3f44e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f44e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f44e-105">Contient un indicateur qui a la valeur TRUE si le fournisseur prend en charge plusieurs adresses de messagerie par élément de contact.</span><span class="sxs-lookup"><span data-stu-id="3f44e-105">Contains a flag that is TRUE when the provider supports multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3f44e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3f44e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f44e-107">PR_CONTAB_MULTI_ADDR_FLAG</span><span class="sxs-lookup"><span data-stu-id="3f44e-107">PR_CONTAB_MULTI_ADDR_FLAG</span></span>  <br/> |
|<span data-ttu-id="3f44e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3f44e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f44e-109">0x6614</span><span class="sxs-lookup"><span data-stu-id="3f44e-109">0x6614</span></span>  <br/> |
|<span data-ttu-id="3f44e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3f44e-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f44e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3f44e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3f44e-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3f44e-112">Area:</span></span>  <br/> |<span data-ttu-id="3f44e-113">Carnet d’adresses de contacts</span><span class="sxs-lookup"><span data-stu-id="3f44e-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f44e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3f44e-114">Remarks</span></span>

<span data-ttu-id="3f44e-115">Si cette propriété a la valeur TRUE, le fournisseur n’autorise pas les contacts sans les adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3f44e-115">If this property is TRUE, the provider does not allow contacts without email addresses.</span></span> <span data-ttu-id="3f44e-116">Si la valeur est FALSE, le fournisseur affiche tous les contacts ou non une adresse de messagerie principale.</span><span class="sxs-lookup"><span data-stu-id="3f44e-116">If FALSE, the provider shows all contacts whether or not they have a primary email address.</span></span> <span data-ttu-id="3f44e-117">Uniquement l’adresse de messagerie principale sera respectée.</span><span class="sxs-lookup"><span data-stu-id="3f44e-117">Only the primary email address will be honored.</span></span> <span data-ttu-id="3f44e-118">Il s’agit d’une propriété sur un conteneur de carnet d’adresses de contacts et une colonne dans la table des conteneurs du carnet d’adresses de contacts.</span><span class="sxs-lookup"><span data-stu-id="3f44e-118">This is a property on a Contact Address Book container, and a column in the table of Contact Address Book containers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3f44e-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3f44e-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3f44e-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3f44e-120">Header files</span></span>

<span data-ttu-id="3f44e-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f44e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f44e-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3f44e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f44e-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3f44e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="3f44e-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="3f44e-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f44e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f44e-125">See also</span></span>



[<span data-ttu-id="3f44e-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3f44e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f44e-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3f44e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f44e-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3f44e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f44e-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3f44e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

