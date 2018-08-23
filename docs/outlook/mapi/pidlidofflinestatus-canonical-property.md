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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7d9f8cf4fbdeab70e40447411ed8efd35ef7899e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588775"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="56e1a-103">Propriété canonique PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="56e1a-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="56e1a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56e1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56e1a-105">Détermine l’état d’un fichier de document sur un serveur qui implémente [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="56e1a-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56e1a-106">Propriétés associées</span><span class="sxs-lookup"><span data-stu-id="56e1a-106">Associated properties</span></span>  <br/> |<span data-ttu-id="56e1a-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="56e1a-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="56e1a-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="56e1a-108">Property set:</span></span>  <br/> |<span data-ttu-id="56e1a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="56e1a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="56e1a-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="56e1a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="56e1a-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="56e1a-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="56e1a-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="56e1a-112">Data type:</span></span>  <br/> |<span data-ttu-id="56e1a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="56e1a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="56e1a-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="56e1a-114">Area:</span></span>  <br/> |<span data-ttu-id="56e1a-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="56e1a-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56e1a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="56e1a-116">Remarks</span></span>

<span data-ttu-id="56e1a-117">Le tableau suivant présente les valeurs possibles de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="56e1a-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="56e1a-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="56e1a-118">**Value**</span></span>|<span data-ttu-id="56e1a-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="56e1a-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56e1a-120">0</span><span class="sxs-lookup"><span data-stu-id="56e1a-120">0</span></span>  <br/> |<span data-ttu-id="56e1a-121">Document n’est pas extrait.</span><span class="sxs-lookup"><span data-stu-id="56e1a-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="56e1a-122">1</span><span class="sxs-lookup"><span data-stu-id="56e1a-122">1</span></span>  <br/> |<span data-ttu-id="56e1a-123">Document est extrait par l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="56e1a-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="56e1a-124">2</span><span class="sxs-lookup"><span data-stu-id="56e1a-124">2</span></span>  <br/> |<span data-ttu-id="56e1a-125">Document n’est pas extrait, mais l’utilisateur actuel possède une copie du fichier enregistré pour la modification sur l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="56e1a-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="56e1a-126">Cette propriété est calculée localement et n’est pas envoyée à un serveur à tout moment, sauf si un utilisateur fait glisser l’élément vers un autre compte.</span><span class="sxs-lookup"><span data-stu-id="56e1a-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="56e1a-127">Dans ce cas, il est traité comme une propriété personnalisée définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56e1a-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="56e1a-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="56e1a-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56e1a-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="56e1a-129">Protocol specifications</span></span>

<span data-ttu-id="56e1a-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="56e1a-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="56e1a-131">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="56e1a-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56e1a-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="56e1a-132">Header files</span></span>

<span data-ttu-id="56e1a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="56e1a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="56e1a-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="56e1a-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56e1a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56e1a-135">See also</span></span>



[<span data-ttu-id="56e1a-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="56e1a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56e1a-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="56e1a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56e1a-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="56e1a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56e1a-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="56e1a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

