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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d43ec0bd2978c64e3a5ceb635f0dcda57de01cfd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590735"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="9d07d-103">Propriété canonique PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="9d07d-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="9d07d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d07d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d07d-105">Spécifie si un délégué peut afficher des objets de message privé de la personne.</span><span class="sxs-lookup"><span data-stu-id="9d07d-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d07d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9d07d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d07d-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9d07d-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="9d07d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9d07d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d07d-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="9d07d-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="9d07d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9d07d-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d07d-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="9d07d-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="9d07d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9d07d-112">Area:</span></span>  <br/> |<span data-ttu-id="9d07d-113">Message défini par la classe transmissible</span><span class="sxs-lookup"><span data-stu-id="9d07d-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d07d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d07d-114">Remarks</span></span>

<span data-ttu-id="9d07d-115">Chaque entrée de cette propriété doit être définie sur une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d07d-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="9d07d-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="9d07d-116">**Flag**</span></span>|<span data-ttu-id="9d07d-117">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="9d07d-117">**Value**</span></span>|<span data-ttu-id="9d07d-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="9d07d-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9d07d-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="9d07d-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="9d07d-120">0</span><span class="sxs-lookup"><span data-stu-id="9d07d-120">0</span></span>  <br/> |<span data-ttu-id="9d07d-121">Le délégué doit pas afficher les objets de message privé.</span><span class="sxs-lookup"><span data-stu-id="9d07d-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="9d07d-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="9d07d-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="9d07d-123">1</span><span class="sxs-lookup"><span data-stu-id="9d07d-123">1</span></span>  <br/> |<span data-ttu-id="9d07d-124">Le délégué convient pour afficher les objets de message privé.</span><span class="sxs-lookup"><span data-stu-id="9d07d-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="9d07d-125">Cette propriété doit être définie dans l’objet d’informations de délégué.</span><span class="sxs-lookup"><span data-stu-id="9d07d-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="9d07d-126">La valeur de « ShowPrivate » indique que la personne souhaite afficher les objets de message privé.</span><span class="sxs-lookup"><span data-stu-id="9d07d-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="9d07d-127">Cette préférence s’applique à tous les dossiers pour lesquels le délégué a un rôle réviseur, auteur ou l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="9d07d-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9d07d-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9d07d-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d07d-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="9d07d-129">Protocol specifications</span></span>

<span data-ttu-id="9d07d-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d07d-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d07d-131">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d07d-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d07d-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9d07d-132">Header files</span></span>

<span data-ttu-id="9d07d-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d07d-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d07d-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9d07d-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d07d-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9d07d-135">Mapitags.h</span></span>
  
> <span data-ttu-id="9d07d-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="9d07d-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d07d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d07d-137">See also</span></span>



[<span data-ttu-id="9d07d-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9d07d-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d07d-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9d07d-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d07d-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9d07d-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d07d-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9d07d-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

