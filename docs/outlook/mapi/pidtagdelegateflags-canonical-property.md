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
ms.openlocfilehash: 160ddc53edf3d9681adf6f9d536a488c0c345a07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785911"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="18578-103">Propriété canonique PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="18578-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="18578-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18578-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18578-105">Spécifie si un délégué peut afficher des objets de message privé de la personne.</span><span class="sxs-lookup"><span data-stu-id="18578-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18578-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="18578-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18578-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="18578-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="18578-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="18578-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18578-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="18578-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="18578-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="18578-110">Data type:</span></span>  <br/> |<span data-ttu-id="18578-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="18578-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="18578-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="18578-112">Area:</span></span>  <br/> |<span data-ttu-id="18578-113">Message défini par la classe transmissible</span><span class="sxs-lookup"><span data-stu-id="18578-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18578-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="18578-114">Remarks</span></span>

<span data-ttu-id="18578-115">Chaque entrée de cette propriété doit être définie sur une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="18578-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="18578-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="18578-116">**Flag**</span></span>|<span data-ttu-id="18578-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="18578-117">**Value**</span></span>|<span data-ttu-id="18578-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="18578-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18578-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="18578-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="18578-120">0</span><span class="sxs-lookup"><span data-stu-id="18578-120">0</span></span>  <br/> |<span data-ttu-id="18578-121">Le délégué doit pas afficher les objets de message privé.</span><span class="sxs-lookup"><span data-stu-id="18578-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="18578-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="18578-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="18578-123">1</span><span class="sxs-lookup"><span data-stu-id="18578-123">1</span></span>  <br/> |<span data-ttu-id="18578-124">Le délégué convient pour afficher les objets de message privé.</span><span class="sxs-lookup"><span data-stu-id="18578-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="18578-125">Cette propriété doit être définie dans l’objet d’informations de délégué.</span><span class="sxs-lookup"><span data-stu-id="18578-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="18578-126">La valeur de « ShowPrivate » indique que la personne souhaite afficher les objets de message privé.</span><span class="sxs-lookup"><span data-stu-id="18578-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="18578-127">Cette préférence s’applique à tous les dossiers pour lesquels le délégué a un rôle réviseur, auteur ou l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="18578-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18578-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="18578-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18578-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="18578-129">Protocol specifications</span></span>

<span data-ttu-id="18578-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18578-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18578-131">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18578-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18578-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="18578-132">Header files</span></span>

<span data-ttu-id="18578-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18578-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="18578-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="18578-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="18578-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="18578-135">Mapitags.h</span></span>
  
> <span data-ttu-id="18578-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="18578-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18578-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18578-137">See also</span></span>



[<span data-ttu-id="18578-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="18578-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18578-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="18578-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18578-140">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="18578-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18578-141">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="18578-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

