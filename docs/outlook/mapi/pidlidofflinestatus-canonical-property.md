---
title: Propriété canonique PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 34f50766c2c45d85bbb0bd9e12d32c5dd87e3cac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785307"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="7f8d8-103">Propriété canonique PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="7f8d8-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="7f8d8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f8d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f8d8-105">Détermine l’état d’un fichier de document sur un serveur qui implémente [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="7f8d8-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f8d8-106">Propriétés associées</span><span class="sxs-lookup"><span data-stu-id="7f8d8-106">Associated properties</span></span>  <br/> |<span data-ttu-id="7f8d8-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="7f8d8-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="7f8d8-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="7f8d8-108">Property set:</span></span>  <br/> |<span data-ttu-id="7f8d8-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="7f8d8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="7f8d8-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="7f8d8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7f8d8-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="7f8d8-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="7f8d8-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7f8d8-112">Data type:</span></span>  <br/> |<span data-ttu-id="7f8d8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7f8d8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7f8d8-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="7f8d8-114">Area:</span></span>  <br/> |<span data-ttu-id="7f8d8-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="7f8d8-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f8d8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f8d8-116">Remarks</span></span>

<span data-ttu-id="7f8d8-117">Le tableau suivant présente les valeurs possibles de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="7f8d8-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="7f8d8-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7f8d8-118">**Value**</span></span>|<span data-ttu-id="7f8d8-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="7f8d8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f8d8-120">0</span><span class="sxs-lookup"><span data-stu-id="7f8d8-120">0</span></span>  <br/> |<span data-ttu-id="7f8d8-121">Document n’est pas extrait.</span><span class="sxs-lookup"><span data-stu-id="7f8d8-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="7f8d8-122">1</span><span class="sxs-lookup"><span data-stu-id="7f8d8-122">1</span></span>  <br/> |<span data-ttu-id="7f8d8-123">Document est extrait par l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7f8d8-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="7f8d8-124">2</span><span class="sxs-lookup"><span data-stu-id="7f8d8-124">2</span></span>  <br/> |<span data-ttu-id="7f8d8-125">Document n’est pas extrait, mais l’utilisateur actuel possède une copie du fichier enregistré pour la modification sur l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7f8d8-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="7f8d8-126">Cette propriété est calculée localement et n’est pas envoyée à un serveur à tout moment, sauf si un utilisateur fait glisser l’élément vers un autre compte.</span><span class="sxs-lookup"><span data-stu-id="7f8d8-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="7f8d8-127">Dans ce cas, il est traité comme une propriété personnalisée définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f8d8-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f8d8-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7f8d8-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f8d8-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="7f8d8-129">Protocol specifications</span></span>

<span data-ttu-id="7f8d8-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="7f8d8-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="7f8d8-131">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="7f8d8-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f8d8-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7f8d8-132">Header files</span></span>

<span data-ttu-id="7f8d8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f8d8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f8d8-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7f8d8-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f8d8-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f8d8-135">See also</span></span>



[<span data-ttu-id="7f8d8-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7f8d8-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f8d8-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7f8d8-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f8d8-138">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7f8d8-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f8d8-139">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="7f8d8-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

