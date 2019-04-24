---
title: Propriété canonique PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359898"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="17da2-103">Propriété canonique PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="17da2-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="17da2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17da2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17da2-105">Indique si un délégué peut afficher les objets de message privés de la personne ayant la délégation.</span><span class="sxs-lookup"><span data-stu-id="17da2-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17da2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="17da2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17da2-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="17da2-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="17da2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="17da2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17da2-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="17da2-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="17da2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="17da2-110">Data type:</span></span>  <br/> |<span data-ttu-id="17da2-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="17da2-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="17da2-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="17da2-112">Area:</span></span>  <br/> |<span data-ttu-id="17da2-113">Transmission définie par la classe de message</span><span class="sxs-lookup"><span data-stu-id="17da2-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17da2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="17da2-114">Remarks</span></span>

<span data-ttu-id="17da2-115">Chaque entrée de cette propriété doit être définie sur l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="17da2-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="17da2-116">**Indicateur**</span><span class="sxs-lookup"><span data-stu-id="17da2-116">**Flag**</span></span>|<span data-ttu-id="17da2-117">**Value**</span><span class="sxs-lookup"><span data-stu-id="17da2-117">**Value**</span></span>|<span data-ttu-id="17da2-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="17da2-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="17da2-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="17da2-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="17da2-120">0</span><span class="sxs-lookup"><span data-stu-id="17da2-120">0</span></span>  <br/> |<span data-ttu-id="17da2-121">Le délégué ne doit pas être autorisé à afficher des objets de message privés.</span><span class="sxs-lookup"><span data-stu-id="17da2-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="17da2-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="17da2-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="17da2-123">0,1</span><span class="sxs-lookup"><span data-stu-id="17da2-123">1</span></span>  <br/> |<span data-ttu-id="17da2-124">Le délégué doit être autorisé à afficher des objets de message privés.</span><span class="sxs-lookup"><span data-stu-id="17da2-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="17da2-125">Cette propriété doit être définie dans l'objet information de délégué.</span><span class="sxs-lookup"><span data-stu-id="17da2-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="17da2-126">La valeur de «ShowPrivate» indique que la personne qui a besoin de créer des objets de message privés est visible.</span><span class="sxs-lookup"><span data-stu-id="17da2-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="17da2-127">Cette préférence s'applique à tous les dossiers pour lesquels le délégué a le rôle de réviseur, d'auteur ou d'éditeur.</span><span class="sxs-lookup"><span data-stu-id="17da2-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="17da2-128">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="17da2-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17da2-129">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="17da2-129">Protocol specifications</span></span>

<span data-ttu-id="17da2-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17da2-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17da2-131">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets message et Calendar lorsqu'ils agissent pour le compte d'un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17da2-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17da2-132">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="17da2-132">Header files</span></span>

<span data-ttu-id="17da2-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="17da2-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="17da2-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="17da2-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="17da2-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="17da2-135">Mapitags.h</span></span>
  
> <span data-ttu-id="17da2-136">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="17da2-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17da2-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17da2-137">See also</span></span>



[<span data-ttu-id="17da2-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="17da2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17da2-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="17da2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17da2-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="17da2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17da2-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="17da2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

